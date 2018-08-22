---
title: A Power BI Premium-kapacitás memóriahasználata és optimalizálása
description: Ismerkedjen meg a Power BI Premium-kapacitás memóriakezelésével és annak optimalizálásával.
ms.date: 04/30/2018
ms.topic: conceptual
ms.service: powerbi
ms.component: powerbi-admin
ms.author: mblythe
ms.reviewer: mblythe
author: mgblythe
manager: kfile
ms.openlocfilehash: aee7fb94f1e132783fc2b7791f7e634c903f7aa6
ms.sourcegitcommit: 1574ecba7530e6e0ee97235251a3138fb0e4789b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/14/2018
ms.locfileid: "40256928"
---
# <a name="power-bi-premium-capacity-resource-management-and-optimization"></a>A Power BI Premium-kapacitás erőforrás-kezelése és optimalizálása

Ebben a cikkben azt ismertetjük, hogyan kezeli erőforrásait a Power BI Premium, valamint tippeket adunk Önnek saját megoldásának tervezése és optimalizálása kapcsán.

## <a name="premium-capacity-memory-management"></a>A prémium szintű kapacitás memóriakezelése

 A prémium szintű kapacitás memóriafelhasználása:

* A betöltött adatkészletek által használt memória
* Adatkészlet (ütemezett és igény szerinti) frissítéséhez használt memória
* Jelentéslekérdezésekhez használt memória

Amikor a kapacitáson belül egy közzétett adatkészletre vonatkozó kérelem érkezik, az adott adatkészletet a rendszer az állandó tárolóból tölti be a memóriába (ezt a folyamatot lemezkép betöltésének is nevezzük). Ha az adatkészlet betöltve marad a memóriában, az adatkészletre vonatkozó későbbi lekérdezések esetén rövidebb lesz a válaszidő. Az adatkészletek memóriában való tárolásához szükséges memórián felül a jelentéslekérdezések és az adatkészlet-frissítések is további memóriát használnak fel.

### <a name="dataset-memory-estimation"></a>Az adatkészlet becsült memóriafelhasználása

Amikor a rendszer megkísérli betölteni az adatkészletet a memóriába, a Power BI megbecsüli, mennyi memóriára lesz szüksége az adatkészletnek a kért parancs végrehajtásához. A memóriában tárolt adatkészletek általában nagyobb méretűek a lemezre mentett adatkészleteknél. Egy adatkészlet frissítéséhez legalább kétszer annyi memóriára van szükség a memóriakapacitásból, mint amennyire egy inaktív adatkészletnek szüksége van.

### <a name="overcommitting-capacity-eviction-and-reloading-of-datasets"></a>Kapacitás túlterhelése, kizárás és adatkészletek újbóli betöltése

A Power BI Premium lehetővé teszi, hogy túlterhelje kapacitását. Közzétehet például több adatkészletet, mint amennyi a kapacitás memóriájában elfér. Ha a kapacitáson belül közzétett adatkészletek több memóriát igényelnek annál, mint amennyit a kapacitás biztosítani tud, egyes adathalmazokat külön, egy állandó tárolóban fog eltárolni a rendszer. Az állandó tároló az egyes kapacitásokhoz tartozó 100 terabájtos tárterület részét képezi.

Tehát mely adatkészletek maradnak a memóriában, és mi történik a többi adatkészlettel? Ahogyan korábban már leírtuk, amikor kérelem érkezik egy adott adatkészletre vonatkozóan, az adatkészlet betöltődik a memóriába (lemezkép betöltése). A kérelem lehet jelentéslekérdezés vagy frissítési műveletet.

Mivel kapacitását túlterhelheti, előfordulhat, hogy kapacitása memóriaterheléssel szembesül. Ha a kapacitás memóriaterheléssel szembesül (mivel új adatkészletet kell betölteni, vagy a betöltött adatkészletekre vonatozó kérelmek megnövelik a memóriaszükségletet), a csomópont *kizár egy vagy több adatkészletet* a kapacitásmemóriát lefoglaló adatkészletek közül. Elsőként az inaktív adatkészletek (amelyekhez jelenleg nem kapcsolódik lekérdezés/frissítési művelet) „legrégebbi használat” (LRU) szerinti kizárása történik meg. Ha új parancs érkezik egy kizárt adatkészletre vonatkozóan, a szolgáltatás megkísérli annak újbóli betöltését a memóriába, adott esetben kizárva más adatkészleteket. Ez a működési mód nagyobb kihasználtságot és hatékonyságot biztosít, mivel a kapacitás így sokkal több adatkészletet tud kiszolgálni, mint amennyi a memóriájában elfér.

Az adatkészletek memóriába történő betöltése viszonylag erőforrás-igényes művelet. A folyamat hossza az adatkészlet méretétől függően változik: kis adatkészletek esetén néhány másodpercig, míg nagy, például 10 gigabájtos adatkészletek esetén több tíz másodpercig, sőt akár percekig is eltarthat. Prémium szintű kapacitás esetén a rendszer a legrégebben használt adatkészleteket igyekszik minél tovább a memóriában tárolni, hogy a kapacitást minél kevesebbszer kelljen újratölteni. Ha további memóriára van szükség, ki kell zárni egy vagy több adatkészletet, a rendszer pedig megpróbálja kiválasztani azokat, amelyek kizárása a legkevésbé befolyásolja majd a felhasználói élményt. Ha további memóriára van szükség, ki kell zárni egy vagy több adatkészletet, a rendszer pedig megpróbálja kiválasztani azokat, amelyek kizárása a legkevésbé befolyásolja majd a felhasználói élményt. A rendszer megpróbálja például elkerülni azoknak az adatkészleteknek a kizárását, amelyek az elmúlt néhány percben használatban voltak, ugyanis az ilyen adatkészletekhez rövid időn belül valószínűleg újabb lekérdezések érkeznek.

Maga a kizárási folyamat egy gyors művelet. Ha kizáráskor az adatkészlet épp nincsen használatban, a felhasználó nem fog sokat észlelni a kizárásból. Ha azonban a kizáráskor egyszerre túl sok adatkészlet van használatban, és nincs elegendő memória mindegyik tárolásához, több kizárás is történhet. Ez „akadozáshoz” vezethet, ugyanis ebben az esetben a rendszer folyamatosan kizárja, majd újból betölti az adatkészleteket, aminek következtében a felhasználók a válaszidők növekedését és a teljesítmény csökkenését tapasztalhatják.

### <a name="dataset-refresh-memory-requirement-competing-with-an-active-dataset-memory-requirement"></a>Az adatkészletek frissítéséhez, valamint a használatban lévő adatkészletekhez szükséges memóriaszükségletek közti versengés

Az adatkészleteket a felhasználók ütemezett módon vagy igény szerint is frissíthetik. Ahogyan korábban már leírtuk, egy teljes frissítéshez legalább kétszer annyi memóriára van szükség, mint amennyire egy betöltött, inaktív adatkészletnek szüksége van. A frissítés megkezdése előtt a rendszer felbecsüli a folyamat memóriaszükségletét. Ha a teljes memóriaszükséglet meghaladja a kapacitáson belül rendelkezésre álló memóriát, a rendszer kizár egy vagy több adatkészletet. Kizáráskor a rendszer a legrégebbi használat szerinti sorrendben választ az adatkészletek közül, tehát igyekszik minél több nemrégiben használt adatkészletet a memóriában tartani.

Ha a kizárás ellenére sem áll rendelkezésre elegendő memória, a rendszer újbóli végrehajtás céljából sorba állítja a frissítési folyamatot. A szolgáltatás egészen addig próbálja újra és újra végrehajtani a folyamatot, amíg sikerrel nem jár, vagy amíg el nem indul egy másik frissítési folyamat.

Ha interaktív lekérdezés érkezik bármelyik adatkészlethez kapcsolódóan a kapacitáson belül, egy folyamatban lévő frissítés miatt azonban nem áll rendelkezésre elegendő memória, az említett kérelem sikertelen lesz, és a felhasználónak újból végre kell azt hajtania.

## <a name="cpu-resource-management-in-premium-capacity"></a>A CPU erőforrás-kezelése prémium szintű kapacitás esetén

A CPU erőforrásait elsősorban az alábbi két folyamat használja:

- Jelentéslekérdezések
- Frissítés (feldolgozás)

### <a name="queries-from-reports"></a>Jelentéslekérdezések

A jelentéslekérdezések a meglévő kapacitásán belül használják a CPU erőforrásait. Ha a jelentés nem hatékony lekérdezéseket tartalmaz, illetve ha az egyidejű felhasználók száma magas, az a CPU erőforrásainak jelentős részét felemésztheti, meglévő kapacitása pedig kevésnek bizonyulhat a terhelés kezeléséhez.

### <a name="refresh-parallelization-policy"></a>A párhuzamos frissítésekre vonatkozó irányelv

Nem a memória az egyetlen olyan erőforrás, melynek kapacitása korlátozhatja az adatkészletek frissítését. Az adott kiszolgáló virtuális magjainak száma szintén befolyásolhatja a folyamatokat. Mivel minden egyes frissítési művelethez adott számú virtuális magra van szükség, a párhuzamosan futtatható frissítések száma korlátozva van. Az alábbi táblázat az egyes termékváltozatokra vonatkozó felső határértéket mutatja. A határértékeken túli, további frissítési műveleteket a rendszer sorba állítja.

 | Termékváltozat  | Háttérrendszeri virtuális magok  | Párhuzamos frissítések modellezése   |
 | --- | --- | --- |
 | A1  | 0,5  | 1  |
 | A2  | 1  | 2  |
 | A3  | 2  | 3  |
 | A4  | 4  | 6  |
 | A5  | 8  | 12  |
 | A6  | 16  | 24  |
 | EM1  | 0,5  | 1  |
 | EM2  | 1  | 2  |
 | EM3  | 2  | 3  |
 | P1  | 4  | 6  |
 | P2  | 8  | 12  |
 | P3  | 16  | 24  |
 | P4  | 32  | 48  |
 | P5  | 64  | 96  |

 > [!TIP]
> Ha a frissítései késlekednek, ellenőrizze, hogy kapacitása egyszerre hány párhuzamos frissítést tud kezelni.

## <a name="example-scenarios"></a>Esetpéldák

Az alábbiakban bemutatunk néhány gyakori helyzetet, valamint azt, hogyan reagál esetükben a szolgáltatás:

 **Húsz, egy időben beküldött, ütemezett frissítés** – A Power BI megkísérli az első *x* frissítés párhuzamos elindítását. Az *x* értékét az adott termékváltozat párhuzamos frissítésekre vonatozó irányelve határozza meg. Ha a Power BI nem tud elég memóriát felszabadítani az inaktív (régebben használt) adatkészletek kizárásával, nem fog az *összes* frissítés egy időben elindulni. Azokat a frissítéseket, amelyek nem tudnak elindulni, a rendszer sorba állítja.

 **Két frissítés fut egy időben, de csak az egyik befejezéséhez van elegendő memória** – Az, amelyik le tud futni, elindul. A másikat a rendszer megpróbálja később újból végrehajtani.

 **Sok adatkészlethez érkeznek lekérdezések, miközben több adatkészlet épp frissül** – Ha nem áll rendelkezésre elegendő memória, a Power BI megkísérli leállítani az aktív frissítéseket, hogy az interaktív lekérdezések lefuthassanak. Ez csökkenti a frissítési teljesítményt.

 **A kapacitás aktuális mérete miatt nem áll rendelkezésre elegendő memória az adatkészlet frissítéséhez** – A frissítés sikertelen lesz. A rendszer nem kísérli meg további memória felszabadítását az adatkészletek kizárásával.

 **Egyetlen adatkészlet frissítése során hirtelen ugrás tapasztalható a memóriahasználatban** – Ha a hirtelen ugrás során fellépő memóriaszükséglet túllépi az inaktív adatkészletek kizárásával felszabadítható memória mennyiségét, a rendszer később újból megkísérli végrehajtani a frissítést, egészen addig, amíg elegendő memória nem áll rendelkezésre a hirtelen ugrás során fellépő memóriaszükséglet biztosításához.

 **Olyan adatkészletre érkezik lekérdezés, amely nem tud elegendő memóriát felszabadítani az inaktív adatkészletek és a frissítési műveletek kizárásával** – Ezek a lekérdezések sikertelenek lesznek. Az ilyen típusú munkaterhelési követelmények esetén nagyobb kapacitást kell megvásárolnia.

## <a name="troubleshooting-and-testing"></a>Hibaelhárítás és tesztelés

Ha a jelentések lassúak vagy nem válaszolnak, teszteljen egy jelentést először egyetlen egy felhasználó esetén. Ezután kezdje el megemelni az egyidejű felhasználók számát, hogy kiderítse, hány felett lassul le a rendszer. A (jelentéslekérdezésekhez kapcsolódó) DAX-függvények finomhangolása sok esetben jelentősen befolyásolhatja a jelentések teljesítményét (és növelheti a kapacitása által támogatott egyidejű felhasználók számát).

Használjon Power BI Embedded-kapacitást az Azure-ban, hogy a különféle termékváltozatok tesztelését követően eldönthesse, melyik a legmegfelelőbb Premium termékváltozat az Ön számára feltételezett munkaterhelése alapján. A Power BI Embedded A4 termékváltozat a P1-gyel, az A5 a P2-vel, az A6 pedig a P3-mal egyezik meg. Az Azure Portal felületén egyszerűen váltogathat a kisebb vagy nagyobb kapacitású termékváltozatok között. Miután megtalálta a munkaterheléséhez legmegfelelőbb termékváltozatot, és befejezte a tesztelést, törölheti is a termékváltozatot.

Bizonyos esetekben sokat megtudhat az adott problémáról, ha megnyitja számítógépén a modell PBIX-fájlját, illetve ellenőrzi a memória- és a CPU-felhasználást. Kisebb modellek esetén próbálkozzon azzal, hogy megnyitja a modellt a számítógépéről, frissíti, majd lekérdezéseket küld rá. Nagyon nagy modellek esetén azonban ez nem fog működni. A modell megnyitásakor ellenőrizze a modell méretét, valamint a memória- és a CPU-felhasználást. Próbáljon meg frissíteni és lekérdezéseket indítani. A feladatkezelő segítségével ellenőrizze a helyi PBIX-fájl CPU- és memóriafelhasználását). Néha magának a számítógépnek a metrikáiból is kiderül, hogy egy alacsonyabb (pl. P1/P2) prémium szintű kapacitás nem feltétlen elegendő az Ön számára.
