---
title: "Adatriasztások beállítása a Power BI szolgáltatásban"
description: "Itt elsajátíthatja, hogyan állíthat be riasztásokat, amelyek figyelmeztetik, ha az irányítópultjain lévő adatok változásai meghaladják a Microsoft Power BI szolgáltatásban beállított korlátokat."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: JbL2-HJ8clE
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/06/2017
ms.author: mihart
ms.openlocfilehash: cfbd7d124784b15b432921554c8ac5bbe321846c
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="data-alerts-in-power-bi-service"></a>Adatriasztások a Power BI szolgáltatásban
Riasztásokat állíthat be, amelyek figyelmeztetik, ha az irányítópultjain lévő adatok változásai meghaladják a beállított korlátokat. Csak a jelentések vizualizációiról rögzített csempéken, és kizárólag mérőműszerekre, KPI-kre és kártyákra állíthat be riasztásokat. A riasztásokat beállíthatja a jelentésekből az irányítópultokra rögzített streamelési adatkészletekről készített vizualizációkon, azonban az irányítópultokon a **Csempe hozzáadása** > **Egyedi folyamatos átviteli adatok** paranccsal közvetlenül létrehozott streamelési csempéken nem. Mindenki csak a saját riasztásait látja, még az irányítópult megosztása esetén is. A rendszer teljes mértékben szinkronizálja az adatriasztásokat a platformok között, így [a Power BI mobilalkalmazásokban](mobile-set-data-alerts-in-the-mobile-apps.md) és a Power BI szolgáltatásban is beállíthatja és megtekintheti őket. A Power BI Desktopban azonban nem érhetők el. A riasztások [automatizálhatók és integrálhatók a Microsoft Flow-val](https://flow.microsoft.com) - [– próbálja ki](service-flow-integration.md).

![](media/service-set-data-alerts/powerbi-alert-types-new.png)

> [!WARNING]
> Az adatalapú riasztások értesítései az adatokkal kapcsolatos információkat tartalmaznak. Ha Power BI-adatait egy mobileszközön követi, és az adott eszközt ellopják, javasoljuk, hogy a Power BI szolgáltatásban tiltsa le az összes adatalapú riasztási szabályt.
> 
> 

## <a name="set-data-alerts-in-power-bi-service"></a>Adatriasztások beállítása a Power BI szolgáltatásban
Tekintse meg, ahogy Amanda riasztásokat ad hozzá egyes csempékhez az irányítópultján. Ezután a videó alatt látható részletes utasítások szerint próbáljon meg Ön is riasztásokat beállítani.

<iframe width="560" height="315" src="https://www.youtube.com/embed/JbL2-HJ8clE" frameborder="0" allowfullscreen></iframe>

A példában Amanda a Retail Analysis (Kiskereskedelmi elemzés) minta-irányítópultról származó kártyacsempét használ.

1. Kezdje a műveletet egy irányítópulttal. Az irányítópult egyik mérőműszer-, KPI- vagy kártyacsempéjén kattintson a három pontra (...).
   
   ![](media/service-set-data-alerts/powerbi-card.png)
2. A harang ikon ![](media/service-set-data-alerts/power-bi-bell-icon.png) kiválasztásával adjon hozzá egy vagy több riasztást a **Total Stores** (Összes üzlet) csempéhez.
   
   ![](media/service-set-data-alerts/powerbi-set-alert.png)
3. Először győződjön meg róla, hogy a csúszka **Be** állásba van kapcsolva, és adjon címet a riasztásnak. A címek segítségével könnyebben felismerheti a riasztásokat.
   
   ![](media/service-set-data-alerts/powerbi-alert-title.png)
4. Görgessen le, és adja meg a riasztás adatait.  Ebben a példában most egy olyan riasztást állítunk be, amely napi küld értesítést, ha az üzletek száma 100 fölé emelkedik. A riasztások az Értesítési központban jelennek meg. Azt is beállítjuk, hogy a Power BI egy e-mailt is küldjön.
   
   ![](media/service-set-data-alerts/powerbi-set-alert-details.png)
5. Kattintson a **Mentés** gombra.

## <a name="receiving-alerts"></a>Riasztások fogadása
Ha egy követett adat eléri valamelyik beállított küszöböt, több dolog történik. Először is, a Power BI ellenőrzi, hogy eltelt-e legalább egy óra vagy 24 óra (a választott beállítástól függően) az utolsó riasztás óta. Ha az adat meghaladja a küszöböt, a rendszer mindenképp riasztást küld.

Ezután a Power BI egy riasztást küld az Értesítési központba, valamint választhatóan az e-mail-fiókjába is. Az egyes riasztásokban közvetlen hivatkozás mutat az adatokra. A hivatkozásra megnyitásával megtekintheti a vonatkozó csempét, ahol részletesebb információkat találhat, valamint megoszthatja az információkat.  

1. Ha úgy konfigurálta a riasztást, hogy az e-mailben is értesítse, valami ilyesmit talál majd a bejövő levelei közt.
   
   ![](media/service-set-data-alerts/powerbi-alerts-email.png)
2. A Power BI egy üzenetet küld az **Értesítési központba**, és egy új riasztás ikont jelenít meg az érintett csempén.
   
   ![](media/service-set-data-alerts/powerbi-alert-notifications.png)
3. A riasztás részleteinek megtekintéséhez nyissa meg az Értesítési központot.
   
    ![](media/service-set-data-alerts/powerbi-alert-notfication.png)
   
   > [!NOTE]
   > A riasztások kizárólag a frissített adatokon működnek. Az egyes adatok frissítésekor a Power BI ellenőrzi, hogy az adott adathoz van-e beállítva riasztás. Ha az adott adat elérte a riasztási küszöböt, a riasztás aktiválódik.
   > 
   > 

## <a name="managing-alerts"></a>Riasztások kezelése
A riasztások kezelésének három módja van: Magáról az irányítópulti csempéről, a Power BI Beállítások menüjéből, illetve egy adott csempéről a [Power BI iPhone-mobilalkalmazásban](mobile-set-data-alerts-in-the-mobile-apps.md) vagy a [Power BI Windows 10-mobilalkalmazásban](mobile-set-data-alerts-in-the-mobile-apps.md).

### <a name="from-the-tile-itself"></a>Magáról a csempéről
1. Ha módosítani vagy törölni szeretné egy adott csempe valamelyik riasztását, nyissa meg újra a **Riasztások kezelése** ablakot a harang ikon ![](media/service-set-data-alerts/power-bi-bell-icon.png) kiválasztásával. Az adott csempéhez beállított összes riasztás megjelenik.
   
    ![](media/service-set-data-alerts/powerbi-see-alerts.png).
2. A riasztás módosításához válassza a neve mellett balra található nyilat.
   
    ![](media/service-set-data-alerts/powerbi-see-alerts-arrow.png).
3. A riasztás módosításához válassza a neve mellett jobbra található kukát.
   
      ![](media/service-set-data-alerts/powerbi-see-alerts-delete.png)

### <a name="from-the-power-bi-settings-menu"></a>A Power BI Beállítások menüjéből
1. Kattintson a fogaskerék ikonra a Power BI menüsorán.
   
    ![](media/service-set-data-alerts/powerbi-gear-icon.png).
2. A **Beállítások** alatt válassza a **Riasztások** elemet.
   
    ![](media/service-set-data-alerts/powerbi-alert-settings.png)
3. Erről a felületről be- és kikapcsolhatja a riasztásokat, megnyithatja a **Riasztások kezelése** ablakot a riasztás módosításához, vagy akár törölheti is a riasztást.

## <a name="tips-and-troubleshooting"></a>Tippek és hibaelhárítás
* A Bing-csempék, illetve a dátum/idő mértékekkel rendelkező kártyacsempék jelenleg nem támogatják a riasztásokat.
* A riasztások kizárólag numerikus adattípusokkal működnek.
* A riasztások kizárólag a frissített adatokon működnek. Statikus adatokon nem.
* A riasztások a streamelési adatkészleteken csak akkor működnek, ha felépít egy KPI-/kártya-/mérőműszer-jelentési vizualizációt, majd rögzíti az irányítópulton.

## <a name="next-steps"></a>További lépések
[Adatriasztást tartalmazó Microsoft Flow létrehozása](service-flow-integration.md)    
[Adatriasztások beállítása mobileszközökön](mobile-set-data-alerts-in-the-mobile-apps.md)    
[Első lépések a Power BI-ban](service-get-started.md)    
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

