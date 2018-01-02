---
title: "Gyors elemzések lekérése a Power BI-ban"
description: "Gyors elemzések készítése és használata a Power BI szolgáltatással ‒ dokumentáció."
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
ms.date: 09/01/2017
ms.author: mihart
ms.openlocfilehash: 8b069f29737992817d20396007864cc8c005ca99
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="quick-insights-with-power-bi"></a>Gyors elemzések a Power BI-jal
Van egy új adatkészlete, de nem tudja, hogy kezdje el feldolgozni?  Gyorsan létre kell hoznia egy irányítópultot?  Rövid időn belül szeretne felfedezni eddig hiányzó összefüggéseket?

A Gyors elemzéseket futtatva érdekes interaktív vizualizációkat hozhat létre adataiból. Gyors elemzések egy teljes adatkészleten (Gyors elemzések), illetve egy adott irányítópult-csempén is futtathatók (Hatókörön belüli elemzés). Elemzésen is futtatható Gyors elemzés.

> **MEGJEGYZÉS:**: A Gyors elemzés szolgáltatás csak a Power BI-ba feltöltött adatokhoz használható, DirectQueryvel előállított adatokhoz nem.
> 
> 

A Gyors elemzés szolgáltatás a Microsoft Research-csel együttműködésben fejlesztett, egyre növekvő számú [haladó szintű elemzési algoritmusra épül](service-insight-types.md). A Microsoft Research egyre több ember számára teszi lehetővé adatai újszerű és intuitív módszerekkel történő elemzését.

## <a name="run-quick-insights-on-a-dataset"></a>Gyors elemzések futtatása adatkészleteken
Tekintse meg, hogyan futtat Amanda gyors elemzést egy adatkészleten, hogyan nyit meg egy elemzést Fókusz módban, hogyan tűzi ki egy ilyen elemzést irányítópultjára csempeként, és hogyan kér gyors elemzést egy vizualizációs elemhez kapcsolódóan.

<iframe width="560" height="315" src="https://www.youtube.com/embed/et_MLSL2sA8" frameborder="0" allowfullscreen></iframe>


Most Ön következik. Fedezze fel a Gyors elemzések szolgáltatást a [Supplier Quality Analysis mintát](sample-supplier-quality.md) (Szállítói minőségelemzési mintát) használva.

1. Az **Adatkészletek** lapon kattintson a három pontra (...), majd válassza az **Elemzések lekérése** lehetőséget.
   
    ![](media/service-insights/power-bi-ellipses.png)
   
    ![](media/service-insights/power-bi-tab.png)
2. A Power BI [különböző algoritmusokat](service-insight-types.md) használ az adatkészlet trendjeinek kimutatásához.
   
    ![](media/service-insights/pbi_autoinsightssearching.png)
3. Az elemzés másodpercek alatt elkészül.  A vizualizációk megjelenítéséhez kattintson az **Elemzések megtekintése** lehetőségre.
   
    ![](media/service-insights/pbi_autoinsightsuccess.png)
   
   > **MEGJEGYZÉS:**: Bizonyos adatkészletek esetén nem hozható létre Gyors elemzés, mert az adatok statisztikailag nem szignifikánsak.  Ha ezzel kapcsolatban további információra van szüksége, tekintse át az [adatok Gyors elemzésekhez történő optimalizálását](service-insights-optimize.md) bemutató cikket.
   > 
   > 
4. A vizualizációk a **Gyors elemzések** speciális vásznán jelennek meg, akár 32 különálló elemzéskártyán. Minden kártyán egy-egy diagram vagy ábra és egy rövid leírás látható.
   
    ![](media/service-insights/power-bi-insights.png)

## <a name="interact-with-the-quick-insight-cards"></a>A Gyors elemzéseket megjelenítő kártyák interaktív használata
  ![](media/service-insights/pbi_hover.png)

1. A vizualizáció irányítópultra történő felvételéhez vigye a kurzort az egyik kártya fölé, és válassza a kitűzés ikont.
2. Ha teljes képernyős méretben szeretné megtekinteni az egyik kártyát, húzza fölé a kurzort, majd válassza a Fókusz mód ikont.
   
    ![](media/service-insights/power-bi-insight-focus.png)
3. Fókusz módban a következő műveleteket végrehajtására van lehetőség:
   
   * Vizualizációk [szűrése](service-interact-with-a-report-in-reading-view.md).  A szűrők megjelenítéshez a jobb felső sarokban látható nyilat választva tudja kinyitni a Szűrők ablaktábláját.
     
        ![](media/service-insights/power-bi-insights-filter-new.png)
   * Az elemzéskártyát a kitűzés ![](media/service-insights/power-bi-pin-icon.png) ikont vagy a **Vizualizáció rögzítése** lehetőséget választva tűzheti ki egy irányítópultra.
   * Gyors elemzést magára a kártyára vonatkozóan is futtathat. Ezt **Hatókörön belüli gyors elemzésnek** nevezik. Válassza a jobb felső sarokban látható villanykörte ![](media/service-insights/power-bi-bulb-icon.png) ikont vagy az **Elemzések lekérése** lehetőséget.
     
       ![](media/service-insights/pbi-autoinsights-tile.png)
     
     A bal oldalon megjelennek a Gyors elemzések, a jobb oldalon pedig új kártyák láthatók, melyeket kizárólag az adott Gyors elemzésben szereplő adatok alapján készített a rendszer.
     
       ![](media/service-insights/power-bi-insights-on-insights-new.png)
4. Az eredeti gyors elemzéseket tartalmazó vászonra a bal felső sarokban látható **Kilépés a fókusz módból** lehetőséget választva léphet vissza.

## <a name="run-quick-insights-on-a-dashboard-tile"></a>Irányítópult csempére vonatkozó Gyors elemzések futtatása
Teljes adatkészletek összefüggéseinek feltárása helyett egyetlen irányítópult-csempe létrehozásához használt adatokra is szűkíthető az elemzés. Ezt **Hatókörön belüli gyors elemzésnek** nevezik.

1. Nyisson meg egy irányítópultot.
2. Válassza ki az egyik csempét és [nyissa meg Fókusz módban](service-focus-mode.md).
3. A jobb felső sarokban válassza az **Elemzések lekérése** lehetőséget.
   
    ![](media/service-insights/pbi-autoinsights-tile.png)
4. A Power BI a csempe jobb oldalán fogja megjeleníteni az elemzéskártyákat.
   
    ![](media/service-insights/pbi-insights-tile.png)
5. Felkeltette valamelyik elemzés az érdeklődését? Az adott elemzéskártyát kiválasztva az adatok mélyebb szintjére is leáshat. A kiválasztott Gyors elemzés a bal oldalon fog megjelenni, az új, kizárólag az adott Gyors elemzés adatain alapuló új elemzéskártyák pedig a jobb oldalon.
6. Az adatok mélyebb szintjeinek feltárását tovább folytatva az érdekes Gyors elemzések vizualizációját a jobb felső sarokban látható **Vizualizáció rögzítése** lehetőséget választva tűzheti ki az irányítópultra. Ezenkívül visszajelzést küldhet, tudatva az adatkészlet tulajdonosával, hogy hasznos volt-e a Gyors elemzés vagy sem.
   
    ![](media/service-insights/useful.png)

## <a name="next-steps"></a>További lépések
Ha Ön az adatkészlet tulajdonosa, akkor [optimalizálhatja azt gyors elemzések készítéséhez](service-insights-optimize.md)

További tudnivalók a [Gyors elemzések típusaival kapcsolatban](service-insight-types.md)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

