---
title: Több-a-többhöz kapcsolatok a Power BI Desktopban (előzetes verzió)
description: Több-a-többhöz kapcsolatok használata a Power BI Desktopban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 07/31/2018
ms.author: davidi
LocalizationGroup: Transform and shape data
ms.openlocfilehash: 40799bb2716b2f6e85405e76c2a301acef3509aa
ms.sourcegitcommit: 06f59902105c93700e71e913dff8453e221e4f82
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/01/2018
ms.locfileid: "39388755"
---
# <a name="many-to-many-relationships-in-power-bi-desktop-preview"></a>Több-a-többhöz kapcsolatok a Power BI Desktopban (előzetes verzió)

A **Power BI Desktop** **több-a-többhöz kapcsolatok** funkciójával **több-a-többhöz** számosságú táblák kapcsolhatók össze, így a több adatforrást tartalmazó adatmodellek egyszerűbb és ésszerűbb módon hozhatók létre. A **több-a-többhöz kapcsolatok** funkció a **Power BI Desktop** tágabb **összetett modellek** képességének része.

![több-a-többhöz a Kapcsolat szerkesztése párbeszédpanelen](media/desktop-many-to-many-relationships/many-to-many-relationships_01.png)

A **Power BI Desktopban** beállítható **több-a-többhöz kapcsolatok** három összefüggő funkció együttesének egy részét képezik:

* **Összetett modellek** – Lehetővé teszi, hogy egy jelentés több adatkapcsolattal, köztük DirectQuery-kapcsolatokkal és importtal, vagy ezek bármilyen kombinációjával rendelkezzen.
* **Több-a-többhöz kapcsolatok** – Az **összetett modellekkel** a táblák között **több-a-többhöz kapcsolatok** hozhatók létre, kiküszöbölve ezzel az egyedi értékek követelményét, és szükségtelenné téve a korábbi kerülő megoldásokat, amilyen például új táblák bevezetése a kapcsolatok létrehozásához. 
* **Tárolási mód** – Mostantól megadható, hogy mely vizualizációk igényelnek a háttér-adatforrásokba irányuló lekérdezéseket. Azok, amelyekhez erre nincs szükség, importálva lesznek még akkor is, ha DirectQuery-alapúak. Ezáltal javul a teljesítmény, és csökken a háttérbeli adatforgalom. Korábban még az olyan egyszerű vizualizációk, mint a szeletelők is kezdeményeztek a háttérbeli forrásokba irányuló lekérdezéseket. 

Az **összetett modelleknek** ezt a három, egymással összefüggő funkcióját külön cikkek ismertetik:

* Az **összetett modellekről** a következő cikk szól részletesen: [Összetett modellek a Power BI Desktopban (előzetes verzió)](desktop-composite-models.md).
* A **több-a-többhöz kapcsolatokat** ez a cikk ismerteti.
* A **tárolási módokról** a következő cikk szól részletesen: [Tárolási mód a Power BI Desktopban (előzetes verzió)](desktop-storage-mode.md).

## <a name="enabling-the-many-to-many-relationships-preview-feature"></a>A több-a-többhöz kapcsolatok funkció engedélyezése

A **több-a-többhöz kapcsolatok** funkció az **összetett modellek** képesség része, és előzetes verzióban van, ezért engedélyezni kell a **Power BI Desktopban**. Az **Összetett modellek** funkció engedélyezéséhez válassza a **Fájl > Lehetőségek és beállítások > Lehetőségek > Előzetes verziójú funkciók** lehetőséget, majd jelölje be az **összetett modellek** jelölőnégyzetet.

![előzetes funkciók engedélyezése](media/desktop-composite-models/composite-models_02.png)

Ahhoz, hogy a funkció engedélyezve legyen, újra kell indítania a **Power BI Desktopot**.

![a változások érvénybe léptetéséhez újraindítás szükséges](media/desktop-composite-models/composite-models_03.png)


## <a name="what-many-to-many-relationships-solves"></a>A több-a-többhöz kapcsolatok által megoldott problémák

A **több-a-többhöz kapcsolatok** elérhetővé válása előtt a Power BI-ban két tábla közötti kapcsolat definiálásakor legalább az egyik érintett oszlopnak egyedi értékeket kellett tartalmaznia. Sok esetben azonban a tábla egyetlen oszlopa sem tartalmazott egyedi értékeket. 

A két tábla tartalmazhatott például egy-egy *Ország* oszlopot, de az *Ország* értékei egyik táblában sem egyediek. Két ilyen tábla összekapcsolásához áthidaló megoldásként például a szükséges egyedi értékeket tartalmazó további táblákat kellett beépíteni a modellbe. A **több-a-többhöz kapcsolatok** funkció más megoldást kínál, lehetővé téve az ilyen táblák közvetlen összekapcsolását egy **több-a-többhöz** számosságú kapcsolattal.  

## <a name="using-many-to-many-relationships"></a>A több-a-többhöz kapcsolatok használata

Amikor kapcsolatot definiál két tábla között a Power BI-ban, meg kell adnia a kapcsolat számosságát. Például a *ProductSales* (értékesítések) és *Product* (termék) táblák közötti kapcsolat (a *ProductSales[ProductCode]* és a *Product[ProductCode]* mezők alapján) **több-az-egyhez** kapcsolatként lenne definiálva, mivel egy termékhez több értékesítés is tartozhat, a *Product* tábla *(ProductCode)* (termékkód) oszlopa pedig egyedi. Amikor egy kapcsolat számosságaként **több-az-egyhez**, **egy-a-többhöz** vagy **egy-az-egyhez** van megadva, a Power BI érvényesítést végez, és ellenőrzi, hogy a megadott számosság megfelel-e a tényleges adatoknak.

Vegyük például az alábbi ábrán látható egyszerű modellt.

![kapcsolat nézet](media/desktop-many-to-many-relationships/many-to-many-relationships_02.png)

Tegyük fel, hogy a *Product* (termék) tábla csak két sorból áll.

![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_03.png)

Tegyük fel továbbá, hogy a *Sales* (termékértékesítések) tábla csak négy sorból áll, köztük (egy hivatkozás-integritási hiba következtében) a *Product* táblában nem szereplő **C** termék értékesítését leíró *Sales* rekorddal.

![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_04.png)

Egy olyan vizualizáció, amely minden termékhez megmutatja a termék nevét (*ProductName*) és árát (*Price*) (a *Product* táblából), valamint az egyes termékek összes mennyiségét (*Qty*) (a *ProductSales* táblából) a következő ábrán látható módon jelenne meg: 

![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_05.png)

Amint a fenti ábrán látható, a vizualizáció egyik sorában a *ProductName* mező üres. Ez tartozik a *C* termék értékesítéséhez. Ez az üres sor a következőket veszi figyelembe:

* A *ProductSales* tábla minden sorát, amelynek nem felel meg sor a *Product* táblában – ez hivatkozás-integritási hiba, amit példánkban a *C* termék esetében láttunk.

* A *ProductSales* tábla minden sorát, amely a külsőkulcs-oszlopban Null értéket tartalmaz. 

A fenti okokból az üres sor mindkét esetben olyan eladásoknak felel meg, ahol a termék neve (*ProductName*) és ára (*Price*) ismeretlen.

Olykor azonban az is előfordul, hogy a táblák két oszlop alapján vannak összekapcsolva, de egyik oszlop sem egyedi. Vegyük például a következő két táblát:

* A *Sales* (értékesítések) tábla államonként (*State*) tartalmazza az értékesítéseket, soronként megadva az államban (CA, WA és TX államban) adott módon (Type) értékesített mennyiséget (Sales) 

    ![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_06.png)

* A *CityData* tábla városok (City) adatait tartalmazza, köztük a lakosságot (Population) és az államot (State) (CA, WA és New York állam)

    ![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_07.png)

Bár mindkét táblában van *State* (állam) oszlop, és elképzelhető, hogy az értékesítéseket (*Sales*) államonként (*State*), az egyes államok lakosságával együtt bemutató jelentést szeretnénk készíteni, van egy probléma: a *State* oszlop egyik táblában sem egyedi. 

## <a name="the-prior-workaround"></a>A korábbi áthidaló megoldás

A **Power BI Desktopnak** a 2018. júliusi kiadás előtti verzióiban ezek között a táblák között nem lehetett közvetlen kapcsolatot létrehozni. A probléma gyakran alkalmazott áthidaló megoldása a következő lépésekből állt:

* Egy harmadik, csak az egyedi államazonosítókat (*State*) tartalmazó tábla létrehozása. Ez lehetett (a DAX használatával definiált) számított tábla, vagy a **Lekérdezésszerkesztőben** megadott lekérdezéssel létrehozott tábla, amely a táblák egyikéből kinyert egyedi azonosítókat, vagy a két halmaz teljes unióját tartalmazta.

* A két eredeti tábla és az új tábla összekapcsolása a szokásos **több-az-egyhez* kapcsolatokkal.

Ez az áthidaló tábla maradhatott látható, de el is lehetett rejteni, hogy nem jelenjen meg a mezőlistában. Az utóbbi esetben a **több-az-egyhez** kapcsolat általában kétirányú szűrésre volt beállítva, hogy bármelyik tábla *State* mezője használható legyen, amelyet aztán keresztszűrés vitt át a másik táblára. Ezt a kerülő megoldást mutatja be a **Kapcsolat nézetről** készült alábbi kép.

![kapcsolat nézet](media/desktop-many-to-many-relationships/many-to-many-relationships_08.png)

Az államokat (*State*) (a *CityData* táblából) a teljes lakossággal (*Population*) és az összes értékesített mennyiséggel (*Sales*) együtt bemutató vizualizáció ekkor az alábbihoz hasonló lenne.

![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_09.png)

Figyelje meg, hogy mivel ez az áthidaló megoldás az államot a *CityData* táblából veszi, csak az ebben a táblában szereplő *State* értékek jelennek meg (TX állam így kimaradt). Ezen felül, a **több-az-egyhez** kapcsolatoktól eltérően, bár az összeg sor minden *Sales* értéket figyelembe vesz (a TX államhoz tartozókat is), a részletezésben nincs a nem párosított soroknak megfelelő üres sor. Ugyanígy azoknak a *Sales* értékeknek sem felelne meg üres sor, amelyekhez Null érték tartozik a *State* oszlopban.

Ha a *City* (város) mező is hozzá lenne adva a vizualizációhoz, akkor bár az egyes *városok* lakossága ismert, a *City* mellett feltüntetett *Sales* értékek egyszerűen a megfelelő államhoz (*State*) tartozó *Sales* értékek ismétlései lennének (ez történik olyan oszlop szerinti csoportosítás esetén, amelyhez nem kapcsolódik összesíthető érték). Ezt mutatja be az alábbi ábra.

![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_10.png)

Ha az áthidaló megoldáshoz létrehozott az új tábla *Sales* oszlopa az összes *States* mező uniójaként volna definiálva, és meg lenne jelenítve a mezőlistában, akkor ugyanez a vizualizáció, amely a *State* (az új tábla alapján) mellett a teljes lakosságot (*Population*) és a teljes értékesített mennyiséget (*Sales*) mutatja be, a következőképpen nézne ki.

![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_11.png)

Ebben az esetben a vizualizációban *TX* (*Sales* értékkel, de ismeretlen lakossággal) és *New York* (ismert lakossággal de *Sales* érték nélkül) is szerepelne. 

Mint látható, ez az áthidaló megoldás nem optimális, és számos problémával jár. A **több-a-többhöz kapcsolatok** létrehozásának célja ezeknek a problémáknak a megoldása, a következő bekezdésben leírtak szerint.

## <a name="using-many-to-many-relationships-instead-of-the-workaround"></a>Több-a-többhöz kapcsolatok használata áthidaló megoldás helyett

A **Power BI Desktop** 2018. júliusi verziójától kezdve az előző bekezdésekben leírt táblák közvetlenül összekapcsolhatók, és nincs többé szükség áthidaló megoldásokra. A kapcsolatok mostantól **több-a-többhöz** számosságúra állíthatók, ezzel jelezve, hogy egyik tábla sem egyedi értékeket tartalmaz. Ilyen kapcsolatokhoz is megadható, hogy melyik tábla szűri a másikat, vagy hogy a szűrés kétirányú legyen, és a táblák kölcsönösen szűrjék egymást.  

> [!NOTE]
> A **több-a-többhöz** kapcsolatok létrehozásának lehetősége előzetes verzióban érhető el, és amíg előzetes verziójú, addig a **több-a-többhöz** kapcsolatokat használó modellek nem tehetők közzé a Power BI szolgáltatásban. 

A **Power BI Desktop** alapértelmezés szerint **több-a-többhöz** számosságot állít be, ha azt észleli, hogy egyik tábla sem egyedi értékeket tartalmaz a kapcsolatban részt vevő oszlopokban. Ilyen esetben figyelmeztetés jelenik meg, amelyben meg kell erősíteni, hogy a kapcsolat beállítása a kívánt viselkedés, nem pedig egy adathiba nem szándékos következménye. 

Amikor például közvetlen kapcsolatot hozunk létre a *CityData* és a *Sales* táblák között, ahol a szűrés a *CityData* felől a *Sales* táblára irányul, akkor az alábbi ábrán látható figyelmeztetés jelenik meg.

![Kapcsolat szerkesztése párbeszédpanel](media/desktop-many-to-many-relationships/many-to-many-relationships_01.png)

Az így keletkező **Kapcsolat nézetben** ekkor a két tábla közötti közvetlen **több-a-többhöz** kapcsolat látszana. A **Mezők** listában való megjelenés és az ez utáni viselkedés a vizualizációk létrehozásakor ugyanolyan lesz, mint az előző bekezdésben leírt áthidaló megoldásnál, ha a kiegészítő tábla (benne az egyedi *Sales* értékekkel) nincs láthatóvá téve. Egy, a *States* (államok) értékeket a teljes lakossággal és értékesített mennyiséggel együtt bemutató vizualizáció például az áthidaló megoldást leíró előző bekezdésben látotthoz hasonlóan, az alábbi ábrán látható módon jelenne meg.

![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_12.png)

A **több-a-többhöz** kapcsolatok ás a gyakoribb **több-az-egyhez** kapcsolatok közötti fő eltérések tehát a következők.

* A megjelenő értékek között nincs üres sor, amely a másik tábla párosítatlan sorainak felelne meg, sem azoknak, amelyekben a kapcsolatban használt oszlop Null értéket tartalmaz a másik táblában.
* A *RELATED()* függvény nem használható (mivel egynél több sor is kapcsolódhat)
* Az *ALL()* függvény használata egy táblán nem távolítja el a vele **több-a-többhöz** kapcsolatban álló más táblákra alkalmazott szűrőket. Az alábbi módon definiált mérték például nem távolítaná el az előző példában a kapcsolódó *CityData* tábla oszlopaira alkalmazott szűrőket:

    ![példaszkript](media/desktop-many-to-many-relationships/many-to-many-relationships_13.png)

    Emiatt a *State*, *Sales*, és *Sales total* értékeket feltüntető vizualizáció az alábbi eredményt mutatná:

    ![táblavizualizáció](media/desktop-many-to-many-relationships/many-to-many-relationships_14.png)

Éppen ezért nagy gonddal kell eljárni, hogy az *ALL(\<Tábla>)* függvényt használó számítások, amilyen a *végösszeg %-a*, a kívánt eredményt adják. 


## <a name="limitations-and-considerations"></a>Korlátozások és szempontok

A **több-a-többhöz kapcsolatoknak** és az **összetett modelleknek** erre a verziójára érvényes néhány korlátozás.

Az alábbi többdimenziós források nem használhatók **összetett modellekkel**:

* SAP HANA
* SAP Business Warehouse
* SQL Server Analysis Services
* Power BI-adathalmazok

Ha ezekhez a többdimenziós forrásokhoz a DirectQuery használatával csatlakozik, nem tud ugyanakkor más DirectQuery-forráshoz is csatlakozni, és importált adatokkal kombinálni sem.

A DirectQuery használatára jelenleg vonatkozó korlátozások a **több-a-többhöz kapcsolatok** használatára is érvényesek. Sok ilyen korlátozás jelenleg táblánként értendő, a tábla **tárolási módjától** függően. Egy importált tábla egy számított oszlopa például hivatkozhat más táblákra, egy DirectQuery-tábla számított oszlopai viszont továbbra is csak a táblán belüli oszlopokra hivatkozhatnak. Más korlátozások a modell egészére vonatkoznak, ha a modellen belül bármelyik tábla DirectQuery módban van. A **QuickInsights** és a **Q&A** funkciók például nem érhetők el a modellben, ha a táblák bármelyikének **tárolási módja** DirectQuery. 

## <a name="next-steps"></a>Következő lépések

Az alábbi cikkek bővebben ismertetik az összetett modelleket, és a DirectQuery részletes leírását is tartalmazzák.

* [Összetett modellek a Power BI Desktopban (előzetes verzió)](desktop-composite-models.md)
* [Tárolási mód a Power BI Desktopban (előzetes verzió)](desktop-storage-mode.md)

A DirectQuery-vel kapcsolatos cikkek:

* [DirectQuery használata a Power BI-ban](desktop-directquery-about.md)
* [A DirectQuery által támogatott adatforrások a Power BI-ban](desktop-directquery-data-sources.md)

