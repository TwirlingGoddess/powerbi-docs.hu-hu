---
title: Táblázatos vizualizációk a Power BI-jelentésekben és -irányítópultokon
description: 'Oktatóanyag: Tippek a táblázatos vizualizációk használatához a Power BI-jelentésekben és -irányítópultokon, beleértve az oszlopszélességek átméretezését.'
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/27/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 8c2ec6a93b41fd097bc5097a6e3921505d975a3c
ms.sourcegitcommit: 67336b077668ab332e04fa670b0e9afd0a0c6489
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/12/2018
ms.locfileid: "44744483"
---
# <a name="working-with-tables-in-power-bi-reports-and-dashboards"></a>Táblák használata a Power BI-jelentésekben és -irányítópultokon
A táblák olyan táblázatok, amelyek sorok és oszlopok logikai sorozataként jelenítik meg a kapcsolódó adatokat. Tartalmazhatnak fejléceket és összesítősorokat is. A táblák jól használhatók mennyiségi összehasonlításokhoz, ahol több, egy kategóriába tartozó érték vizsgálható egyszerre. Ez a tábla például a **Kategória** 5 különböző mértékét jeleníti meg.

![](media/power-bi-visualization-tables/table.png)

## <a name="when-to-use-a-table"></a>Mikor érdemes táblát használni?
A tábla remek választás a következő esetekben:

* részletes adatok és pontos értékek megtekintéséhez és összehasonlításához (vizualizációk helyett)
* az adatok táblázatos formában való megjelenítéséhez
* numerikus adatok kategóriák szerinti megjelenítéséhez   

> [!NOTE]
> Ha a tábla túl sok értéket tartalmaz, érdemes lehet mátrixszá alakítani és/vagy lefúrást alkalmazni.

## <a name="prerequisites"></a>Előfeltételek
- Power BI szolgáltatás vagy Power BI Desktop
- Kiskereskedelmi elemzési minta

## <a name="create-a-table"></a>Tábla létrehozása
Létrehozzuk a fenti ábrát az értékesítési adatok elemkategória szerinti megjelenítéséhez. Hogy követni tudja a lépéseket, jelentkezzen be a Power BI szolgáltatásba, és válassza az **Adatok lekérése \> Minták \> Kiskereskedelmi elemzési minta > Kapcsolódás** lehetőséget, majd válassza az **Ugrás az irányítópultra lehetőséget. A vizualizációk létrehozásához az adatkészletre és a jelentésre vonatkozó szerkesztési jogosultságok szükségesek. A Power BI mintái mind szerkeszthetőek. Ha a jelentést megosztották Önnel, akkor nem fog tudni vizualizációkat létrehozni a jelentésben.

1. A bal oldali navigációs panelen válassza a **Munkaterületek > Saját munkaterület** lehetőséget.    
2. Válassza az Adatkészletek lapot, és görgessen le az imént hozzáadott Kiskereskedelmi elemzés minta adatkészletig.  Válassza a **Jelentés létrehozása** ikont.

    ![](media/power-bi-visualization-tables/power-bi-create-report.png)
2. A jelentésszerkesztőben válassza az **Elem** > **Kategória** lehetőséget.  A Power BI automatikusan létrehoz egy táblát, amely az összes kategóriát felsorolja.

    ![](media/power-bi-visualization-tables/power-bi-table1.png)
3. Jelölje ki a **Sales > Average Unit Price** (Értékesítés > Átlagos egységár), a **Sales > Last Year Sales** (Értékesítés > Tavalyi értékesítések) és a **Sales > This Year Sales** (Értékesítés > Idei értékesítések) elemet, és válassza ki mind a 3 beállítást (Érték, Cél, Állapot).   
4. A Vizualizációk ablaktáblán húzza az értékeket az **Értékek** területre, amíg a tábla oszlopainak rendje meg nem egyezik az oldalon fentebb látható első ábrával.  Az Értékek területnek így kell kinéznie.

    ![](media/power-bi-visualization-tables/power-bi-table2.png)
5. Rögzítse a táblát az irányítópultra a rajzszög ikonnal  

     ![](media/power-bi-visualization-tables/pbi_pintile.png)

## <a name="format-the-table"></a>A táblázat formázása
A táblák sokféleképpen formázhatók, és itt csak néhányat mutatunk be ezek közül. A többi formázási lehetőség megismeréséhez nyissa meg és fedezze fel a Formázás ablaktáblát (festőhenger ikon ![](media/power-bi-visualization-tables/power-bi-format.png)).

* Próbálja ki a tábla formázását. Itt hozzáadtunk egy függőleges kék rácsot, növeltük a sorok közötti távolságot, és egy kicsivel növeltük a külső szegélyek és a szöveg méretét is.

    ![](media/power-bi-visualization-tables/power-bi-table-gridnew.png)

    ![](media/power-bi-visualization-tables/power-bi-table-grid3.png)
* Az oszlopok fejléceiben módosítottuk a háttérszínt, hozzáadtunk egy körvonalat, és növeltük a betűméretet. 

    ![](media/power-bi-visualization-tables/power-bi-table-column-headers.png)


~~~
![](media/power-bi-visualization-tables/power-bi-table-column2.png)
~~~

* Még az egyes oszlopokra és oszlopfejlécekre is alkalmazhat formázást. Kezdje a **Mezőformázás** kibontásával, majd jelölje ki az oszlopot a formázáshoz a legördülő menüben. Az oszlopértékektől függően a Mezőformázás lehetővé teszi a következők beállítását: megjelenítési egységek, betűszín, tizedesjegyek száma, háttér, igazítás stb. Miután módosította a beállításokat, döntse el, hogy alkalmazza-e ezeket a fejlécre és az összesítési sorra is.

    ![](media/power-bi-visualization-tables/power-bi-field-formatting.png)

* Egyéb formázást is végrehajtottunk, mire megkaptuk ezt a végleges táblát. Mivel rengeteg formázási lehetőség létezik, a tanuláshoz a legjobb, ha az alapértelmezett formázással indít, megnyitja a Formázás ablaktáblát ![](media/power-bi-visualization-tables/power-bi-format.png), és kísérletez. 

    ![](media/power-bi-visualization-tables/power-bi-table-format.png)

### <a name="conditional-formatting"></a>Feltételes formázás
A formázás egyik típusa a *feltételes formázás*, amely a Power BI szolgáltatásban vagy a Power BI Desktopban a **Vizualizációk** ablaktábla **Értékek** területén alkalmazható a mezőkre. 

A táblák feltételes formázásával a cellák értéke alapján határozhat meg egyéni háttér- vagy betűszínt (akár színátmeneteket is) a cellákhoz. 

1. A Power BI szolgáltatás vagy Power BI Desktop **Vizualizációk** ablaktábláján kattintson az **Értékek** területen a formázni kívánt érték mellett a lefele mutató nyílra (vagy kattintson a jobb gombbal a mezőre). A mezők feltételes formázása kizárólag az **Értékek** terület **Mezők** szakaszában kezelhető.

    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-background.png)
2. Válassza a **Háttérszínek színskálái** elemet. A megjelenő párbeszédpanelen beállíthatja a színt, valamint a *Minimum* és *Maximum* értékeket. A **Széttartó** jelölőnégyzet bejelölése esetén megadhat egy választható *Középértéket* is.

    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-background2.png)

    Most alkalmazzunk feltételes formázást az Average Unit Price (Átlagos egységár) értékekre. Válassza a **Széttartó** lehetőséget, adjon hozzá színeket, és kattintson az **OK** gombra. 

    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-data-background.png)
3. Vegyen fel egy pozitív és negatív értékeket is tartalmazó új mezőt a táblába.  Válassza az **Sales > Total Sales Variance** (Értékesítés > Teljes értékesítés szórása) lehetőséget. 

    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting2.png)
4. Adjon hozzá feltételes adatsávformázást – ehhez válassza a lefelé mutató nyilat a **Total Sales Variance** (Teljes értékesítés szórása) mellett, majd a **Feltételes formázás > Adatsávok** lehetőséget.

    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-data-bars.png)
5. A megjelenő párbeszédpanelen állítsa be a **Pozitív sáv** és a **Negatív sáv** színeit, jelölje be a **Csak sávok megjelenítése** lehetőséget, és végezze el a többi kívánt módosítást.

    ![](media/power-bi-visualization-tables/power-bi-data-bars.png)

    Az **OK** gombra kattintva a numerikus értékek helyét adatsávok veszik át a táblában, így könnyebben áttekinthető lesz.

    ![](media/power-bi-visualization-tables/power-bi-conditional-formatting-data-bars2.png)
6. A vizualizációk feltételes formázásának törléséhez egyszerűen kattintson újra a mezőre a jobb gombbal, és válassza a **Feltételes formázás eltávolítása** lehetőséget.

> [!TIP]
> A feltételes formázás a Formázás ablaktábláról is elérhető (festőhenger ikon). Válassza ki a formázni kívánt értéket, és az alapértelmezett beállítások alkalmazásához állítsa a **Színskálák** vagy az **Adatsávok** beállítást Be értékre, vagy a beállítások testreszabásához válassza a **Speciális vezérlők** lehetőséget.
> 
> 

## <a name="adjust-the-column-width-of-a-table"></a>Tábla oszlopszélességeinek állítása
Előfordul, hogy a Power BI csonkolja az oszlopfejléceket a jelentésekben vagy az irányítópultokon. Az oszlop teljes nevének megjelenítéséhez vigye a kurzort a fejléc jobb oldalára, amíg meg nem jelenik a dupla nyíl, majd válassza ki és húzza el oldalra a nyilakat.

![](media/power-bi-visualization-tables/resizetable.gif)

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
* Oszlopformázás alkalmazásakor oszloponként választhat igazítási beállítást a következők közül: Automatikus, Balra, Középre vagy Jobbra. Az oszlopok általában csak szöveget vagy csak számokat tartalmaznak, nem pedig azok keverékét. Azokban az esetekben viszont, amelyekben egy oszlop számokat és szöveget is tartalmaz, az **Automatikus** beállítás szöveg esetén balra, számok esetén pedig jobbra fog igazítani. Ez a működés azokat a nyelveket támogatja, melyeket balról jobbra kell olvasni.   

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

