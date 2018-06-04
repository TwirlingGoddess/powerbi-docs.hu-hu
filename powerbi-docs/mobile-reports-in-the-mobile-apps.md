---
title: Jelentések vizsgálata a Power BI mobilalkalmazásokban
description: Tudja meg, hogyan tekintheti meg és használhatja Power BI mobilalkalmazásokban a jelentéseket a telefonján vagy a táblagépén. A jelentéseket a Power BI szolgáltatásban vagy a Power BI Desktopban hozza létre, majd használhatja azokat a mobilalkalmazásokban.
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-mobile
ms.topic: conceptual
ms.date: 03/22/2018
ms.author: maggies
ms.openlocfilehash: 6d7ab55c3ecbb13b40354f67263d597f0e1179f7
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34297676"
---
# <a name="explore-reports-in-the-power-bi-mobile-apps"></a>Jelentések vizsgálata a Power BI mobilalkalmazásokban
A következőkre vonatkozik:

| ![iPhone](media/mobile-reports-in-the-mobile-apps/ios-logo-40-px.png) | ![iPad](media/mobile-reports-in-the-mobile-apps/ios-logo-40-px.png) | ![Android rendszerű telefon](media/mobile-reports-in-the-mobile-apps/android-logo-40-px.png) | ![Android rendszerű táblagép](media/mobile-reports-in-the-mobile-apps/android-logo-40-px.png) | ![Windows 10-eszközök](media/mobile-reports-in-the-mobile-apps/win-10-logo-40-px.png) |
|:--- |:--- |:--- |:--- |:--- |
| iPhone-ok |iPadek |Android rendszerű telefonok |Android rendszerű táblagépek |Windows 10-eszközök |

A Power BI jelentés egy interaktív nézet az adatokról különböző, az adatokból származó eredményeket és elemzéseket bemutató vizualizációkkal. A jelentések megtekintése a Power BI mobilalkalmazásokban a harmadik lépés egy háromlépéses folyamatban.

1. [Jelentések létrehozása a Power BI Desktopban](desktop-report-view.md). A jelentéseket [optimalizálhatja is telefonra](mobile-apps-view-phone-report.md) a Power BI Desktopban. 
2. A jelentéseket tegye közzé a Power BI szolgáltatásban [(https://powerbi.com)](https://powerbi.com) vagy a [Power BI jelentéskészítő kiszolgálón](report-server/get-started.md).  
3. Ezután használhatja a jelentéseket a Power BI mobilalkalmazásokban.

## <a name="open-a-power-bi-report-in-the-mobile-app"></a>Power BI jelentések megnyitása a mobilalkalmazásban
A Power BI jelentéseket a rendszer a beszerzési helyük függvényében különböző helyeken tárolja a mobilalkalmazásban. Lehetnek az Alkalmazások, a Velem megosztva, a Munkaterületek (beleértve a Saját munkaterületet) területen vagy egy jelentéskészítő kiszolgálón. Néha át kell lépnie egy kapcsolódó irányítópultra egy jelentésért, néha pedig listázva vannak.

* Egy irányítópulton koppintson a három pont (...) ikonra a csempe jobb felső sarkában > válassza a **Jelentés megnyitása** lehetőséget.
  
  ![Jelentés megnyitása](media/mobile-reports-in-the-mobile-apps/power-bi-android-open-report-tile.png)
  
  Nem minden csempénél van lehetőség a jelentés megnyitására. Azok a csempék például, amelyek egy, a Q&A mezőben feltett kérdéssel jöttek létre, nem nyitnak meg jelentéseket a rájuk koppintáskor. 
  
  Telefonon a jelentés fekvő tájolásban jelenik meg, kivéve, ha [telefonos megtekintésre van optimalizálva](mobile-reports-in-the-mobile-apps.md#view-reports-optimized-for-phones).
  
  ![Jelentés telefonon fekvő tájolásban](media/mobile-reports-in-the-mobile-apps/power-bi-iphone-report-landscape.png)

## <a name="view-reports-optimized-for-phones"></a>Telefonra optimalizált jelentések megtekintése
A Power BI-jelentések szerzői létrehozhatnak kifejezetten a telefonokra optimalizált jelentéselrendezést. A telefonokra optimalizált jelentésoldalak további funkciókkal is rendelkeznek: többek között részletes elemzés végezhető, a vizualizációk rendezhetők, és elérhetők [azok a szűrők is, amelyeket a szerző adott hozzá a jelentésoldalhoz](mobile-apps-view-phone-report.md#filter-the-report-page-on-a-phone). A jelentés azokra a weben beállított értékekre szűrve jelenik meg a telefonon egy üzenettel, hogy az oldalon aktív szűrő működik. A szűrők a telefonon módosíthatók.

A jelentések listáján az optimalizált jelentésnek speciális ikonja van ![Telefonos jelentés ikon](media/mobile-reports-in-the-mobile-apps/power-bi-phone-report-icon.png):

![Telefonos jelentés megnyitása](media/mobile-reports-in-the-mobile-apps/power-bi-android-phone-report.png)

Az ilyen jelentések álló tájolásban nyílnak meg telefonon.

![Jelentés álló tájolásban](media/mobile-reports-in-the-mobile-apps/07-power-bi-phone-report-portrait.png)

 Egy jelentés állhat a telefonokra optimalizált és a telefonokra nem optimalizált oldalakból. Ha ez a helyzet, a jelentés végiglapozása során a nézet az egyes oldalaknál váltani fog a fekvő és az álló tájolás között.

További információ a [telefonos megtekintésre optimalizált jelentésekről](mobile-apps-view-phone-report.md).

## <a name="use-slicers-to-filter-a-report"></a>Szeletelők használta egy jelentés szűréséhez
Ha jelentéseket hoz létre a Power BI Desktopban vagy a Power BI szolgáltatásban, érdemes lehet [szeletelőket hozzáadni a jelentésoldalhoz](power-bi-visualization-slicers.md). A szeletelőkkel egyszerűen lehet szűrni az oldalt böngészőben és mobilalkalmazásban is. Ha telefonon jelenítik meg a jelentést, a szeletelőket a telefonra optimalizált fekvő és álló tájolással is lehet használni. A szeletelőkben vagy szűrőkben kijelölt értékek akkor is ki lesznek jelölve, amikor az oldalt a mobilalkalmazásban nyitja meg. Egy üzenet tájékoztat arról, hogy az oldalon aktív szűrés van érvényben.  

* Amikor kiválaszt egy értéket egy szeletelőben a jelentésoldalon, az szűri az oldalon lévő többi vizualizációt.
  
  ![Jelentésszeletelő](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-slicer.png)
  
  Ezen az ábrán a szeletelő az oszlopdiagramot szűri, hogy csak a júliusi értékeket jelenítse meg.

## <a name="cross-filter-and-highlight-a-report"></a>Keresztszűrés és kiemelés a jelentésekben
Amikor kiválaszt egy értéket egy vizualizációban, az más vizualizációkat nem szűr. Kiemeli a kapcsolódó értékeket a többi vizualizációban.

* Koppintson egy vizualizáció egy értékére.
  
  ![Oldal keresztszűrése](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-highlight.png)
  
  Ha a Nagy oszlopra koppint az egyik vizualizációban, a rendszer kiemeli a többi vizualizációban a kapcsolódó értékeket. 

## <a name="sort-a-visual-on-an-ipad-or-a-tablet"></a>Vizualizáció rendezése iPaden vagy táblagépen
* Koppintson a diagramra, koppintson a három pontra (**...**), és koppintson a mező nevére.
  
   ![Vizualizáció rendezése](media/mobile-reports-in-the-mobile-apps/power-bi-android-tablet-report-sort.png)
* A rendezés irányának megfordításához koppintson ismét a három pontra (**...**), és koppintson újra ugyanarra a mezőnévre.

## <a name="drill-down-on-an-ipad-or-a-tablet"></a>Részletezés iPaden vagy táblagépen
Ha egy jelentésszerző hozzáadta a részletezés funkciót a vizualizációhoz, iPaden vagy táblagépen részletezhet egy vizualizációban az annak egy részét felépítő adatokhoz. A [részletes elemzési képességet egy vizualizációhoz](power-bi-visualization-drill-down.md) a Power BI Desktopban vagy a Power BI szolgáltatásban adhatja hozzá. 

> [!NOTE]
> A részletes elemzés térképeken jelenleg nem működik iPaden és táblagépen.
> 
> 

* Koppintson egy vizualizációra. Ha szerepel felfelé és lefelé mutató nyíl a felső sarkokban ![Felhatolás és részletes elemzés ikonjai](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-up-down.png), akkor végezhet részletes elemzést. Ha részletes elemzést szeretne végezni egy értéken, koppintson a jobb felső sarokban lévő nyílra, majd koppintson egy értékre a vizualizációban – ebben az esetben a sötétkék FD-04 buborékra.
  
  ![Vizualizációk részletes elemzése](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-down-one.png)
* A visszahatoláshoz koppintson a felfelé mutató nyílra a bal felső sarokban.
  
  ![Felhatolás](media/mobile-reports-in-the-mobile-apps/power-bi-mobile-drill-up.png)

## <a name="go-back-to-my-workspace"></a>Visszatérés a Saját munkaterületre
* Koppintson a jelentés neve melletti nyílra > koppintson a **Saját munkaterület** elemre.
  
  ![Vissza felfelé](media/mobile-reports-in-the-mobile-apps/power-bi-iphone-report-back.png)

## <a name="next-steps"></a>Következő lépések
* [Telefonra optimalizált Power BI-jelentések megtekintése és használata](mobile-apps-view-phone-report.md)
* [Telefonra optimalizált verzió létrehozása egy jelentéshez](desktop-create-phone-report.md)
* Kérdése van? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

