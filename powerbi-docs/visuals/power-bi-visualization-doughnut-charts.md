---
title: Perecdiagramok a Power BI szolgáltatásban
description: Perecdiagramok a Power BI szolgáltatásban
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 12/23/2017
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 3bf0aa516f50d363b53d2ed91b86d999e7855c30
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/21/2018
ms.locfileid: "46545022"
---
# <a name="doughnut-charts-in-power-bi"></a>Perecdiagramok a Power BI szolgáltatásban
A perecdiagram hasonlít a tortadiagramhoz, amennyiben a részek egészhez való viszonyát mutatja. Az egyetlen különbség az, hogy a középső rész üres, így helyet biztosít egy címkének vagy ikonnak.

## <a name="create-a-doughnut-chart"></a>Perecdiagram létrehozása
Ezen útmutatás a Kiskereskedelmi elemzési mintát használja egy olyan perecdiagram létrehozásához, mely az ez évi értékesítést jeleníti meg kategória szerint. Annak érdekében, hogy követni tudja a lépéseket, [töltse le a mintát](../sample-datasets.md), mely a Power BI szolgáltatásban (az app.powerbi.com webhelyen) vagy a Power BI Desktopban használható.

1. Kezdjen egy [üres jelentésoldalon](../power-bi-report-add-page.md), és válassza a **SalesStage** \> **Sales Stage** (Értékesítési fázis) mezőt. Ha a Power BI szolgáltatást használja, mindenképpen a [Szerkesztési nézetében](../service-interact-with-a-report-in-editing-view.md) nyissa meg a jelentést.

2. A Mezők panelen válassza a **Sales** \> **Last Year Sales** (Értékesítés > Előző évi értékesítés) lehetőséget.  
   
3. A Megjelenítések ablaktáblán válassza a perecdiagram ikonját ![perecdiagram ikonja]() az oszlopdiagram perecdiagrammá alakításához. Ha a **Last Year Sales** (Előző évi értékesítés) nem az **Értékek** területen található, húzza át oda.
     
   ![](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-chart.png)

4. Válassza az **Elem** \> **Kategória** lehetőséget, hogy hozzáadja az **Jelmagyarázat** területhez. 
     
    ![](media/power-bi-visualization-doughnut-charts/power-bi-doughnut-done.png)

5. Ha szeretné, [módosíthatja a diagram szövegének méretét és színét](power-bi-visualization-customize-title-background-and-legend.md). 

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
* A perecdiagram értékeinek összege 100%-nak kell lennie.
* A túl sok kategória megnehezíti az átlátást és az értelmezést.
* A perecdiagramok használhatók a legjobban, hogy egy részt az egészhez hasonlítsunk, kevésbé arra, hogy külön szakaszokat vessünk össze egymással. 

## <a name="next-steps"></a>További lépések
[Power BI-jelentések](../consumer/end-user-reports.md)

[Vizualizációtípusok a Power BI-ban](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Vizualizációk a Power BI-jelentésekben](power-bi-report-visualizations.md)

[Power BI – Alapfogalmak](../consumer/end-user-basic-concepts.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

