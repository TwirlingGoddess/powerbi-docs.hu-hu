---
title: "Jelentés használata Olvasó nézetben a Power BI-ban"
description: "Jelentés használata Olvasó nézetben a Power BI-ban"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/15/2017
ms.author: mihart
ms.openlocfilehash: 54de712e0743801b3e8c565ca997bbc56e254c69
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="interact-with-a-report-in-reading-view-in-power-bi"></a>Jelentés használata Olvasó nézetben a Power BI-ban
## <a name="reading-view"></a>Olvasó nézet
Az Olvasó nézet nem annyira interaktív, mint a [Szerkesztő nézet](service-interact-with-a-report-in-editing-view.md), azonban így is sok lehetőséget biztosít az adatok feltárására. Ezek akkor bizonyulnak hasznosnak, ha [megosztanak Önnel](service-share-dashboards.md) egy jelentést, ugyanis az csak Olvasó nézetben nyitható meg.

Az Olvasó nézetben nyugodtan kísérletezhet az adataival, és egy biztonságos környezetben tárhatja fel őket. Az Olvasó nézetben megadhat keresztkiemelést és keresztszűrést az oldal vizualizációin.  Egyszerűen csak emelje ki vagy válassza ki egy vizualizáció egy értékét, és a többi vizualizáción azonnal látni fogja ennek hatását. A Szűrők ablaktáblán új szűrőket adhat hozzá egy jelentésoldalhoz, vagy módosíthatja a meglévőket, illetve módosíthatja a vizualizációk értékeinek rendezését is. A megadott szűréseket vagy kiemeléseket nem menti a rendszer.

## <a name="cross-highlight-the-related-visualizations-on-a-page"></a>Kapcsolódó vizualizációk keresztkiemelése egy oldalon
Egy jelentésben az egy jelentésoldalon található vizualizációk mind „összeköttetésben” állnak.  Ez azt jelenti, hogy ha egy vizualizáción kijelöl egy vagy több értéket, akkor a többi olyan vizualizáció is megváltozik, amelyik használja a kijelölt értékeket.

![](media/service-interact-with-a-report-in-reading-view/pagefilter3b.gif)

> [!NOTE]
> Egy vizualizáció több elemét a CTRL billentyű nyomva tartásával jelölheti ki egyszerre.
> 
> 

## <a name="hover-over-visual-elements-to-see-the-details"></a>Vizualizáció részleteinek megjelenítése rámutatással
![](media/service-interact-with-a-report-in-reading-view/amarillachart.png)

## <a name="sort-the-data-in-a-visualization"></a>Adatok rendezése vizualizációkban
Válassza a három pontot (...), majd a **Rendezés szempontja:** lehetőséget. A legördülő menüben kiválaszthatja, hogy melyik mező alapján történjen a rendezés, az AZ ikon kiválasztásával pedig a növekvő vagy a csökkenő rendezés között válthat. 

![](media/service-interact-with-a-report-in-reading-view/pbi_changechartsort.gif) 

## <a name="interact-with-filters"></a>Szűrők használata
Ha egy jelentés készítője szűrőket adott hozzá a jelentés egy oldalához, akkor használhatja ezeket a szűrőket az Olvasó nézetben. A módosításokat nem menti a rendszer.

1. Válassza a jobb felső sarokban található Szűrők ikont.
   
   ![](media/service-interact-with-a-report-in-reading-view/filters.png)  
2. Ekkor láthatja, hogy milyen szűrők tartoznak a kijelölt vizualizációhoz (Látványelemszint szűrői), a jelentés egy teljes oldalához (Lapszintű szűrők), illetve az egész jelentéshez (Jelentési szint szűrői).
   
   ![](media/service-interact-with-a-report-in-reading-view/power-bi-reading-filters.png)
3. Helyezze a kurzort egy szűrő fölé, majd bontsa ki a lefelé mutató nyíl választásával.
   
   ![](media/service-interact-with-a-report-in-reading-view/power-bi-expan-filter.png)
4. Módosítsa a szűrőt, majd nézze meg, hogy ez milyen hatással van a vizualizációkra.  
   
   * Ebben a példában van egy lapszintű szűrőnk a **Chain** (Üzletlánc) elemre. Módosítsa a szűrőt **Lidseysről** **Fashions Directre**. Ezt úgy tudja megtenni, ha eltávolítja a pipát az egyik elől, és kipipálja a másikat.
     
     ![](media/service-interact-with-a-report-in-reading-view/power-bi-filter-chain.png)
   * De akár el is távolíthatja a **Chain** (Üzletlánc) teljes szűrőjét a radír ikon kiválasztásával ![](media/service-interact-with-a-report-in-reading-view/power-bi-eraser-icon.png) vagy mindkét üzletlánc kijelölésével.
   * Válassza ki a **District** (Körzet) lapszintű szűrőt, és váltson **Speciális szűrésre**. Szűrjön azokra a körzetekre, amelyek **FD**-vel kezdődnek és nem tartalmazzák a 4-es számot.
     
     ![](media/service-interact-with-a-report-in-reading-view/power-bi-advanced-filter.png)

További tudnivalókért tekintse meg a [Szűrő hozzáadása jelentéshez](power-bi-report-add-filter.md) és a [Szűrők és kiemelések jelentésekben](power-bi-reports-filters-and-highlighting.md) című cikkeket.

## <a name="zoom-in-on-individual-visuals"></a>Önálló vizualizáció nagyítása
Helyezze a kurzort egy vizualizáció fölé, majd válassza a **Fókusz mód** ikont ![](media/service-interact-with-a-report-in-reading-view/pbi_popouticon.jpg). Ha egy vizualizációt Fókusz módban jelenít meg, akkor az kitölti az egész jelentésvásznat, ahogyan az alábbi képen is látható.

![](media/service-interact-with-a-report-in-reading-view/powerbi-focus-mode.png)

Ha ugyanezt a vizualizációt a zavaró menüsávok, a szűrők ablaktábla vagy egyéb sötét színű elemek nélkül szeretné megjeleníteni, válassza a menüsáv tetején található **Teljes képernyő** ikont ![](media/service-interact-with-a-report-in-reading-view/power-bi-focus-icon.png) .

![](media/service-interact-with-a-report-in-reading-view/power-bi-full-screen.png)

További tudnivalókért tekintse meg a [Fókusz mód jelentésekhez](service-focus-mode.md) és a [Teljes képernyős mód jelentésekhez](service-fullscreen-mode.md) című cikkeket.

## <a name="adjust-the-display-dimensions"></a>Megjelenítés méreteinek módosítása
A jelentéseket több különböző eszközön is megtekintik, amelyek képernyőjének eltérő a mérete vagy a méretaránya.  Előfordulhat, hogy nem az alapértelmezett megjelenítést a megfelelő az eszközén.  A módosításhoz válassza a **Nézet** lehetőséget, majd válasszon az alábbi lehetőségek közül:

* Laphoz igazítás: a tartalmakat úgy méretezi, hogy a legjobban igazodjanak a laphoz.
* Szélességhez igazítás: a tartalmakat úgy méretezi, hogy a lap szélességéhez igazodjanak.
* Tényleges méret: a tartalmakat teljes méretükben jeleníti meg.  

![](media/service-interact-with-a-report-in-reading-view/power-bi-view.png)

  Olvasó nézetben a kiválasztott megjelenítési beállítás csak ideiglenes, a rendszer nem menti a jelentés bezárásakor.

  További tudnivalókért tekintse meg az [Oktatóanyag: megjelenítési beállítások módosítása jelentésekben](power-bi-change-report-display-settings.md) című cikket.

## <a name="next-steps"></a>Következő lépések
[Jelentések a Power BI-ban](service-reports.md)

[Szerkesztő nézet megnyitása](service-reading-view-and-editing-view.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

