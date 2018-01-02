---
title: "Alapszintű területdiagram (oktatóanyag)"
description: "Oktatóanyag: Alapszintű területdiagram."
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
ms.openlocfilehash: 42e068b11c22c32f1a6736a6ca8f9020594fb40a
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="basic-area-chart-tutorial"></a>Alapszintű területdiagram (oktatóanyag)
Az alapszintű területdiagram (más néven a rétegzett területdiagram) a vonaldiagramon alapul. A tengely és a vonal közötti terület a mennyiségek jelzése érdekében színnel van kitöltve. 

A területdiagramokon jól látható a változások nagysága időre vetítve, és a használatukkal hatékonyan mutatható meg a teljes érték egy trend mentén. Például a nyereség időbeli alakulását jelző adatok felrajzolhatóak területdiagramként, és így megmutatható a teljes nyereség.

![](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)

## <a name="when-to-use-a-basic-area-chart"></a>Mikor érdemes alapszintű területdiagramot használni?
Az alapszintű területdiagram remek választás a következőkhöz:

* az időre vetített mennyiségi trendek kimutatásához és összehasonlításához 
* a fizikailag megszámlálható halmazokat jelölő egyéni sorozatokhoz

## <a name="create-a-basic-area-chart"></a>Alapszintű területdiagram létrehozása
Hogy követni tudja a lépéseket, jelentkezzen be a Power BI-ba, és válassza az **Adatok lekérése\> Minták \> Kiskereskedelmi elemzési minta** lehetőséget. 

1. A „Kiskereskedelmi elemzési minta” irányítópulton nyissa meg a „Kiskereskedelmi elemzési minta” jelentést a **Total Stores** (Összes áruház) csempe kiválasztásával.
2. Válassza a **Jelentés szerkesztése** elemet a jelentés Szerkesztési nézetben való megnyitásához.
3. Adjon hozzá egy új jelentésoldalt.
4. Hozzon létre egy területdiagramot, amely az ez évi és az előző évi értékesítést jeleníti meg havi bontásban.
   
   a.  A **Mezők** panelen válassza a **Sales \> Last Year Sales** (Értékesítés > Előző évi értékesítés) és **This Year Sales > Value** (Idei értékesítés > Érték) lehetőségeket.
   
   b.  Konvertálja a diagramot egy alapszintű területdiagrammá.    
   ![](media/power-bi-visualization-basic-area-chart/convertchart.png)
   
   c.  Válassza az **Idő \> Hónap** lehetőséget, hogy ezzel hozzáadja a **Tengely** területhez.   
   ![](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)
   
   d.  A diagram havi bontásban való megjelenítéséhez kattintson a három pontra (...) a vizualizáció jobb felső sarkában, és válassza a **Rendezés hónapok szerint** lehetőséget.

## <a name="highlighting-and-cross-filtering"></a>Kiemelés és keresztszűrés
További információ a Szűrök ablaktábla használatáról: [Szűrők hozzáadása jelentésekhez](power-bi-report-add-filter.md).

Egy terület kiválasztásához kattintson az adott területbe vagy a felső vonalra.  Az alapszintű területdiagramok nem keresztszűrik a jelentésoldalon lévő többi vizualizációt. A területdiagramokat magukat azonban a jelentésoldalon lévő többi vizualizáció képes keresztszűrni.

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
* Az alapszintű területdiagramok az értékek összehasonlításához nem jól használhatóak, mivel a rétegzett területek kitakarják egymást. A Power BI átlátszósággal jelzi a területek fedését. Ez azonban csak két vagy három külön terület esetén működik. Ha háromnál több mérték trendjeit szeretné összehasonlítani, próbáljon inkább vonaldiagramokat alkalmazni. Ha háromnál több mérték mennyiségét szeretné összehasonlítani, próbáljon inkább faszerkezetes térképet alkalmazni.

## <a name="next-steps"></a>Következő lépések
[Power BI-jelentések](service-reports.md)  
[Vizualizációk a Power BI-jelentésekben](power-bi-report-visualizations.md)  
[Power BI – Alapfogalmak](service-basic-concepts.md)  
További kérdései vannak? [Forduljon a Power BI közösségéhez](http://community.powerbi.com/)

