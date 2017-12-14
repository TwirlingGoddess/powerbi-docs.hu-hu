---
title: "Perecdiagramok a Power BI szolgáltatásban (Oktatóanyag)"
description: "Oktatóanyag: Perecdiagramok a Power BI szolgáltatásban"
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
ms.date: 09/27/2017
ms.author: mihart
ms.openlocfilehash: 2f428095eb57c5358770f1d6d8572316d2b84c37
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="doughnut-charts-in-power-bi-tutorial"></a>Perecdiagramok a Power BI szolgáltatásban (Oktatóanyag)
A perecdiagram hasonlít a tortadiagramhoz, amennyiben a részek egészhez való viszonyát mutatja. Az egyetlen különbség az, hogy a középső rész üres, így helyet biztosít egy címkének vagy ikonnak.

## <a name="create-a-doughnut-chart"></a>Perecdiagram létrehozása
Hogy követni tudja a lépéseket, jelentkezzen be a Power BI szolgáltatásba, és válassza az **Adatok lekérése** \> **Minták** \> **Kiskereskedelmi elemzési minta** \> **Kapcsolódás** lehetőséget. 

1. Az irányítópulton nyissa meg a „Kiskereskedelmi elemzési minta” jelentést az **Összes áruház** csempe kiválasztásával.
2. Válassza a **Jelentés szerkesztése** a jelentés Szerkesztési nézetben való megnyitásához.
3. [Adjon hozzá új jelentésoldalt](power-bi-report-add-page.md).
4. Hozzon létre egy perecdiagramot, amely az ez évi értékesítést jeleníti meg kategória szerint.
   
   * A **Mezők** panelen válassza az **Értékesítés** \> **Előző évi értékesítések** lehetőséget.
   * Konvertálja perecdiagrammá. Ha az Előző évi értékesítések nem az **Értékek** területen vannak, húzza át ide.
     
       ![](media/power-bi-visualization-doughnut-charts/convertdonut.png)
   * Válassza az **Elem** \> **Kategória** lehetőséget, hogy hozzáadja az **Jelmagyarázat** területhez. 
     
       ![](media/power-bi-visualization-doughnut-charts/doughnuttutorial.png)

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
* A perecdiagram értékeinek összege 100%-nak kell lennie.
* A túl sok kategória megnehezíti az átlátást és az értelmezést.
* A perecdiagramok használhatók a legjobban, hogy egy részt az egészhez hasonlítsunk, kevésbé arra, hogy külön szakaszokat vessünk össze egymással. 

## <a name="next-steps"></a>További lépések
[Power BI-jelentések](service-reports.md)

[Vizualizációtípusok a Power BI-ban](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Vizualizációk a Power BI-jelentésekben](power-bi-report-visualizations.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

