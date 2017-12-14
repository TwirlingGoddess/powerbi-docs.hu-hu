---
title: "I. rész – Vizualizációk hozzáadása Power BI-jelentésekhez (oktatóanyag)"
description: "Oktatóanyag: I. rész, Vizualizációk hozzáadása Power BI-jelentésekhez"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: IkJda4O7oGs
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: c8baa19eef8210a375e77acee379389ccd5dbade
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="part-i-add-visualizations-to-a-power-bi-report-tutorial"></a>I. rész – Vizualizációk hozzáadása Power BI-jelentésekhez (oktatóanyag)
A cikk röviden bemutatja a vizualizációk jelentésekben történő létrehozását.  Részletesebb útmutatásért [lásd a II. részt](power-bi-report-add-visualizations-ii.md). Amanda bemutatja, hogyan lehet különbözőképpen létrehozni, szerkeszteni és formázni a vizualizációkat a jelentésvásznon. Ezután Ön is megpróbálhatja létrehozni a saját jelentését a [Értékesítési és marketing minta](sample-datasets.md) segítségével.

<iframe width="560" height="315" src="https://www.youtube.com/embed/IkJda4O7oGs" frameborder="0" allowfullscreen></iframe>


## <a name="open-a-report-and-add-a-new-page"></a>Jelentés megnyitása és egy üres lap hozzáadása
1. Nyisson meg egy [jelentést Szerkesztési nézetben](service-reading-view-and-editing-view.md). Ez az oktatóanyag az [Értékesítési és marketing mintát](sample-datasets.md) használja.
2. Ha a Mezők panel nem látható, a nyíl ikonnal tudja megnyitni. 
   
   ![](media/power-bi-report-add-visualizations-i/pbi_nancy_fieldsfiltersarrow.png)
3. [Adjon hozzá egy üres lapot a jelentéshez](power-bi-report-add-page.md).

## <a name="add-visualizations-to-the-report"></a>Vizualizációk hozzáadása a jelentéshez
1. A vizualizáció létrehozásához válasszon egy mezőt a **Mezők** panelen.  
   
   **Ha egy numerikus mezővel kezdi**, mint az Értékesítés > Értékesítés $, a Power BI egy egy oszlopból álló oszlopdiagramot hoz létre.
   
   ![](media/power-bi-report-add-visualizations-i/pbi_onecolchart.png)
   
   **Ha egy kategóriamezővel kezdi**, mint a Név vagy a Termék, A Power BI egy táblát hoz létre, és hozzáadja az adott mezőt az **Értékek** területhez.
   
   ![](media/power-bi-report-add-visualizations-i/pbi_agif_createchart3.gif)
   
   **Ha egy földrajzi mezővel indít**, mint a Földrajz > Város, a Power BI a Bing Maps segítségével egy térképi vizualizációt hoz létre.
   
   ![](media/power-bi-report-add-visualizations-i/power-bi-map.png)
2. Hozzon létre egy vizualizációt, majd módosítsa a típusát. Jelölje ki a **Termék > Termékek száma** és a **Termék > Kategória** elemeket, és adja hozzá őket az **Értékek** területhez.
   
   ![](media/power-bi-report-add-visualizations-i/part1table1.png)
3. Az oszlopdiagram ikonra kattintva váltsa át a vizualizációt egy oszlopdiagramra.
   
   ![](media/power-bi-report-add-visualizations-i/part1converttocolumn.png)
4. Ha vizualizációkat hoz létre egy jelentésben, [rögzítheti őket az irányítópulton](service-dashboard-pin-tile-from-report.md). A vizualizáció rögzítéséhez kattintson a rajzszög ikonra ![](media/power-bi-report-add-visualizations-i/pinnooutline.png).
   
   ![](media/power-bi-report-add-visualizations-i/part1pin1.png)
5. Ezután:
   
   Továbbléphet a következőre: [2. rész: Vizualizációk hozzáadása Power BI-jelentésekhez](power-bi-report-add-visualizations-ii.md).
   
   [Használhatja a vizualizációkat](service-interact-with-a-report-in-reading-view.md) a jelentésben.
   
   [Még hatékonyabban használhatja a vizualizációkat](power-bi-report-visualizations.md).
   
   [Mentheti a jelentést](service-report-save.md).

## <a name="next-steps"></a>További lépések
További információk [a Power BI-jelentések vizualizációjáról](power-bi-report-visualizations.md).

[Power BI-jelentések](service-reports.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

