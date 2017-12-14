---
title: "Nagy méretű számot tartalmazó csempe létrehozása Power BI-jelentésből"
description: "Nagy méretű számot tartalmazó csempe létrehozása Power BI-jelentésből"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 09/26/2017
ms.author: mihart
ms.openlocfilehash: 9f748ed1d3a34c6c6aceb14337bbb780598a15f9
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="create-a-big-number-tile-from-a-power-bi-report"></a>Nagy méretű számot tartalmazó csempe létrehozása Power BI-jelentésből
Néha egyetlen szám az a legfontosabb dolog, amelyet nyomon szeretne követni a Power BI-irányítópulton, például összes értékesítés, évenkénti piaci részesedés vagy összes lehetőség. Nagy számot tartalmazó csempét létrehozhat [kérdés feltevésével a Q&A mezőben](power-bi-visualization-big-number.md) vagy egy Power BI-jelentésben. Ez a cikk azt ismerteti, hogyan hozhat létre egyet egy jelentésben.

1. Hozzon létre egy [irányítópultot](service-dashboards.md), és [töltse be az adatokat](service-get-data.md).
   
   Ha gyakorláshoz szeretne adatokat, [töltse le a Kiskereskedelmi elemzés mintát](sample-retail-analysis.md). 
2. Nyissa meg a jelentést [Szerkesztés nézetben](service-reading-view-and-editing-view.md).
3. Keressen a jelentésben némi üres helyet tartalmazó lapot, vagy [adjon hozzá egy új lapot a jelentéshez](power-bi-report-add-page.md).
4. A Mezők listában válassza ki a megjeleníteni kívánt számmezőt.
   
   Ebben a példában ez az **Open Store count** (Nyitott boltok száma) a **Store** (Áruház) táblában. A Power BI létrehoz egy oszlopdiagramot ezzel az egy számmal.
   
   ![](media/power-bi-visualization-big-number-report/pbi_rptnumbertilechart.png)
5. A Megjelenítések ablaktáblán kattintson a Kártya ikonra.
   
   ![](media/power-bi-visualization-big-number-report/pbi_changechartcard.png)
6. Vigye az egérkurzort a kártyára, és kattintson a gombostű ikonra ![](media/power-bi-visualization-big-number-report/pbi_pintile.png) a csempe irányítópulthoz adásához. 
   
   ![](media/power-bi-visualization-big-number-report/power-bi-pin-icon.png)
7. Rögzítse a csempét egy meglévő vagy egy új irányítópultra. 
   
   * Meglévő irányítópult: válassza ki az irányítópult nevét a legördülő listából.
   * Új irányítópult: írja be az új irányítópult nevét.
8. Válassza a **Rögzítés** lehetőséget.
   
   Megjelenik egy üzenet (a jobb felső sarok közelében), amely értesíti, hogy sikeresen hozzáadta a vizualizációt az irányítópultjához csempeként.
   
   ![](media/power-bi-visualization-big-number-report/power-bi-pin-success-message.png)
9. Válassza az **Ugrás az irányítópultra** lehetőséget. Itt [szerkesztheti és áthelyezheti](service-dashboard-edit-tile.md) a rögzített vizualizációt.

## <a name="next-steps"></a>Következő lépések
[Irányítópult-csempék a Power BI-ban](service-dashboard-tiles.md)

[Irányítópultok a Power BI-ban](service-dashboards.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

