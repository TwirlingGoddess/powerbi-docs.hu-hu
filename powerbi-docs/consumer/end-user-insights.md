---
title: Adatelemzések automatikus generálása a Power BI-jal
description: Ismerje meg, hogyan kaphat elemzési információkat az adatkészletekről és az irányítópult-fájlokról.
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: et_MLSL2sA8
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 05/25/2018
ms.author: mihart
LocalizationGroup: Dashboards
ms.openlocfilehash: be2f1997fe27878967ac22435c0a6dbe94ffc5a2
ms.sourcegitcommit: 70192daf070ede3382ac13f6001e0c8b5fb8d934
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/22/2018
ms.locfileid: "46565291"
---
# <a name="automatically-generate-data-insights-with-power-bi"></a>Adatelemzések automatikus generálása a Power BI-jal
Van egy új adatkészlete, de nem tudja, hogy kezdje el feldolgozni?  Gyorsan létre kell hoznia egy irányítópultot?  Szeretne felfedezni eddig hiányzó összefüggéseket?

A Gyors elemzéseket futtatva érdekes interaktív vizualizációkat hozhat létre adataiból. Gyors elemzések egy teljes adatkészleten (gyors elemzések), illetve egy adott irányítópult-csempén is futtathatók (hatókörön belüli elemzés). Elemzésen is futtatható elemzés.

> **MEGJEGYZÉS:**: Az elemzés szolgáltatás csak a Power BI-ba feltöltött adatokhoz használható, DirectQueryvel előállított adatokhoz nem.
> 

Az elemzés szolgáltatás a Microsoft Research-csel együttműködésben fejlesztett, egyre növekvő számú [haladó szintű elemzési algoritmusra épül](end-user-insight-types.md). A Microsoft Research egyre több ember számára teszi lehetővé adatai újszerű és intuitív módszerekkel történő elemzését.

## <a name="run-quick-insights-on-a-dataset"></a>Gyors elemzések futtatása adatkészleteken
Tekintse meg, hogyan futtat Amanda gyors elemzést egy adatkészleten, hogyan nyit meg egy elemzést Fókusz módban, hogyan tűzi ki egy ilyen elemzést irányítópultjára csempeként, és hogyan kér gyors elemzést egy irányítópult-csempéhez kapcsolódóan.

<iframe width="560" height="315" src="https://www.youtube.com/embed/et_MLSL2sA8" frameborder="0" allowfullscreen></iframe>


Most Ön következik. Fedezze fel az elemzések szolgáltatást a [Supplier Quality Analysis mintát](../sample-supplier-quality.md) (Szállítói minőségelemzési mintát) használva.

1. Az **Adatkészletek** lapon kattintson a három pontra (...), majd válassza az **Elemzések lekérése** lehetőséget.
   
    ![Adatkészletek lap](./media/end-user-insights/power-bi-ellipses.png)
   
    ![három pont menü](./media/end-user-insights/power-bi-tab.png)
2. A Power BI [különböző algoritmusokat](end-user-insight-types.md) használ az adatkészlet trendjeinek kimutatásához.
   
    ![Elemzések keresése párbeszédpanel](./media/end-user-insights/pbi_autoinsightssearching.png)
3. Az elemzés másodpercek alatt elkészül.  A vizualizációk megjelenítéséhez kattintson az **Elemzések megtekintése** lehetőségre.
   
    ![sikert jelző üzenet](./media/end-user-insights/pbi_autoinsightsuccess.png)
   
   > **MEGJEGYZÉS:**: Bizonyos adatkészletek esetén nem hozható létre elemzés, mert az adatok statisztikailag nem szignifikánsak.  Ha ezzel kapcsolatban további információra van szüksége, tekintse át az [Adatok elemzésekhez történő optimalizálását](../service-insights-optimize.md) bemutató cikket.
   > 
   > 
1. A vizualizációk a **Gyors elemzések** speciális vásznán jelennek meg, akár 32 különálló elemzéskártyán. Minden kártyán egy-egy diagram vagy ábra és egy rövid leírás látható.
   
    ![Gyors elemzések vászon](./media/end-user-insights/power-bi-insights.png)

## <a name="interact-with-the-insight-cards"></a>Az elemzéseket megjelenítő kártyák interaktív használata
  ![gombostű ikon](./media/end-user-insights/pbi_hover.png)

1. A vizualizáció irányítópultra történő felvételéhez vigye a kurzort az egyik kártya fölé, és válassza a kitűzés ikont.
2. Mutasson egy kártyára, válassza a három pontot (...), majd az **Elemzések megtekintése** elemet. Ekkor az elemzés megnyílik teljes képernyős módban.
   
    ![Elemzés teljes képernyőn](./media/end-user-insights/power-bi-insight-focus.png)
3. Fókusz módban a következő műveleteket végrehajtására van lehetőség:
   
   * Vizualizációk szűrése.  A szűrők megjelenítéshez a jobb felső sarokban látható nyilat választva tudja kinyitni a Szűrők ablaktábláját.
        ![elemzés és a Szűrők menü kibontva](./media/end-user-insights/power-bi-insights-filter-new.png)
   * Az elemzéskártyát a gombostű ![gombostű ikon](./media/end-user-insights/power-bi-pin-icon.png)  ikont vagy a **Vizualizáció rögzítése** lehetőséget választva tűzheti ki egy irányítópultra.
   * Elemzést magára a kártyára vonatkozóan is futtathat. Ezt gyakran **hatókörön belüli elemzésnek** is nevezik. Válassza a jobb felső sarokban látható villanykörte ikont ![Elemzések lekérése ikon](./media/end-user-insights/power-bi-bulb-icon.png)  vagy az **Elemzések lekérése** lehetőséget.
     
       ![az Elemzések lekérése ikon a menüsávon](./media/end-user-insights/pbi-autoinsights-tile.png)
     
     A bal oldalon megjelennek az elemzések, a jobb oldalon pedig új kártyák láthatók, melyeket kizárólag az adott elemzésben szereplő adatok alapján készített a rendszer.
     
       ![egymáson lévő elemzések](./media/end-user-insights/power-bi-insights-on-insights-new.png)
4. Az eredeti elemzéseket tartalmazó vászonra a bal felső sarokban látható **Kilépés a fókusz módból** lehetőséget választva léphet vissza.

## <a name="run-insights-on-a-dashboard-tile"></a>Irányítópult csempére vonatkozó elemzések futtatása
Teljes adatkészletek összefüggéseinek feltárása helyett egyetlen irányítópult-csempe létrehozásához használt adatokra is szűkíthető az elemzés. Ezt is gyakran **hatókörön belüli elemzésnek** is nevezik.

1. Nyisson meg egy irányítópultot.
2. Vigye az egérmutatót egy csempe fölé. válassza a három pontot (...), majd az **Elemzések megtekintése** lehetőséget. A csempe [Fókusz módban](end-user-focus.md) nyílik meg, és a jobb oldalán jelennek meg az elemzéskártyák.    
   
    ![Fókusz mód](./media/end-user-insights/pbi-insights-tile.png)    
4. Felkeltette valamelyik elemzés az érdeklődését? Az adott elemzéskártyát kiválasztva az adatok mélyebb szintjére is leáshat. A kiválasztott elemzés a bal oldalon fog megjelenni, az új, kizárólag az adott elemzés adatain alapuló új elemzéskártyák pedig a jobb oldalon.    
6. Az adatok mélyebb szintjeinek feltárását tovább folytatva az érdekes elemzéseket a jobb felső sarokban látható **Vizualizáció rögzítése** lehetőséget választva tűzheti ki az irányítópultra.

## <a name="next-steps"></a>Következő lépések
Ha Ön az adatkészlet tulajdonosa, akkor [optimalizálhatja azt gyors elemzések készítéséhez](../service-insights-optimize.md)

További tudnivalók a [Gyors elemzések típusaival kapcsolatban](end-user-insight-types.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

