---
title: A tárolási mód használata a Power BI Desktopban (előzetes verzió)
description: A tárolási mód használatával szabályozható, hogy az adatok gyorsítótárazva legyenek-e a memóriában a jelentésekhez a Power BI Desktopban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 07/31/2018
ms.author: davidi
LocalizationGroup: Transform and shape data
ms.openlocfilehash: 28dcc4812a37b5ad3f514227f4e5fbcdfebeb579
ms.sourcegitcommit: 06f59902105c93700e71e913dff8453e221e4f82
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/01/2018
ms.locfileid: "39388801"
---
# <a name="storage-mode-in-power-bi-desktop-preview"></a>Tárolási mód a Power BI Desktopban (előzetes verzió)

A **Power BI Desktopban** megadható a táblák **tárolási módja**, ezáltal szabályozható, hogy a táblák adatai gyorsítótárazva legyenek-e a memóriában a jelentésekhez. 

![Tárolási mód a Power BI Desktopban](media/desktop-storage-mode/storage-mode_01.png)

A **tárolási mód** beállítása több előnnyel is jár. Az egyes táblák **tárolási módja** külön adható meg a modellben, így egyetlen adathalmaz a következő előnyök közül akár többet is kihasználhat:

* **Lekérdezési teljesítmény** – amikor a felhasználók Power BI-jelentések vizualizációival dolgoznak, DAX-lekérdezések lesznek továbbítva az adathalmazhoz. Az adatok memóriabeli gyorsítótárazása a **tárolási mód** helyes beállításával fokozza a lekérdezési teljesítményt és a jelentések kezelhetőségét.
* **Nagy adathalmazok** – a nem gyorsítótárazott táblák nem foglalnak memóriát gyorsítótár céljára. Olyan adathalmazokhoz, amelyek túl nagyok vagy szerteágazóak ahhoz, hogy teljes egészükben gyorsítótárazva legyenek a memóriában, engedélyezheti az interaktív elemzést. Ön döntheti el, hogy mely táblákat érdemes gyorsítótárazni, és melyeket nem.
* **Adatfrissítés optimalizálása** – A nem gyorsítótárazott táblákat nem szükséges frissíteni. Csökkentheti a frissítések időigényét, ha csak a szolgáltatási szint és az üzleti igények kielégítéséhez szükséges adatokat gyorsítótárazza.
* **Közel valós idejű követelmények** – a közel valós idejű kezelést igénylő táblákat az adatok késésének csökkentése érdekében jobb nem gyorsítótárazni.
* **Visszaírás** – A visszaírás által az üzleti felhasználók feltételes helyzeteket vizsgálhatnak a cellaértékek módosításával. Az egyéni alkalmazások módosításokat hajthatnak végre az adatforráson. A nem gyorsítótárazott táblákban a változás azonnal megjelenik, így a következmények azonnal elemezhetők.

A **Power BI Desktopban** beállítható **tárolási mód** három összefüggő funkció egyike:

* **Összetett modellek** – Lehetővé teszi, hogy egy jelentés több adatkapcsolattal, köztük DirectQuery-kapcsolatokkal és importtal, vagy ezek bármilyen kombinációjával rendelkezzen.
* **Több-a-többhöz kapcsolatok** – Az **összetett modellekkel** a táblák között **több-a-többhöz kapcsolatok** hozhatók létre, kiküszöbölve ezzel az egyedi értékek követelményét, és szükségtelenné téve a korábbi kerülő megoldásokat, amilyen például új táblák bevezetése a kapcsolatok létrehozásához. 
* **Tárolási mód** – Mostantól megadható, hogy mely vizualizációk igényelnek a háttér-adatforrásokba irányuló lekérdezéseket. Azok, amelyekhez erre nincs szükség, importálva lesznek még akkor is, ha DirectQuery-alapúak. Ezáltal javul a teljesítmény, és csökken a háttérbeli adatforgalom. Korábban még az olyan egyszerű vizualizációk, mint a szeletelők is kezdeményeztek a háttérbeli forrásokba irányuló lekérdezéseket. 

Az **összetett modelleknek** ezt a három, egymással összefüggő funkcióját külön cikkek ismertetik:

* Az **összetett modellekről** a következő cikk szól részletesen: [Összetett modellek a Power BI Desktopban (előzetes verzió)](desktop-composite-models.md).
* A **több-a-többhöz kapcsolatokról** a következő cikk szól részletesen: [Több-a-többhöz kapcsolatok a Power BI Desktopban (előzetes verzió)](desktop-many-to-many-relationships.md).
* A **tárolási mód** funkcióról ez a cikk szól.

## <a name="enabling-the-storage-mode-preview-feature"></a>Az előzetes verziójú tárolási mód funkció engedélyezése

A **Tárolási mód** előzetes verziójú funkció, és azt a **Power BI Desktopban** engedélyezni kell. A **Tárolási mód** funkció engedélyezéséhez válassza a **Fájl > Lehetőségek és beállítások > Lehetőségek > Előzetes verziójú funkciók** lehetőséget, majd jelölje be az **összetett modellek** jelölőnégyzetet. 

![előzetes funkciók engedélyezése](media/desktop-composite-models/composite-models_02.png)

Ahhoz, hogy a funkció engedélyezve legyen, újra kell indítania a **Power BI Desktopot**.

![a változások érvénybe léptetéséhez újraindítás szükséges](media/desktop-composite-models/composite-models_03.png)


## <a name="using-the-storage-mode-property"></a>A tárolási mód tulajdonság használata

A **tárolási mód** egy tulajdonság, amely a modell minden táblájához beállítható. A **tárolási mód** beállításához jelölje ki a táblát a **Mezők** panelen, majd kattintson rá a jobb gombbal a helyi menü megnyitásához. A helyi menüből válassza a **Tulajdonságok** lehetőséget.

![A Tulajdonságok kiválasztása a helyi menüben](media/desktop-storage-mode/storage-mode_02.png)

A **tárolási mód** szakasz a tábla **Mezőtulajdonságok** paneljén jelenik meg. Itt megtekintheti az aktuális **tárolási módot**, és módosíthatja is.

![Tábla tárolási módjának beállítása](media/desktop-storage-mode/storage-mode_03.png)

A **tárolási mód** értéke háromféle lehet:

* **Importálás** – Az **Importálás** beállítású importált táblák gyorsítótárazva lesznek. A Power BI adathalmazra irányuló, importált táblákból adatokat visszaadó lekérdezések csak a gyorsítótárazott adatokon hajthatók végre.
* **DirectQuery** – Az így beállított DirectQuery-táblák nem lesznek gyorsítótárazva. A Power BI adathalmazra irányuló (például DAX), DirectQuery-táblákból adatokat visszaadó lekérdezések csak igény szerinti lekérdezéseknek az adatforráson való futtatásával hajthatók végre. Az adatforrásra irányuló lekérdezések az adott adatforrás lekérdezési nyelvét (például SQL) használják.
* **Kettős** – A kettős beállítású táblák gyorsítótárazottként és nem gyorsítótárazottként is viselkedhetnek a Power BI adathalmazra irányuló lekérdezés környezetétől függően. A lekérdezések bizonyos esetekben a gyorsítótárazott adatok alapján teljesülnek. Más esetekben a lekérdezések teljesítése egy igény szerinti lekérdezésnek az adatforráson való futtatásával történik.

Egy tábla tulajdonságának Importálásra állítása *visszafordíthatatlan* művelet. Több nem lehet visszaállítani DirectQueryre vagy Kettősre.

## <a name="constraints-on-directquery-and-dual-tables"></a>A DirectQuery és Kettős táblákra vonatkozó megkötések

A Kettős táblákra ugyanazok a megkötések vonatkoznak, mint a DirectQuery-táblákra. Ezek közé tartozik az M átalakítások korlátozása, és a DAX-függvények korlátozott használata a számított oszlopokban. További tudnivalók: [A DirectQuery használatának következményei](desktop-directquery-about.md#implications-of-using-directquery)

## <a name="relationship-rules-on-tables-with-different-storage-modes"></a>Eltérő tárolási módú táblákra vonatkozó kapcsolati szabályok

A kapcsolatoknak eleget kell tenniük a kapcsolódó táblák **tárolási módja** alapján meghatározott szabályoknak. Ez a fejezet érvényes kapcsolatokra mutat példákat. Teljes körű tájékoztatást a [Több-a-többhöz kapcsolatok a Power BI Desktopban (előzetes verzió)](desktop-many-to-many-relationships.md) című cikkben talál.

Egyetlen adatforrással rendelkező adathalmaz esetén az alábbi összetételű **egy-a-többhöz** kapcsolatok érvényesek:

| Tábla a **több** oldalon | Tábla az **egy** oldalon |
| ------------- |----------------------| 
| Kettős          | Kettős                 | 
| Importálás        | Importálás vagy kettős       | 
| DirectQuery   | DirectQuery vagy kettős  | 

## <a name="propagation-of-dual"></a>Kettős mód propagálása
Lássunk erre egy példát. Tekintsük meg az alábbi egyszerű modellt, amelyben minden tábla egyetlen, az Importálást és a DirectQuery-t is támogató forrásból származik.

![Példa Kapcsolat nézete a tárolási mód bemutatásához](media/desktop-storage-mode/storage-mode_04.png)

Tegyük fel, hogy kezdetben a modell minden táblája DirectQuery beállítású. Ha a *SurveyResponse* tábla **tárolási módját** Importálásra állítjuk, megjelenik az alábbi üzenet:

![Tárolási mód figyelmeztetés ablak](media/desktop-storage-mode/storage-mode_05.png)

A dimenziótáblák (*Customer*, *Date* és *Geography*) beállításának **Kettősnek** kell lennie, hogy eleget tegyenek a fent leírt kapcsolati szabályoknak. Ezeket a táblákat nem kell előre **Kettős** tárolási módra állítani, hanem egyetlen művelettel átállíthatók.

A propagálási logika úgy van megtervezve, hogy segítsen a sok táblát tartalmazó modellek esetében. Tegyük fel, hogy a modellje 50 táblát tartalmaz, és csak bizonyos tény- (tranzakciós) táblákat kell gyorsítótárazni. A **Power BI Desktop** logikája megállapítja a dimenziótáblák legszűkebb halmazát, amelyet **Kettősre** kell beállítani, így ezt Önnek nem kell megtennie.

A propagálási logika csak az **egy-a többhöz** kapcsolatok „egy” oldalát járja be.

* A *Customer* tábla **Importálás** beállítása (a *SurveyResponse* módosítása helyett) nem megengedett, mert kapcsolatban áll a *Sales* és *SurveyResponse* DirectQuery-táblákkal.
* A *Customer* tábla **Kettős** beállítása (a *SurveyResponse* módosítása helyett) megengedett. A propagálási logika a *Geography* táblát is **Kettősre** állítja be.

## <a name="storage-mode-usage-example"></a>Példa a tárolási mód használatára
Folytatva az előző szakaszban megkezdett példát, tegyük fel, hogy a következő **Tárolási mód** beállításokat alkalmaztuk:

| Tábla                   | Tárolási mód         |
| ----------------------- |----------------------| 
| *Sales*                 | DirectQuery          | 
| *SurveyResponse*        | Importálás               | 
| *Date*                  | Kettős                 | 
| *Customer*              | Kettős                 | 
| *Geography*             | Kettős                 | 


Ezek a tárolásimód-beállítások a következő viselkedést eredményezik, feltéve hogy a *Sales* tábla jelentős mennyiségű adatot tartalmaz.
* A dimenziótáblák (*Date*, *Customer* és *Geography*) gyorsítótárazva lesznek, így a jelentések első betöltésének gyorsnak kell lennie a megjelenítendő szeletelő-értékek lekérésekor.
* Ha a *Sales* tábla nincs gyorsítótárazva, az a következő eredményekkel jár:
    * Az adatfrissítési idők javulnak, a memóriahasználat pedig csökken
    * A jelentéseknek a *Sales* táblán alapuló lekérdezései DirectQuery-módban futnak, ami tovább tarthat, de közelebb áll a valós időhöz, mert nem jár gyorsítótárazási késéssel

* A jelentéseknek a *SurveyResponse* táblán alapuló lekérdezései a memóriabeli gyorsítótárból térnek vissza, ezért viszonylag gyorsnak kell lenniük.

## <a name="queries-that-hit-or-miss-the-cache"></a>A gyorsítótárat érintő vagy elkerülő lekérdezések

Az **SQL Profilert** a **Power BI Desktop** diagnosztikai portjára csatlakoztatva a következő események nyomkövetésével megállapítható, hogy mely lekérdezések érintik vagy kerülik el a gyorsítótárat:

* Queries Events\Query Begin
* Query Processing\Vertipaq SE Query Begin
* Query Processing\DirectQuery Begin

Minden *Query Begin* (lekérdezés kezdete) eseménynél ellenőrizze az azonos *ActivityID* tevékenységazonosítóval rendelkező többi eseményt. Ha például nincs *DirectQuery Begin* esemény, *Vertipaq SE Query Begin* esemény viszont van, akkor a lekérdezés a gyorsítótárból kapott választ.

A **Kettős** módú táblákra hivatkozó lekérdezések lehetőség szerint a gyorsítótárból adnak vissza adatokat, egyébként a DirectQueryre hagyatkoznak.

A korábbi példát folytatva, a következő lekérdezés csak a **Kettős** módban lévő *Date* tábla egyik oszlopára hivatkozik. Így tehát a gyorsítótárhoz kell fordulnia.

![Szkript a tárolási mód diagnosztizálásához](media/desktop-storage-mode/storage-mode_06.png)

A következő lekérdezés csak a **DirectQuery** módban lévő *Sales* tábla egyik oszlopára hivatkozik. Így tehát *nem* fordulhat a gyorsítótárhoz.

![Szkript a tárolási mód diagnosztizálásához](media/desktop-storage-mode/storage-mode_07.png)

A következő lekérdezés érdekessége, hogy mindkét oszlop szerepel benne. Ez a lekérdezés elkerüli a gyorsítótárat. Számítani lehetett volna arra, hogy a *CalendarYear* értékeket a gyorsítótárból, a *SalesAmount* értékeket padig a forrásból kéri le, majd kombinálja az eredményeket, ez azonban kevésbé volna hatékony, mint a forrásrendszerhez továbbítani a SUM/GROUP BY műveletet. A műveletet a forrásnak leküldve a visszaadott sorok száma valószínűleg sokkal kisebb lesz. 

![Szkript a tárolási mód diagnosztizálásához](media/desktop-storage-mode/storage-mode_08.png)

> [!NOTE]
> Ez a viselkedés gyorsítótárazott és nem gyorsítótárazott táblák együttes használatakor más, mint a [Több-a-többhöz kapcsolatok a Power BI Desktopban (előzetes verzió)](desktop-many-to-many-relationships.md) leírt.

## <a name="caches-should-be-kept-in-sync"></a>A gyorsítótárakat szinkronizálva kell tartani

Az előző szakaszban bemutatott lekérdezések szemléltették, hogy a **Kettős** módú táblák bizonyos esetekben érintik, más esetekben elkerülik a gyorsítótárat. Emiatt előfordulhat, hogy ha a gyorsítótár elavul, különböző értékek lesznek visszaadva. A lekérdezések végrehajtása nem kísérli meg elfedni az adatokkal kapcsolatos problémákat például azzal, hogy a DirectQuery-eredményeket a gyorsítótárazott értékekkel való egyezés alapján szűri. Önnek kell ismernie a saját adatfolyamait, és azok alapján terveznie. Léteznek bevált módszerek az ilyen eseteknek a forrásnál való kezelésére, ha szükséges.

A **Kettős** tárolási mód teljesítmény-optimalizálás. Csak olyan módon szabad használni, hogy ne veszélyeztesse az üzleti követelmények teljesítésének képességét. Másféle viselkedés eléréséhez fontolja meg a [Több-a-többhöz kapcsolatok a Power BI Desktopban (előzetes verzió)](desktop-many-to-many-relationships.md) című cikkben ismertetett módszerek használatát.

## <a name="data-view"></a>Adatnézet
Ha az adathalmazban legalább egy tábla Importálás vagy Kettős **tárolási módra** van beállítva, akkor megjelenik az **Adatnézet** fül.

![Adatnézet a Power BI Desktopban](media/desktop-storage-mode/storage-mode_09.png)

Az *adatnézetben** kijelölt **Kettős** és **Importálás** módú táblákhoz megjelennek a gyorsítótárazott adatok. A DirectQuery-táblák adatai nem láthatók, és megjelenik egy üzenet, amely szerint a DirectQuery-táblák nem jeleníthetők meg.


## <a name="limitations-and-considerations"></a>Korlátozások és szempontok

A **tárolási módnak** erre a verziójára és az **összetett modellekkel** való viszonyára érvényes néhány korlátozás.

Az alábbi többdimenziós források nem használhatók **összetett modellekkel**:

* SAP HANA
* SAP Business Warehouse
* SQL Server Analysis Services
* Power BI-adathalmazok

Ha ezekhez a többdimenziós forrásokhoz a DirectQuery használatával csatlakozik, nem tud ugyanakkor más DirectQuery-forráshoz is csatlakozni, és importált adatokkal kombinálni sem.

A DirectQuery használatára jelenleg vonatkozó korlátozások az **összetett modellek** használatára is érvényesek. Sok ilyen korlátozás jelenleg táblánként értendő, a tábla **tárolási módjától** függően. Egy importált tábla egy számított oszlopa például hivatkozhat más táblákra, egy DirectQuery-tábla számított oszlopai viszont továbbra is csak a táblán belüli oszlopokra hivatkozhatnak. Más korlátozások a modell egészére vonatkoznak, ha a modellen belül bármelyik tábla DirectQuery módban van. A **QuickInsights** és a **Q&A** funkciók például nem érhetők el a modellben, ha a táblák bármelyikének **tárolási módja** DirectQuery. 

## <a name="next-steps"></a>Következő lépések

Az alábbi cikkek bővebben ismertetik az összetett modelleket, és a DirectQuery részletes leírását is tartalmazzák.

* [Összetett modellek a Power BI Desktopban (előzetes verzió)](desktop-composite-models.md)
* [Több-a-többhöz kapcsolatok a Power BI Desktopban (előzetes verzió)](desktop-many-to-many-relationships.md)

A DirectQuery-vel kapcsolatos cikkek:

* [DirectQuery használata a Power BI-ban](desktop-directquery-about.md)
* [A DirectQuery által támogatott adatforrások a Power BI-ban](desktop-directquery-data-sources.md)

