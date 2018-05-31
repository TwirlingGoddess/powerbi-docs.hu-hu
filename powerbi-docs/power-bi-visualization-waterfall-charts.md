---
title: Vízesésdiagramok a Power BI-ban
description: Vízesésdiagramok a Power BI-ban
services: powerbi
documentationcenter: ''
author: mihart
manager: kfile
backup: ''
editor: ''
tags: ''
featuredvideoid: maTzOJSRB3g
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/20/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 101680bd353237af61a885155acd2fcd66a35404
ms.sourcegitcommit: 493f160d04ed411ff4741c599adc63ba1f65230f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/07/2018
ms.locfileid: "33812610"
---
# <a name="waterfall-charts-in-power-bi"></a>Vízesésdiagramok a Power BI-ban
A vízesésdiagramok göngyölített összeget jelenítenek meg az értékek összeadásakor vagy kivonásakor. Ez hasznos annak megértéséhez, hogy egy kezdeti értékre (pl. nettó bevétel) hogyan hat egy sornyi pozitív és negatív változás.

Az oszlopok színkódolással rendelkeznek, így gyorsan megállapíthatja az értékek növekedését és csökkenését. A kezdeti és végértékeket tartalmazó oszlopok gyakran [a vízszintes tengelyről indulnak](https://support.office.com/article/Create-a-waterfall-chart-in-Office-2016-for-Windows-8de1ece4-ff21-4d37-acd7-546f5527f185#BKMK_Float "a vízszintes tengelyről indulnak"), míg a középső értékek lebegő oszlopokat képeznek. Emiatt a megjelenés miatt a vízesésdiagramokat híddiagramoknak is nevezik.

<iframe width="560" height="315" src="https://www.youtube.com/embed/qKRZPBnaUXM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## <a name="when-to-use-a-waterfall-chart"></a>Mikor érdemes vízesésdiagramot használni?
A vízesésdiagram remek választás a következőkhöz:

* ha a mérték az idősorok vagy különböző kategóriák között is változik;
* ha naplózni kívánja az összértéket befolyásoló főbb változásokat;
* ha a vállalat éves profitját szeretné ábrázolni különféle bevételi források megjelenítésével, majd az összbevétel (vagy veszteség) kiemelésével;
* ha a vállalat alkalmazottainak számát szeretné ábrázolni az év eleji és év végi értékekkel;
* ha szeretné megjeleníteni, hogy mennyi pénzt keresett és költött az egyes hónapok során, valamint a fiók folyóegyenlegét. 

## <a name="create-a-waterfall-chart"></a>Vízesésdiagram létrehozása
Olyan vízesésdiagramot hozunk létre, amely megjeleníti a havi értékesítési eltérést (a becsült és a tényleges értékek közötti különbséget). Hogy követni tudja a lépéseket, jelentkezzen be a Power BI-ba, és válassza az **Adatok lekérése\> Minták \> Kiskereskedelmi elemzési minta** lehetőséget. 

1. Válassza az **Adatkészletek** lapot, és görgessen le az új „Kiskereskedelmi elemzés minta” adatkészletig.  A **Jelentés létrehozása** ikon kiválasztásával nyissa meg az adatkészletet jelentéskészítési nézetben. 
   
    ![](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-report.png)
2. A **Mezők** panelen válassza az **Értékesítés \> Teljes értékesítési eltérés** lehetőséget. Ha a **Teljes értékesítési eltérés** nem az **Y tengely** területén található, húzza át oda.
3. Konvertálja a diagramot **Vízesésdiagrammá**. 
   
    ![](media/power-bi-visualization-waterfall-charts/convertwaterfall.png)
4. Válassza az **Idő**  \> **FiscalMonth** (Pénzügyi hónap) lehetőséget, és adja hozzá a **Kategória** területhez. 
   
    ![](media/power-bi-visualization-waterfall-charts/power-bi-waterfall.png)
5. Rendezze időrend szerint a vízesésdiagramot. A diagram jobb felső sarkában kattintson a három pontra (...), és válassza a **FiscalMonth** lehetőséget.
   
    ![](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-sort.png)
   
    ![](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-sorted.png)
6. Derítse ki részletesebben, hogy mi járul hozzá legnagyobb mértékben az egyes hónapok közötti változáshoz. Húzza a **Tároló** > **Terület** elemet a **Lebontás** gyűjtőbe.
   
    ![](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-breakdown.png)
7. A Power BI alapértelmezés szerint a havi növekedésekhez és csökkenésekhez hozzájáruló 5 fő tényezőt adja hozzá. Minket azonban csak az első 2 tényező érdekel.  A Formázás panelen válassza a **Lebontás** lehetőséget, és a **Maximum** beállítást állítsa 2 értékre.
   
    ![](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-breakdown-maximum.png)
   
    A vízesésdiagram gyors áttekintéséből kiderül, hogy Ohio és Pennsylvania területek járulnak hozzá a változáshoz a legnagyobb (negatív és pozitív) mértékben. 
   
    ![](media/power-bi-visualization-waterfall-charts/power-bi-waterfall-axis.png)
8. Ez érdekes eredmény. Vajon azért van Ohio és Pennsylvania ilyen jelentős befolyással, mert ezen a két területen jóval több az értékesítés, mint a többin?  Ezt könnyedén ellenőrizhetjük. Hozzon létre egy térképet az értékesítések terület szerinti megjelenítéséhez.  
   
    ![](media/power-bi-visualization-waterfall-charts/power-bi-map.png)
   
    Az elkészült térkép alátámasztja ezt az elméletet.  Látható, hogy ezen a 2 területen volt a legmagasabb az értékesítés a tavalyi (buborék mérete) és az idei évben (buborék árnyékolása).

## <a name="highlighting-and-cross-filtering"></a>Kiemelés és keresztszűrés
További információ a Szűrök ablaktábla használatáról: [Szűrők hozzáadása jelentésekhez](power-bi-report-add-filter.md).

A vízesésdiagram egyes oszlopainak kiemelésével a rendszer keresztszűri a jelentésoldalon lévő többi vizualizációt... és viszont. Azonban az Összesen oszlop nem aktivál kiemelést, és nem reagál a keresztszűrésre.

## <a name="next-steps"></a>Következő lépések
[Power BI-jelentések](service-reports.md)

[Vizualizációtípusok a Power BI-ban](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Vizualizációk a Power BI-jelentésekben](power-bi-report-visualizations.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

