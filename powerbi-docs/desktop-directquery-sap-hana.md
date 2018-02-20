---
title: DirectQuery az SAP HANA-hoz a Power BI Desktopban
description: "Megfontolandó szempontok a DirectQuery SAP HANA-val való használatakor"
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 02/05/2018
ms.author: davidi
ms.openlocfilehash: 7bc15607272bf5456b960755a3f6fea9f73d143d
ms.sourcegitcommit: db37f5cef31808e7882bbb1e9157adb973c2cdbc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2018
---
# <a name="directquery-and-sap-hana"></a>DirectQuery és SAP HANA
Az **SAP HANA**-adatforrásokhoz közvetlenül kapcsolódhat a **DirectQuery** használatával. A HANA-hoz való kapcsolódás kétféle módszerrel is elvégezhető:

* **A HANA többdimenziós forrásként való kezelése (alapértelmezett):** Ez az új alapértelmezett beállítás, és jelenleg előzetes verzióban érhető el. Ebben az esetben a rendszer hasonlóan viselkedik ahhoz, amikor a Power BI más többdimenziós forrásokhoz, például az SAP Business Warehouse-hoz vagy az Analysis Serviceshez kapcsolódik. Ha a HANA-hoz ezzel a beállítással kapcsolódik, egyetlen elemzési vagy számítási nézet lesz kiválasztva, és ennek a nézetnek a mértékei, hierarchiái és attribútumai lesznek elérhetőek a mezőlistában. A vizualizációk létrehozásakor az adatok összesítése mindig a HANA-ból lesz lekérdezve. Ez a szokásos és ajánlott eljárás.

* **A HANA relációs forrásként való kezelése:** Ebben az esetben a Power BI relációs forrásként kezeli a HANA-t. Ez nagyobb rugalmasságot tesz lehetővé, de ügyelni kell, hogy a mértékek az elvárt módon legyenek összesítve, és hogy ne merüljenek fel teljesítménybeli problémák.

A kapcsolódáshoz használt módszert egy globális beállítással lehet meghatározni, amelyet a **Fájl > Lehetőségek és beállítások**, majd a **Beállítások > DirectQuery** kiválasztásával, majd pedig **A HANA relációs forrásként való kezelése** választásával lehet beállítani, ahogy az alábbi képen látható. 

![](media/desktop-directquery-sap-hana/directquery-sap-hana_01a.png)

Vegye figyelembe, hogy az **SAP HANA-összekötő** jelenleg **előzetes verzióban** érhető el, és az előzőekben említett beállítások használatához engedélyezni kell. Az SAP HANA új előzetes verziós használatát a **Beállítások > Előzetes verziós funkciók** területen lehet engedélyezni, ahogy az alábbi képen látható.

![](media/desktop-directquery-sap-hana/directquery-sap-hana_01b.png)

Ha a HANA relációs forrásként való kezelését választotta, az minden létrehozott *új* kapcsolatot is befolyásol. Az aktuális jelentésben már meglévő HANA-kapcsolatokra azonban nincs hatással, ahogyan a többi megnyitott jelentés kapcsolatait sem befolyásolja. Ezért ha ez a beállítás nincs engedélyezve, akkor ha az **Adatok beolvasása** lehetőséggel új HANA-kapcsolatot ad hozzá, akkor ez a kapcsolat a HANA-t többdimenziós forrásként kezeli majd. Ha azonban megnyit egy másik jelentést, amely már kapcsolódik a HANA-hoz, akkor az a jelentés továbbra is azt a beállítást alkalmazza, amelyet *a jelentés létrehozásakor* meghatározott. Ez azt is jelenti, hogy a 2018 februárja előtt létrehozott jelentések, amelyek már rendelkeznek HANA-kapcsolattal, továbbra is relációs forrásként kezelik a HANA-t. 

A két megközelítés jelentősen eltérő viselkedéssel jár, és egy már meglévő jelentést nem lehetséges egyikről a másikra változtatni. 

Az alábbiakban részletesen is megvizsgáljuk a két megközelítést.

## <a name="treat-hana-as-a-multi-dimensional-source-default"></a>A HANA többdimenziós forrásként való kezelése (alapértelmezett)

Ez az alapértelmezett viselkedés, és jelenleg előzetes verzióban érhető el. Ezt az előzetes verziójú funkciót az előzőekben ismertetett módon kapcsolhatja be az előzetes funkciók engedélyezésénél. 

Ha ezt az **Előzetes** verziójú funkciót engedélyezte a **Beállítások > Előzetes verziójú funkciók** beállításnál (részletesen lásd az előző szakaszban), akkor minden további új HANA-kapcsolat alapértelmezés szerit ezt a módszert fogja használni, azaz a HANA-t többdimenziós forrásként fogja kezelni. Ha a HANA-kapcsolatot relációs forrásként szeretné kezelni, a **Fájl > Lehetőségek és beállítások** területen jelölje be a **Direct Query > A HANA kezelése relációs forrásként** jelölőnégyzetet. Amíg ez a funkció **előzetes** verzióban van, a többdimenziós megközelítés használatával létrehozott jelentések *nem tehetők közzé* a Power BI szolgáltatásban, és közzétételük esetén hiba jelentkezik, ha a jelentést megnyitják a Power BI szolgáltatásban.  

Ha a HANA-hoz mint többdimenziós forráshoz kapcsolódik, az alábbiak érvényesek:

* Az **Adatok beolvasása navigátorban** egyetlen HANA-nézet választható ki. Egyedi mértékek vagy attribútumok nem választhatók ki. A kapcsolódás idején nincs definiálva lekérdezés, ellentétben az adatimportálással vagy a DirectQuery használatával, amikor a HANA-t relációs forrásként kezeli a rendszer. Ez azt is jelenti, hogy ezzel a kapcsolódási módszerrel nem lehet HANA SQL-t közvetlenül használni.

* A mezőlistában megjelenik a kiválasztott nézethez tartozó összes mérték, hierarchia és attribútum. 

* Mivel a mérték a vizualizációban használatos, a mérték értékét a vizualizációhoz szükséges összesítés szintjén kérdezi le a rendszer a HANA-tól. Ezért a nem additív mértékek esetén (például számlálók, arányok stb.) minden összesítést a HANA végez el, a Power BI-ban már nem történik további összesítés. 

* Ahhoz, hogy midig a helyes összesített értékeket lehessen lekérni a HANA-tól, bizonyos korlátozásokat be kell tartani. Például nem lehetséges hozzáadni számított oszlopokat, vagy ugyanabban a jelentésben több HANA-nézetből származó adatokat kombinálni. 

A HANA többdimenziós forrásként való kezelése nem biztosítja a *relációs* megközelítésnél tapasztalható nagyobb rugalmasságot, de egyszerűbb annál, és helyes összesített értékeket nyújt bonyolultabb HANA-mértékek esetén is, és általában jobb teljesítményt eredményez. 

A **mezők** listája a HANA-nézethez tartozó összes mértéket, attribútumot és hierarchiát tartalmazza. Ennek a módszernek a használatánál az alábbi viselkedés tapasztalható:

* A legalább egy hierarchiában megtalálható attribútumok mindegyike alapértelmezés szerint el lesz rejtve. Szükség esetén azonban meg is jeleníthetőek. Ehhez a mezőlista helyi menüjében válassza a **Rejtettek megjelenítése** lehetőséget. Ugyanebben a helyi menüben szükség esetén meg is jeleníthetőek.

* A HANA-ban meghatározható, hogy az attribútumok címkeként egy másik attribútumot használjanak. Az 1,2,3 stb. értékeket tartalmazó **Product** például címkeként használhatja a **ProductName** attribútumot, amely a Bicikli,Ing,Kesztyű stb. értékeket tartalmazza. Ebben az esetben a mezőlistában egyetlen mezőként a **Product** jelenik meg, amelynek az értékei Bicikli, Ing, Kesztyű stb., de amelynek rendezési alapja és az egyedisége az 1,2,3 kulcsértékek alapján lesz meghatározva. Emellett létre lesz hozva a rejtett **Product.Key** oszlop is, amely lehetővé teszi, hogy szükség esetén hozzá lehessen férni az alapul szolgáló értékekhez is. 

Az alapul szolgáló HANA-ban definiált minden változó megjelenik a kapcsolódáskor, és a szükséges értékek így megadhatók. Ezek az értékek később meg is változtathatók. Ehhez a menüszalagon válassza a **Lekérdezések szerkesztése**, majd a **Változók szerkesztése** lehetőséget a legördülő listából. 

A megengedett modellezési műveletekre szigorúbb korlátozások vonatkoznak, mint általában a DirectQuery használatánál, mivel biztosítani szükséges, hogy a HANA-ból mindig a megfelelő összesített adatok legyenek lekérdezve. Ezzel együtt azonban számos kiegészítés és módosítás is engedélyezett, többek között mértékek definiálása, mezők átnevezése és elrejtése vagy a megjelenítési formátum meghatározása. Az ilyen változások mind megmaradnak frissítés után is, és a HANA-n végzett nem ütköző módosítások is alkalmazva lesznek. 

### <a name="additional-modelling-restrictions"></a>További modellezési korlátozások

A DirectQuery SAP HANA-val való használatakor (azt többdimenziós forrásként kezelve) a legfőbb további modellezési korlátozások a következők: 

* **Nem támogatottak a számított oszlopok:** A számított oszlopok létrehozásának lehetősége le van tiltva. Ez azt is jelenti, hogy a számított oszlopokat létrehozó Csoportosítás és Fürtözés művelet sem érhető el.
* **További mértékkorlátozások:** További, az SAP HANA által nyújtott támogatás szintjét tükröző korlátozások vonatkoznak a mértékekben használható DAX-kifejezésekre.
* **Kapcsolatok definiálása nem támogatott:** Egy jelentésen belül csak egyetlen nézetet lehet lekérdezni, és ezért nem lehetséges kapcsolatokat definiálni.
* **Nincs adatnézet:** Az **Adatnézet** alapértelmezés szerint megjeleníti a részletességiszint-adatokat a táblákban. Az SAP HANA és a hasonló OLAP-források természetéből adódóan az SAP HANA-ban ez a nézet nem érhető el.
* **Az oszlopok és mértékek részletei rögzítettek:** A mezőlistában látható oszlopok és mértékek listája a forrásuk miatt rögzített és nem módosítható. Például nem lehet oszlopokat törölni, sem módosítani az adattípusukat (ugyanakkor át lehet őket nevezni).
* **További korlátozások a DAX-ben:** További, a forrás korlátozásait tükröző korlátozások vonatkoznak a mértékekben használható DAX-re. Például nem lehet a táblákban összesítési függvényeket használni.

### <a name="additional-visualization-restrictions"></a>További vizualizációs korlátozások

A DirectQuery SAP HANA-val való használatakor (azt többdimenziós forrásként kezelve) van néhány korlátozás a vizualizációkban: 
* **Nincs oszlopösszesítés:** Nem módosítható a vizualizációs oszlopok összesítése, a beállítás mindig *Nincs összegzés*.

## <a name="treat-hana-as-a-relational-source"></a>A HANA relációs forrásként való kezelése 

Ha a HANA-hoz mint relációs forráshoz kapcsolódik, elérhetővé válik néhány további lehetőség. Például létrehozhatók számított oszlopok, több HANA-nézetből is felhasználhatók adatok, és az eredményül kapott táblák között kapcsolatok hozhatók létre. Ha azonban ilyen módszerrel használja az SAP HANA-t, fontos tisztában lennie a kapcsolat kezelését érintő néhány szemponttal, amelyek az alábbiakat érintik: 

* A várt eredmények akkor jelennek meg, ha az SAP HANA-nézet nem additív mértékeket tartalmaz (például különböző számadatokat, vagy átlagértékeket egyszerű összegek helyett).
* A kapott lekérdezések hatékonyak

Érdemes gondot fordítani a relációs forrás, például az SQL Server működésének tisztázására, amikor az **Adatok lekérése** utasításban vagy a **Lekérdezésszerkesztőben** meghatározott lekérdezés összesítést végez. A következő példában egy **Lekérdezésszerkesztőben** meghatározott lekérdezés *ProductID* (termékazonosító) szerint rendezve adja vissza az átlagárat.  

![](media/desktop-directquery-sap-hana/directquery-sap-hana_01.png)

Ha a Power BI-ba importálja az adatokat (a DirectQuery helyett), az az alábbiakat eredményezi:

* Az adatok importálása a **Lekérdezésszerkesztőben** létrehozott lekérdezés által meghatározott összesítési szinten történik. Például átlagár termékek szerint rendezve. Ennek eredményeként egy *ProductID* (termékazonosító) és egy *AveragePrice* (átlagár) oszlopokat tartalmazó tábla jön létre, amely vizualizációkban használható.
* Egy vizualizáción belül minden további összesítés (pl. *Sum*, *Average*, *Min* stb.) az importált adatok felhasználásával történik. Ha például belefoglalja az *AveragePrice* (átlagár) értéket egy vizualizációba, akkor a rendszer alapértelmezés szerint a *Sum* (összeg) összesítést fogja használni, és az *AveragePrice* összegét fogja visszaadni minden *ProductID*-hez (termékazonosítóhoz) – amely ebben a példában 13,67. Ugyanez vonatkozik a vizualizációban használt minden alternatív összegzési függvényre (pl. *Min*, *Average* stb.). Az *Average* (átlag) függvény például az *AveragePrice* esetében a 6,66, a 4 és a 3 átlagát fogja visszaadni, ami 4,56, nem pedig az alapul szolgáló tábla 6 rekordjában szereplő *Price* (ár) értékek átlagát, ami 5.17.
  
Ha importálás helyett a **DirectQueryt** használja (ugyanazzal a relációs forrással), akkor is ugyanaz a szemantika, és az eredmények is pontosan ugyanazok lesznek:  

* Ugyanazon lekérdezés esetén logikusan ugyanazok az adatok kerülnek a jelentéskészítési rétegbe, még ha az adatok nem is lettek importálva.

* Egy vizualizáción belül minden további összesítés (*Sum*, *Average*, *Min* stb.) a lekérdezésből származó logikai tábla felhasználásával történik. Az *Average* függvény az *AveragePrice* esetében ekkor is ugyanazt az értéket (4,56) adja vissza.
  
Most vizsgáljuk meg az SAP HANA-t, amikor a kapcsolatot relációs forrásként kezeli. A Power BI az SAP HANA *Analitikus nézetével* és *Számítási nézetével* is működik, és mindkettő tartalmazhat mértékeket. Az SAP HANA jelenlegi módszere viszont szintén az előzőleg ebben a szakaszban bemutatott alapelveket használja: az **Adatok lekérése** utasításban vagy a **Lekérdezésszerkesztőben** meghatározott lekérdezés határozza meg az elérhető adatokat, és a vizualizáción belüli minden további összesítéshez azokat az adatokat használja fel. Ez az importálás és a DirectQuery használata esetén is igaz.  
Azonban a HANA természetéből adódóan a kezdeti **Adatok lekérése** párbeszédablakban vagy a **Lekérdezésszerkesztőben** meghatározott lekérdezés mindig összesítő lekérdezés, és általában olyan mértékeket is tartalmaz, amelyekben a tényleges lekérdezést a HANA-nézet határozza meg.

Az SQL Serverből vett fenti példa megfelelője, hogy adott egy *ID* (azonosító), *ProductID* (termékazonosító) és *DepotID* (raktár-azonosító) adatokból álló HANA-nézet, amely többek között az *AveragePrice* (átlagérték) mértéket is tartalmazza (a nézetben *Average of Price* (ár átlaga) néven van meghatározva).  
    
Ha az **Adatok lekérése** utasítás használatakor kiválasztotta a **ProductID** és az **AveragePrice** mértékeket, akkor az határozza meg a lekérdezést a nézetben, és ezeket az összesített adatokat kéri le (az előző példában az egyszerűség kedvéért egy ál-SQL szerepel, amely nem felel meg tökéletesen a HANA SQL szintaxisának). Ekkor a vizualizáción belül meghatározott minden további összesítés tovább összesíti az ilyen lekérdezések eredményét. Az SQL Server esetében fentebb leírtakhoz hasonlóan ez szintén érvényes az importálásra és a DirectQuery használatára is. Vegye figyelembe, hogy a DirectQuery esetében a rendszer az **Adatok lekérése** utasításból vagy a **Lekérdezésszerkesztőből** származó lekérdezést a HANA-hoz küldött egyetlen lekérdezés részkiválasztásaként használja, így valójában nem történik meg az összes adat beolvasása a további összesítés előtt.  

Mindezek a szempontok és viselkedésmódok az alábbi megfontolásokat teszik szükségessé a DirectQuery HANA-val való használatánál:  

* A vizualizációkban elvégzett minden további összesítésre oda kell figyelni, amikor a HANA-beli mérték nem additív (például nem egyszerű *Sum*, *Min* vagy *Max*).

* Az **Adatok lekérése** utasításban vagy a **Lekérdezésszerkesztőben** csak a szükséges oszlopokat kell kiválasztani a szükséges adatok lekéréséhez, hiszen az eredmény lekérdezés lesz, amelynek a HANA-hoz továbbítható ésszerű lekérdezésnek kell lennie. Például ha több tucat oszlopot választott ki azzal az elgondolással, hogy későbbi vizualizációkban még szüksége lehet rájuk, akkor még egy DirectQuery használatával indított egyszerű lekérdezés esetén is a részkiválasztásban használt összesítő lekérdezés tartalmazni fogja azt a több tucat oszlopot, így az általános teljesítmény igen gyenge lesz.
  
Lássunk erre egy példát. Az alábbi példában öt oszlop van kiválasztva (a **CalendarQuarter**, a **Color**, a **LastName**, a **ProductLine** és a **SalesOrderNumber**) az **Adatok lekérése** párbeszédablakban, illetve az *OrderQuantity* mérték, ez pedig azt jelenti, hogy később egy a Min OrderQuantity (Minimális rendelési mennyiség) mértéket tartalmazó egyszerű vizualizációt kiválasztva az eredmény a következő SQL-lekérdezést küldi a HANA-hoz. Az árnyékolt szakasz a részkiválasztást jelöli, amely az **Adatok lekérése** / **Lekérdezésszerkesztőből** származó lekérdezést tartalmazza. Ha ez a részkiválasztás nagyon magas számosságú eredményt ad, az valószínűleg gyenge HANA-teljesítményt is eredményez.  

![](media/desktop-directquery-sap-hana/directquery-sap-hana_03.png)

   
Ennek következtében ajánlott az **Adatok lekérése** utasításban vagy a **Lekérdezésszerkesztőben** kiválasztott elemeket csak a szükséges elemekre korlátozni úgy, hogy közben továbbra is ésszerű HANA-lekérdezést eredményezzenek.  

## <a name="best-practices"></a>Ajánlott eljárások 

Az SAP HANA-hoz való kapcsolódás mindkét módszerénél a DirectQueryvel kapcsolatos ajánlások a HANA-ra is vonatkoznak, különösképpen a megfelelő teljesítményre vonatkozóak. Ezekről az ajánlásokról részletesen olvashat a [DirectQuery használata a Power BI-ban](desktop-directquery-about.md) című témakörben.
   
## <a name="limitations"></a>Korlátozások

A következő listában található az SAP HANA összes olyan funkciója, amelyek nem teljesen támogatottak, vagy másképp viselkednek a Power BI használatakor. 

* **Szülő-gyermek hierarchiák** – A szülő-gyermek hierarchiák nem lesznek láthatók a Power BI-ban.
Ennek az az oka, hogy a Power BI az SQL-interfészen keresztül érti el a HANA-t, SQL-en keresztül azonban nem érhetők el teljes mértékben a szülő-gyermek hierarchiák.
* **Egyéb hierarchia-metaadatok** – A Power BI megjeleníti a hierarchiák alapvető struktúráját, de egyes hierarchia-metaadatoknak (például hézagos hierarchiák viselkedésének felügyelete) nem lesz hatásuk.
Ez ugyancsak az SQL-interfész használata okozta korlátozások miatt van így.
* **Kapcsolódás SSL használatával** – SSL-használatra konfigurált SAP HANA-hoz nem lehetséges kapcsolódni.
Attribútum-nézet támogatása A Power BI kapcsolódni tud az Elemzési és a Számítási nézetekhez, de nem tud közvetlenül kapcsolódni az Attribútum nézethez.
* **Katalógus objektumok támogatása** – A Power BI nem tud kapcsolódni Katalógus objektumokhoz.
* **Változók módosítása közzétételt követően** – A jelentés közzététele után a Power BI szolgáltatásban közvetlenül nem lehetséges módosítani a HANA-változók értékét. 
 
## <a name="known-issues"></a>Ismert problémák 
Az alábbiakban minden olyan problémát felsorolunk, amely akkor merülhet fel, ha az SAP HANA-hoz a Power BI használatával (DirectQuery) kapcsolódik. 

* **HANA-val kapcsolatos probléma számlálók vagy más mértékek lekérdezésénél** – A HANA helytelen értékeket ad vissza, ha Elemzési nézethez kapcsolódik, és ugyanabban a vizualizációban számláló vagy más, arányt tartalmazó mérték is szerepel. Ezt a viselkedést az SAP 2128928 számú megjegyzése ismerteti (Váratlan eredmények számított oszlop és számláló lekérdezésénél. Az arány mérték ilyen esetben hibás lesz. 

* **Több Power BI-oszlop egy HANA-oszlopból** – Egyes számítási nézeteknél, ahol a HANA-oszlop több hierarchiában is használatos, a HANA az egyetlen oszlopot két külön attribútumként jeleníti meg. Ez azt eredményezi, hogy a Power BI két oszlopot hoz létre.  Ezek az oszlopok alapbeállítás szerint rejtve vannak, és a hierarchiát vagy az oszlopokat érintő minden lekérdezés helyesen működik majd. 
 
## <a name="next-steps"></a>Következő lépések

Ha többet szeretne megtudni a DirectQueryről, tekintse át a következő forrásanyagokat:

* [A DirectQuery használata a Power BI-ban](desktop-directquery-about.md)
* [A DirectQuery által támogatott adatforrások](desktop-directquery-data-sources.md)
* [A DirectQuery és az SAP BW](desktop-directquery-sap-bw.md)
* [Helyszíni adatátjáró](service-gateway-onprem.md)

