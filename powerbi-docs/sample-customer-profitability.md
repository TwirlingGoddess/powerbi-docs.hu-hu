---
title: "Ügyfél-jövedelmezőségi minta a Power BI-hoz: bemutató"
description: "Ügyfél-jövedelmezőségi minta a Power BI-hoz: bemutató"
services: powerbi
documentationcenter: 
author: amandacofsky
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
ms.date: 10/29/2017
ms.author: mihart
ms.openlocfilehash: 9a100b7d13c11a8bd066b72a570f45d0c2bc08be
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="customer-profitability-sample-for-power-bi-take-a-tour"></a>Ügyfél-jövedelmezőségi minta a Power BI-hoz: bemutató
Az „Ügyfél-jövedelmezőségi minta” nevű csomag egy marketinganyagokat készítő céghez tartozó irányítópultot, jelentést és adatkészletet tartalmaz. Az irányítópult létrehozásával a pénzügyi vezető figyelni tudja az 5 üzleti egység kezelőjéhez (vezetőjéhez), a termékekhez, az ügyfelekhez és a bruttó árréshez tartozó fontosabb metrikákat. A pénzügyi vezető egyetlen pillantással láthatja, hogy mely tényezők vannak hatással a jövedelmezőségre.

Ez a minta egy olyan sorozat részét képezi, amely bemutatja, hogyan használhatja a Power BI-t üzleti adatokkal, jelentésekkel és irányítópultokkal. Az adatok az obviEnce-től ([www.obvience.com](http://www.obvience.com/)) származó valós, de anonimizált adatok.

Letöltheti [kizárólag a minta adatkészletét (Excel-munkafüzetét) is](http://go.microsoft.com/fwlink/?LinkId=529781).  
![](media/sample-customer-profitability/power-bi-dash.png)

## <a name="what-is-our-dashboard-telling-us"></a>Mi olvasható le az irányítópultról?
### <a name="company-wide-dashboard-tiles"></a>Vállalati szintű irányítópult-csempék
Ezek a csempék magas szintű, fontos vállalati metrikák megtekintését teszik lehetővé a pénzügyi vezetőnek.  Amint észrevesz valami érdekeset, a vezető az adott csempére kattintva le tud hatolni a mélyebb adatszintekre.

1. A cég bruttó árrése 42,5%.
2. 80 ügyfélről van szó.
3. 5 különböző termék értékesítése történik.
4. A legalacsonyabb százalékos, költségvetéshez viszonyított bevételvariancia februárban volt, míg a legmagasabb azt követően márciusban.
5. A bevétel nagy része a keleti és az északi régióból származik. A bruttó árrés soha nem haladta meg a költségvetést, bár az ER-0 és az MA-0 további vizsgálatot igényel.
6. Az évhez tartozó teljes bevétel megközelíti a költségvetést.

### <a name="manager-specific-dashboard-tiles"></a>Vezetőre vonatkozó irányítópult-csempék
Ezek a csempék a csapat mutatószámait mutatják. A pénzügyi vezetőnek követnie kell a régiós vezetők teljesítményét, és ezek a csempék teszik lehetővé számára a profit magas szintű áttekintését – a százalékos bruttó árrés használatával. Ha a százalékos bruttó árrés trendje váratlan értékeket mutat bármely vezetőhöz kapcsolódóan, a pénzügyi vezető alaposabb vizsgálatot végezhet.

Annelie százalékos bruttó árrése a legalacsonyabb, de folyamatos növekedés tapasztalható március óta. Valery százalékos bruttó árrése jelentősen csökken. Andrew pedig ingadozó értékeket produkált az évben. A vezetőkre vonatkozó csempékre kattintva lehet megnyitni a mögöttes jelentést. A jelentés 3 oldalból áll, és az „Iparági árrés elemzése” lapon nyílik meg.

## <a name="explore-the-pages-in-the-report"></a>A jelentés oldalainak feltárása
A jelentés 3 oldalból áll:

* A „Csapat mutatószámai” az 5 vezető teljesítményére és üzleti mutatóira fókuszál.
* Az „Iparági árrés elemzése” lehetőséget biztosít a jövedelmezőség elemzésére az egész iparág jelenlegi teljesítményéhez viszonyítva.
* A „Vezetők mutatószámai” az egyes vezetők teljesítményét mutatják a Cortanában való formázott megjelenítéshez.

### <a name="team-scorecard-page"></a>Csapat mutatószámai lap
![](media/sample-customer-profitability/customer2.png)

Nézzük meg két csapattag teljesítményét részletesen, és lássuk, mely adatokba kaphatunk betekintést. A bal oldali szeletelőn Andrew nevének kiválasztásával szűrheti a jelentésoldalt, így csak Andrew adatai jelennek meg.

* A KPI gyors ellenőrzésekor láthatja, hogy Andrew **bevételi állapota** zöld színű. Azaz Andrew jól teljesít.
* A „Százalékos, költségvetéshez viszonyított bevételvariancia hónap szerint” diagram azt mutatja, hogy a februári csökkenést leszámítva Andrew összességében jól teljesít. Domináns területe a keleti régió, 49 ügyfelet kezel, és 5 termékkel foglalkozik (a 7 termékből). A százalékos bruttó árrése nem a legmagasabb, de nem is a legkisebb.
* A „Teljes éves bevétel és a százalékos, költségvetéshez viszonyított bevételvariancia hónap szerint” diagram egyenletes profitot mutat. Azonban, ha az adatokat a **Középső** négyszögre kattintva szűrjük a regionális fatérképen, láthatjuk, hogy Andrew csak márciusban és csak Indianában termelt bevételt. Ez vajon szándékos, vagy alaposabb vizsgálatot igényel?

Most térjünk át Valeryre. A szeletelőn Valery nevének kiválasztásával szűrheti a jelentésoldalt, így csak Valery adatai jelennek meg.  
![](media/sample-customer-profitability/customer3.png)

* Vegye észre, hogy a **Teljes éves bevétel állapota** nevű KPI piros színű. Ez mindenképpen további vizsgálatot igényel.
* A bevételvariancia is aggasztó képet fest – Valery nem teljesíti a bevételi árrés követelményeit.
* Valery csak 9 ügyféllel rendelkezik, mindössze 2 terméket kezel, és szinte kizárólag északi ügyfelekkel foglalkozik. Ez a specializáció magyarázhatja a metrikákban tapasztalható túlzott ingadozást.
* Az **Észak** négyszög kiválasztásával a fatérképen látható, hogy Valery bruttó árrése az északi régióban összhangban van az általános árrésre vonatkozó teljesítménnyel.
* Az egyéb **régiós** négyszögeket kiválasztva érdekes történet bontakozik ki: a százalékos bruttó árrés 23% és 79% között ingadozik, és a bevételi számok az északi régiót kivéve rendkívül szezonálisak.

A feltárás folytatásával kideríthető, hogy Valery régiója miért is nem teljesít jól. Nézze meg a régiókat, a többi üzleti egységet, valamint a jelentés következő lapját – az „Iparági árrés elemzése” lapot.

### <a name="industry-margin-analysis"></a>Iparági árrés elemzése
Ez a jelentéslap az adatok egy másik szeletét mutatja meg. A teljes iparág bruttó árrését vizsgálja szegmens szerinti bontásban. A pénzügyi vezető ezt a lapot használva hasonlíthatja össze a cég és az üzleti egységek metrikáit az iparági metrikákkal, és mindez segít megmagyarázni a különböző trendeket és a jövedelmezőséget. Talán furcsa, hogy a csapat-specifikus „Bruttó árrés hónap és vezetőnév szerint” területi diagram szerepel ezen a lapon. Viszont lehetővé teszi a lap szűrését az üzleti egységek vezetői szerint.  
![](media/sample-customer-profitability/customer6.png)

Hogyan változik a jövedelmezőség az iparágban? Hogyan oszlanak meg a termékek és az ügyfelek iparági bontásban? Válasszon legalább egy iparágat a bal felső sarokban. (A fogyasztási cikkek iparágától kezdve) A szűrő törléséhez használja a radír ikont.

A buborékdiagramon a pénzügyi vezető a legnagyobb buborékokat keresheti meg, hiszen ezek befolyásolják a legnagyobb mértékben a bevételt. Ha a területi diagramon a vezetők nevére kattintva szűri a lapot, egyszerűen tekintheti meg az egyes vezetők teljesítményét iparági szegmens szerint.

* Andrew teljesítménye több különböző iparági szegmensben érzékelhető a jelentősen eltérő százalékos bruttó árrésnek (elsősorban a pozitív oldalon) és a százalékos varianciának köszönhetően. 
* Annelie diagramja hasonló, azzal a különbséggel, hogy ő csak pár iparági szegmensre koncentrál (a szövetségi szegmensre és a Gladius nevű termékre fókuszálva). 
* Carlos egyértelműen a szolgáltatási szegmensre koncentrál, és szép profitot termel. Nagy mértékben növelte a százalékos varianciát a high-tech szektorban, és egy számára új szegmensben (ipar) rendkívül jó teljesítményt ért el a költségvetéshez viszonyítva. 
* Tina több szegmensre koncentrál, és ő rendelkezik a legmagasabb százalékos bruttó árréssel, de a buborékok jellemzően kis mérete azt mutatja, hogy a cég profitjára gyakorolt hatása minimális. 
* Valery, aki csak egy termékért felel, mindössze 5 iparági szegmensre koncentrál. Az iparági befolyása szezonális, de mivel mindig nagy méretű buborékokat hoz létre, jelentős hatást gyakorol a cég profitjára. Magyarázható az iparággal a csökkenő teljesítmény?

### <a name="executive-scorecard"></a>Vezetők mutatószámai
Ez a lap Cortana-válaszkártya formátumú. További információ: [Cortana-válaszkártyák létrehozása](service-cortana-answer-cards.md)

## <a name="dig-into-the-data-by-asking-questions-with-qa"></a>Részletes adatfeltárás Q&A-kérdések feltevésével
Az elemzéshez hasznos lenne megállapítani, hogy mely iparág termeli a legtöbb bevételt Valerynek. Használjuk a Q&A-t.

1. A **Power BI** elem felső navigációs sávon való kiválasztásával térhet vissza az irányítópultra.
2. Válassza a Q&A kérdésmezőjét az irányítópult tetején.
   
    ![](media/sample-customer-profitability/customer4.png)
3. Írja be a következőt: **Valery teljes bevétele iparág szerint**. Figyelje meg, ahogy a vizualizáció frissül, miközben beírja a kérdést.
   
    ![](media/sample-customer-profitability/customer5.png)
   
   A forgalmazás képviseli Valery legnagyobb bevételi területét.

### <a name="dig-deeper-by-adding-filters"></a>Részletes feltárás szűrők hozzáadásával
Vessen egy pillantást a *Forgalmazás* iparágra.  

1. Térjen vissza az irányítópultra, és válassza ki a területdiagramot Andrew bruttó árrésének trendjével. Ekkor a jelentés az „Iparági árrés elemzése” lapon nyílik meg.
2. Anélkül, hogy bármilyen vizualizációt kijelölne a jelentéslapon, bontsa ki a jobb oldalon lévő Szűrő ablaktáblát. A Szűrők ablaktáblán csak lapszintű szűrők láthatók.  
   
   ![](media/sample-customer-profitability/power-bi-filters.png)
3. Keresse meg az **Iparág** szűrőt, és a nyíl kiválasztásával bontsa ki a listát. Adjon hozzá egy lapszűrőt a Forgalmazás iparághoz. Először törölje az összes kijelölést **Az összes kijelölése** jelölőnégyzet bejelölésének törlésével. Majd válassza a **Forgalmazás** elemet.  
   
   ![](media/sample-customer-profitability/customer7.png)
4. A „Bruttó árrés hónap és vezető neve szerint" területdiagramon az látható, hogy csak Valery és Tina rendelkezik ügyféllel ebben az iparágban, és csak Valery foglalkozott ezzel az iparággal júniustól novemberig.   
5. Válassza ki **Tina** és  **Valery** nevét a „Bruttó árrés hónap és vezető neve szerint" területdiagram jelmagyarázatában. Figyelje meg, hogy Tina teljesítménye a „Teljes bevétel termék szerint” diagram adatai alapján meglehetősen kicsi Valery teljesítményéhez képest. 
6. A tényleges bevétel megtekintéséhez térjen vissza az irányítópultra, és a Q&A használatával kérdezzen rá a következőre: **teljes forgalmi bevétel környezet és vezető szerint**.  
   
   ![](media/sample-customer-profitability/customer8.png)

Hasonlóan lehet megvizsgálni más iparágakat, és akár az ügyfelek vizualizációhoz való hozzáadásával is feltárhatók a Valery teljesítménye mögötti okok.

Ebben a környezetben nyugodtan kísérletezhet. Bármikor dönthet úgy, hogy nem menti a változtatásokat. De ha mégis mentené őket, bármikor lekérheti a minta egy új másolatát az **Adatok lekérése** lehetőséggel.

## <a name="next-steps-connect-to-your-data"></a>Következő lépések: Kapcsolódás a saját adatokhoz
Reméljük, hogy ez a bemutató segített megérteni a Power BI-irányítópultok, a Q&A és a jelentések segítségével történő ügyféladat-elemzést. Most Önön a sor – kapcsolódjon a saját adataihoz. A Power BI használatával számos különböző adatforráshoz kapcsolódhat. További információ a [Power BI használatának első lépéseiről](service-get-started.md).

[Vissza a Power BI-mintákhoz](sample-datasets.md)  

