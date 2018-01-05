---
title: "Adatelemzések automatikus generálása a Power BI-jal"
description: "Ismerje meg, hogyan kaphat elemzési információkat az adatkészletekről és az irányítópult-fájlokról."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: et_MLSL2sA8
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/06/2017
ms.author: mihart
ms.openlocfilehash: fb498f2b3320b96958467a9db851f119dba20ce7
ms.sourcegitcommit: 54da95f184dd0f7bb59bb0bc8775a1d93129b195
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2017
---
# <a name="automatically-generate-data-insights-with-power-bi"></a>Adatelemzések automatikus generálása a Power BI-jal
Van egy új adatkészlete, de nem tudja, hogy kezdje el feldolgozni?  Gyorsan létre kell hoznia egy irányítópultot?  Szeretne felfedezni eddig hiányzó összefüggéseket?

A Gyors elemzéseket futtatva érdekes interaktív vizualizációkat hozhat létre adataiból. Gyors elemzések egy teljes adatkészleten (gyors elemzések), illetve egy adott irányítópult-csempén is futtathatók (hatókörön belüli elemzés). Elemzésen is futtatható elemzés.

> **MEGJEGYZÉS:**: Az elemzés szolgáltatás csak a Power BI-ba feltöltött adatokhoz használható, DirectQueryvel előállított adatokhoz nem.
> 
> 

Az elemzés szolgáltatás a Microsoft Research-csel együttműködésben fejlesztett, egyre növekvő számú [haladó szintű elemzési algoritmusra épül](service-insight-types.md). A Microsoft Research egyre több ember számára teszi lehetővé adatai újszerű és intuitív módszerekkel történő elemzését.

## <a name="run-quick-insights-on-a-dataset"></a>Gyors elemzések futtatása adatkészleteken
Tekintse meg, hogyan futtat Amanda gyors elemzést egy adatkészleten, hogyan nyit meg egy elemzést Fókusz módban, hogyan tűzi ki egy ilyen elemzést irányítópultjára csempeként, és hogyan kér gyors elemzést egy irányítópult-csempéhez kapcsolódóan.

<iframe width="560" height="315" src="https://www.youtube.com/embed/et_MLSL2sA8" frameborder="0" allowfullscreen></iframe>


Most Ön következik. Fedezze fel az elemzések szolgáltatást a [Supplier Quality Analysis mintát](sample-supplier-quality.md) (Szállítói minőségelemzési mintát) használva.

1. Az **Adatkészletek** lapon kattintson a három pontra (...), majd válassza az **Elemzések lekérése** lehetőséget.
   
    ![](media/service-insights/power-bi-ellipses.png)
   
    ![](media/service-insights/power-bi-tab.png)
2. A Power BI [különböző algoritmusokat](service-insight-types.md) használ az adatkészlet trendjeinek kimutatásához.
   
    ![](media/service-insights/pbi_autoinsightssearching.png)
3. Az elemzés másodpercek alatt elkészül.  A vizualizációk megjelenítéséhez kattintson az **Elemzések megtekintése** lehetőségre.
   
    ![](media/service-insights/pbi_autoinsightsuccess.png)
   
   > **MEGJEGYZÉS:**: Bizonyos adatkészletek esetén nem hozható létre elemzés, mert az adatok statisztikailag nem szignifikánsak.  Ha ezzel kapcsolatban további információra van szüksége, tekintse át az [Adatok elemzésekhez történő optimalizálását](service-insights-optimize.md) bemutató cikket.
   > 
   > 
1. A vizualizációk a **Gyors elemzések** speciális vásznán jelennek meg, akár 32 különálló elemzéskártyán. Minden kártyán egy-egy diagram vagy ábra és egy rövid leírás látható.
   
    ![](media/service-insights/power-bi-insights.png)

## <a name="interact-with-the-insight-cards"></a>Az elemzéseket megjelenítő kártyák interaktív használata
  ![](media/service-insights/pbi_hover.png)

1. A vizualizáció irányítópultra történő felvételéhez vigye a kurzort az egyik kártya fölé, és válassza a kitűzés ikont.
2. Mutasson egy kártyára, válassza a három pontot (...), majd az **Elemzések megtekintése** elemet. Ekkor az elemzés megnyílik teljes képernyős módban.
   
    ![](media/service-insights/power-bi-insight-focus.png)
3. Fókusz módban a következő műveleteket végrehajtására van lehetőség:
   
   * Vizualizációk [szűrése](service-interact-with-a-report-in-reading-view.md).  A szűrők megjelenítéshez a jobb felső sarokban látható nyilat választva tudja kinyitni a Szűrők ablaktábláját.
     
        ![](media/service-insights/power-bi-insights-filter-new.png)
   * Az elemzéskártyát a kitűzés ![](media/service-insights/power-bi-pin-icon.png) ikont vagy a **Vizualizáció rögzítése** lehetőséget választva tűzheti ki egy irányítópultra.
   * Elemzést magára a kártyára vonatkozóan is futtathat. Ezt gyakran **hatókörön belüli elemzésnek** is nevezik. Válassza a jobb felső sarokban látható villanykörte ![](media/service-insights/power-bi-bulb-icon.png) ikont vagy az **Elemzések lekérése** lehetőséget.
     
       ![](media/service-insights/pbi-autoinsights-tile.png)
     
     A bal oldalon megjelennek az elemzések, a jobb oldalon pedig új kártyák láthatók, melyeket kizárólag az adott elemzésben szereplő adatok alapján készített a rendszer.
     
       ![](media/service-insights/power-bi-insights-on-insights-new.png)
4. Az eredeti elemzéseket tartalmazó vászonra a bal felső sarokban látható **Kilépés a fókusz módból** lehetőséget választva léphet vissza.

## <a name="run-insights-on-a-dashboard-tile"></a>Irányítópult csempére vonatkozó elemzések futtatása
Teljes adatkészletek összefüggéseinek feltárása helyett egyetlen irányítópult-csempe létrehozásához használt adatokra is szűkíthető az elemzés. Ezt is gyakran **hatókörön belüli elemzésnek** is nevezik.

1. Nyisson meg egy irányítópultot.
2. Vigye az egérmutatót egy csempe fölé. válassza a három pontot (...), majd az **Elemzések megtekintése** lehetőséget. A csempe [Fókusz módban](service-focus-mode.md) nyílik meg, és a jobb oldalán jelennek meg az elemzéskártyák.    
   
    ![](media/service-insights/pbi-insights-tile.png)    
4. Felkeltette valamelyik elemzés az érdeklődését? Az adott elemzéskártyát kiválasztva az adatok mélyebb szintjére is leáshat. A kiválasztott elemzés a bal oldalon fog megjelenni, az új, kizárólag az adott elemzés adatain alapuló új elemzéskártyák pedig a jobb oldalon.    
6. Az adatok mélyebb szintjeinek feltárását tovább folytatva az érdekes elemzéseket a jobb felső sarokban látható **Vizualizáció rögzítése** lehetőséget választva tűzheti ki az irányítópultra.

## <a name="next-steps"></a>Következő lépések
Ha Ön az adatkészlet tulajdonosa, akkor [optimalizálhatja azt gyors elemzések készítéséhez](service-insights-optimize.md)

További tudnivalók a [Gyors elemzések típusaival kapcsolatban](service-insight-types.md)

További kérdései vannak? [Felteheti azokat a Power BI-közösségnek](http://community.powerbi.com/)
