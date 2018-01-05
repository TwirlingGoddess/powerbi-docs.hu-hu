---
title: "Irányítópult-csempék a Power BI szolgáltatásban"
description: "Minden, amit a Power BI irányítópult csempékről tudni érdemes. Ide tartoznak az SQL Server Reporting Services-ből (SSRS-ből) létrehozott csempék is."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: 
qualitydate: 03/15/2016
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: d1960ea42bee8b00cc6dd095e94ebf6f6303bce8
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="dashboard-tiles-in-power-bi"></a>Irányítópult-csempék a Power BI-ban
Az irányítópultok és az irányítópulton található csempék nem a Power BI Desktophoz, hanem a Power BI szolgáltatáshoz tartozó funkciók. A Power BI mobilalkalmazásban nem hozhatók létre és nem tűzhetők ki irányítópult-csempék, de [megtekinthetők és megoszthatók](mobile-tiles-in-the-mobile-apps.md) abból. Ezenkívül a Power BI mobilalkalmazásban [képeket vehet fel az irányítópulthoz az iPhone-alkalmazással](mobile-iphone-app-get-started.md).

## <a name="dashboard-tiles"></a>Irányítópult-csempék
![](media/service-dashboard-tiles/power-bi-dashboard.png)

A csempék az adatokról készített és az irányítópultra kitűzött pillanatfelvételek. Csempe létrehozható jelentésből, Q&A mezőből, Excelből, SQL Server Reporting Services-ből (SSRS-ből), és sok minden másból.  Ezen a képernyőfelvételen több irányítópultra tűzött csempe látható.

A kitűzés mellett, önmagukban álló csempék is kitűzhetők közvetlenül az irányítópultra a [Csempe hozzáadása](service-dashboard-add-widget.md) lehetőséget használva. Önmagukban álló csempék lehetnek többek között szövegmezők, képek, videók, streaming-adatok, webtartalmak.

További segítségre van szüksége annak megértéséhez, hogy milyen elemekből épül fel a Power BI?  Tekintse meg a [Power BI alapfogalmait](service-basic-concepts.md) ismertető cikket.

> [!NOTE]
> A csempe létrehozásához használt vizualizációs elem változásakor a csempe nem változik.  Például ha kitűz egy sávdiagramot egy jelentésből, majd a sávdiagramot oszlopdiagramra cseréli, az irányítópulton megjelenő csempén továbbra is sávdiagram lesz látható. Az adatok frissülni fognak, de a diagram típusa nem.
> 
> 

## <a name="pin-a-tile-from"></a>Csempe kitűzése
Az irányítópultokra többféleképpen lehet felvenni (kitűzni) csempét. Csempék kitűzhetők:

* [Power BI Q&A-ből](service-dashboard-pin-tile-from-q-and-a.md)
* [jelentésből](service-dashboard-pin-tile-from-report.md)
* [másik irányítópultról](service-pin-tile-to-another-dashboard.md)
* [OneDrive vállalati verzión található Excel-munkafüzetből](service-dashboard-pin-tile-from-excel.md)
* [az Excelhez készült Power BI Publisherből](publisher-for-excel.md)
* [gyors elemzésekből](service-insights.md)
* [SSRS-ből](https://msdn.microsoft.com/library/mt604784.aspx)

A képek, szövegdobozok, videók, streamelési adatok és webtartalmak különálló csempéi közvetlenül az irányítópulton is létrehozhatók a [Csempe hozzáadása](service-dashboard-add-widget.md) lehetőséget használva.

  ![](media/service-dashboard-tiles/add_widgetnew.png)

## <a name="interacting-with-tiles-on-a-dashboard"></a>Az irányítópulton levő csempék használata
### <a name="move-and-resize-a-tile"></a>Csempék mozgatása és átméretezése
Fogja meg az egyik csempét, és [mozgassa körbe az irányítópulton](service-dashboard-edit-tile.md). A csempe átméretezéséhez álljon a csempe fogópontjához ![](media/service-dashboard-tiles/resize-handle.jpg).

### <a name="hover-over-a-tile-to-change-the-appearance-and-behavior"></a>Csempék megjelenésének és működésének módosítása a csempére pozicionálva
1. A három pont megjelenítéséhez álljon a csempe fölé.
   
    ![](media/service-dashboard-tiles/ellipses_new.png)
2. A három pontra kattintva nyissa meg a csempeműveletek menüjét.
   
    ![](media/service-dashboard-tiles/power-bi-tile-menu.png)
   
    Ebből a menüből:
   
   * [Megnyithatja a csempe létrehozásához használt jelentést](service-reports.md)![](media/service-dashboard-tiles/chart-icon.jpg)  
   
   * [Megnyithatja a csempe létrehozásához használt munkafüzetet](service-reports.md)![](media/service-dashboard-tiles/power-bi-open-worksheet.png)  
     
     * [Megnyithatja a csempét fókusz módban](service-focus-mode.md)![](media/service-dashboard-tiles/fullscreen-icon.jpg)  
     * [Exportálhatja a csempéhez használt adatokat](power-bi-visualization-export-data.md)![](media/service-dashboard-tiles/export-icon.png)
     * [Szerkesztheti a címet és az alcímet, felvehet egy hivatkozást, és megjelenítheti az utolsó frissítés idejét](service-dashboard-edit-tile.md)![](media/service-dashboard-tiles/pencil-icon.jpg)
     * [Elemzéseket futtathat](service-insights.md)![](media/service-dashboard-tiles/power-bi-insights.png)
     * [Kitűzheti a csempét egy másik irányítópultra](service-pin-tile-to-another-dashboard.md)
       ![](media/service-dashboard-tiles/pin-icon.jpg)
   * [Eltávolíthatja a csempét](service-dashboard-edit-tile.md)
     ![](media/service-dashboard-tiles/trash-icon.png)
3. A művelet menü bezárásához kattintson egy üres területre a vásznon.

### <a name="select-click-a-tile"></a>Csempék kiválasztása
Az, hogy mi történik, amikor rákattint valamelyik csempére, attól függ, hogyan lett létrehozva a csempe, és hogy tartozik-e hozzá [egyedi hivatkozás](service-dashboard-edit-tile.md). Ha tartozik hozzá egyedi hivatkozás, a csempe kiválasztásakor a rendszer a hivatkozott oldalra lépteti. Más esetben a csempére kattintáskor a létrehozásához használt helyszíni jelentéshez, Excel-munkafüzethez, SSRS-jelentéshez vagy Q&A-kérdéshez irányítja a rendszer.

> [!NOTE]
> Ez alól csak a közvetlenül az irányítópulton a **Csempe hozzáadása** funkcióval létrehozott videócsempék képeznek kivételt. Amikor egy így létrehozott videócsempére kattint, a rendszer közvetlenül az irányítópulton játssza le a videót.   
> 
> 

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
* Ha a vizualizáció létrehozásához használt jelentés nem lett mentve, akkor nem történik semmi a csempére kattintáskor.
* Ha a csempe Excel Online-munkafüzetből lett létrehozva, és a felhasználónak ahhoz nincs legalább Olvasási jogosultsága, a csempe kiválasztásakor nem fog megnyílni az Excel Online-munkafüzet.
* Olyan csempe esetén, melyet a **Csempe létrehozása** funkcióval közvetlenül az irányítópulton hozott létre a felhasználó, és beállított hozzá egy egyedi hiperhivatkozást, a csempe címére, alcímére vagy magára a csempére kattintáskor a rendszer megnyitja az adott URL-címet.  Más esetben a közvetlenül az irányítópulton kép, webkód vagy szövegdoboz részére létrehozott csempe kiválasztása nem indít el semmilyen műveletet.
* Ha az SSRS-en nem jogosult egy jelentés használatára, az SSRS alapján létrehozott csempék kiválasztásakor a rendszer megjelenít egy oldalt, amely jelezni fog, hogy a felhasználó nem rendelkezik megfelelő hozzáféréssel (rsAccessDenied).
* Ha nincs hozzáférése ahhoz a hálózathoz, ahol az SSRS található, SSRS-ből létrehozott csempe kiválasztásakor a rendszer megjelenít majd egy oldalt, amely azt jelzi, hogy a kiszolgáló nem található (HTTP 404). Ahhoz, hogy meg tudja tekinteni a jelentést, az Ön eszközének hálózati hozzáféréssel kell rendelkeznie a jelentés-kiszolgálóhoz.
* A csempe létrehozásához használt vizualizációs elem változásakor a csempe nem változik.  Például ha kitűz egy sávdiagramot egy jelentésből, majd a sávdiagramot oszlopdiagramra cseréli, az irányítópulton megjelenő csempén továbbra is sávdiagram lesz látható. Az adatok frissülni fognak, de a diagram típusa nem.

## <a name="next-steps"></a>További lépések
[Nagy méretű számot tartalmazó csempe létrehozása jelentésből](power-bi-visualization-big-number-report.md)

[Nagy méretű számot tartalmazó csempe létrehozása Q&A -ből](power-bi-visualization-big-number.md)

[A Power BI-irányítópultok](service-dashboards.md)  

[Adatfrissítés](refresh-data.md)

[Power BI – alapfogalmak](service-basic-concepts.md)

[Csempe exportálása Power Pointba](http://blogs.msdn.com/b/powerbidev/archive/2015/09/28/integrating-power-bi-tiles-into-office-documents.aspx)

[Reporting Services-elemek kitűzése Power BI-irányítópultokra](https://msdn.microsoft.com/library/mt604784.aspx)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)
