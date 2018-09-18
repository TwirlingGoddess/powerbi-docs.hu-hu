---
title: Egyszerű területdiagram
description: Egyszerű területdiagram.
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/27/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 83aacb2c3ecf95d8daecc8e9c79bd312cefd6d86
ms.sourcegitcommit: 67336b077668ab332e04fa670b0e9afd0a0c6489
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/12/2018
ms.locfileid: "44744429"
---
# <a name="basic-area-chart"></a>Egyszerű területdiagram
Az alapszintű területdiagram (más néven a rétegzett területdiagram) a vonaldiagramon alapul. A tengely és a vonal közötti terület a mennyiségek jelzése érdekében színnel van kitöltve. 

A területdiagramokon jól látható a változások nagysága időre vetítve, és a használatukkal hatékonyan mutatható meg a teljes érték egy trend mentén. Például a nyereség időbeli alakulását jelző adatok felrajzolhatóak területdiagramként, és így megmutatható a teljes nyereség.

![](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)

## <a name="when-to-use-a-basic-area-chart"></a>Mikor érdemes alapszintű területdiagramot használni?
Az alapszintű területdiagram remek választás a következőkhöz:

* az időre vetített mennyiségi trendek kimutatásához és összehasonlításához 
* a fizikailag megszámlálható halmazokat jelölő egyéni sorozatokhoz

### <a name="prerequisites"></a>Előfeltételek
 - Power BI szolgáltatás
 - Kiskereskedelmi elemzési minta

Hogy követni tudja a lépéseket, jelentkezzen be a Power BI szolgáltatásba, és válassza az **Adatok lekérése \> Minták \> Kiskereskedelmi elemzési minta > Kapcsolódás** lehetőséget, majd válassza az **Ugrás az irányítópultra** lehetőséget. 

## <a name="create-a-basic-area-chart"></a>Alapszintű területdiagram létrehozása
 

1. A „Kiskereskedelmi elemzési minta” irányítópulton nyissa meg a „Kiskereskedelmi elemzési minta” jelentést a **Total Stores** (Összes áruház) csempe kiválasztásával.
2. Válassza a **Jelentés szerkesztése** elemet a jelentés Szerkesztési nézetben való megnyitásához.
3. A jelentés aljánál lévő sárga plusz (+) ikont választva adhat hozzá egy új jelentésoldalt.
4. Hozzon létre egy területdiagramot, amely az ez évi és az előző évi értékesítést jeleníti meg havi bontásban.
   
   a. A MEZŐK panelen válassza a **Sales \> Last Year Sales** (Értékesítés > Előző évi értékesítés) és **This Year Sales > Value** (Idei értékesítés > Érték) lehetőségeket.

   ![](media/power-bi-visualization-basic-area-chart/power-bi-bar-chart.png)

   b.  Konvertálja a diagramot egy alapszintű területdiagrammá, ehhez válassza a MEGJELENÍTÉSEK ablaktáblán a Területdiagram ikont.

   ![](media/power-bi-visualization-basic-area-chart/convertchart.png)
   
   c.  Válassza az **Idő \> Hónap** lehetőséget, hogy ezzel hozzáadja a **Tengely** területhez.   
   ![](media/power-bi-visualization-basic-area-chart/powerbi-area-chartnew.png)
   
   d.  A diagram havi bontásban való megjelenítéséhez kattintson a három pontra (...) a vizualizáció jobb felső sarkában, és válassza a **Rendezés hónapok szerint** lehetőséget.

## <a name="highlighting-and-cross-filtering"></a>Kiemelés és keresztszűrés
További információ a SZŰRÖK panel használatáról: [Szűrők hozzáadása jelentésekhez](../power-bi-report-add-filter.md).

A diagram egy meghatározott területét a terület felső szegélyének kiválasztásával jelölheti ki.  Más típusú vizualizációktól eltérően az alapszintű területdiagram kiválasztásakor nem történik keresztszűrés ugyanannak a jelentésoldalnak a többi vizualizációjával (ha vannak ilyenek). A területdiagramokat magukat azonban a jelentésoldalon lévő többi vizualizáció képes keresztszűrni. További információt a [Vizualizációk interakciói a jelentésekben](../service-reports-visual-interactions.md) című témakörben talál


## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás   
* [Jelentés nevének akadálymentesítése a fogyatékkal élők számára](../desktop-accessibility.md)
* Az alapszintű területdiagramok az értékek összehasonlításához nem jól használhatóak, mivel a rétegzett területek kitakarják egymást. A Power BI átlátszósággal jelzi a területek fedését. Ez azonban csak két vagy három külön terület esetén működik. Ha háromnál több mérték trendjeit szeretné összehasonlítani, próbáljon inkább vonaldiagramokat alkalmazni. Ha háromnál több mérték mennyiségét szeretné összehasonlítani, próbáljon inkább faszerkezetes térképet alkalmazni.

## <a name="next-steps"></a>Következő lépések
[Power BI-jelentések](../service-reports.md)  
[Vizualizációk a Power BI-jelentésekben](power-bi-report-visualizations.md)  
[Power BI – Alapfogalmak](../service-basic-concepts.md)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

