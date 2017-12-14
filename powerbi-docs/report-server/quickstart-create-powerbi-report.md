---
title: "Rövid útmutató: Power BI-jelentés létrehozása a Power BI jelentéskészítő kiszolgálóra"
description: "Ismerje meg, hogy miképpen hozhat létre Power BI-jelentést a Power BI jelentéskészítő kiszolgálóra néhány egyszerű lépésben."
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 10/28/2017
ms.author: maggies
ms.openlocfilehash: e492d31a8e1ed57a769c9a36f515d99369f6d6dc
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="quickstart-create-a-power-bi-report-for-power-bi-report-server"></a>Rövid útmutató: Power BI-jelentés létrehozása a Power BI jelentéskészítő kiszolgálóra
A Power BI-jelentéseket helyszínen is tárolhatja és kezelheti a Power BI jelentéskészítő kiszolgáló webportálján, ahogy a felhőben tárolhatja a Power BI szolgáltatásban (https://powerbi.com). A jelentéseket a Power BI Desktopban hozhatja létre, majd közzéteheti a webportálon. Ekkor a jelentések megtekinthetővé válnak a cégen belüli olvasók számára egy böngésző vagy egy Power BI-mobilalkalmazás használatával.

![Power BI-jelentés a webportálon](media/quickstart-create-powerbi-report/report-server-powerbi-report.png)

Ha már létrehozott jelentéseket a Power BI Desktopban, a Power BI jelentéskészítő kiszolgálóra is létrehozhat Power BI-jelentéseket. Ha még nem, akkor négy gyors lépésben felkészülhet rá.

## <a name="step-1-install-power-bi-desktop-report-server"></a>1. lépés: A jelentéskészítő kiszolgálóra optimalizált Power BI Desktop telepítése
Lehet, hogy a Power BI Desktop már telepítve van a Power BI szolgáltatás számára létrehozandó jelentésekhez. Javasoljuk, hogy a kiszolgáló és az alkalmazás folyamatos szinkronizálása érdekében telepítse a Power BI Desktop Power BI jelentéskészítő kiszolgálóra optimalizált verzióját. Ugyanazon a számítógépen a Power BI Desktop mindkét változata telepítve lehet.

1. A Power BI jelentéskészítő kiszolgáló webportálján kattintson az **Új** > **Power BI-jelentés** elemre.
   
    ![Új Power BI-jelentés](media/quickstart-create-powerbi-report/report-server-web-portal-new-powerbi-report.png)
   
    Ha nincs hozzáférése a Power BI jelentéskészítő kiszolgáló webportáljához, nyissa meg a Microsoft Download Centert, és töltse le a [Microsoft Power BI Desktop](https://go.microsoft.com/fwlink/?linkid=837581) Power BI jelentéskészítő kiszolgálóra optimalizált verzióját – (2017. június GA).
2. A telepítési folyamat végén kattintson a **Power BI Desktop azonnali indítása** lehetőségre.
   
    A folyamat automatikusan elindul, és máris hozzákezdhet. A címsorban látható „Power BI Desktop (Report Server)" feliratból láthatja, hogy a megfelelő verziót töltötte le.
3. Ha még nem ismeri a Power BI Desktopot, érdemes megtekintenie az üdvözlőképernyőn látható videókat.
   
    ![A Power BI Destop üdvözlőképernyője](media/quickstart-create-powerbi-report/report-server-powerbi-desktop-start.png)

## <a name="step-2-select-a-data-source"></a>2. lépés: Az adatforrás kiválasztása
Számos adatforráshoz kapcsolódhat. További információkért lásd: [Kapcsolódás az adatforrásokhoz](connect-data-sources.md).

1. Az üdvözlőképernyőn kattintson az **Adatok beolvasása** elemre.
   
    Vagy a **Kezdőlap** lapon kattintson az **Adatok beolvasása** elemre.
2. Válassza ki az adatforrást – ebben a példában ez az**Analysis Services**.
   
    ![Adatforrás kiválasztása](media/quickstart-create-powerbi-report/report-server-get-data-ssas.png)
3. Adja meg a **Kiszolgálót** és igény szerint az **Adatbázist**. Győződjön meg róla, hogy az **Élő csatlakozás** elem ki van jelölve > **OK**.
   
    ![A kiszolgáló neve](media/quickstart-create-powerbi-report/report-server-ssas-server-name.png)
4. Válassza ki azt a jelentéskészítő kiszolgálót, amelyen menteni fogja jelentéseket.
   
    ![Jelentéskészítő kiszolgáló kiválasztása](media/quickstart-create-powerbi-report/report-server-select-server.png)

## <a name="step-3-design-your-report"></a>3. lépés: A jelentés megtervezése
Most jön a legérdekesebb rész: az adatokat illusztráló vizualizációk létrehozása.

Például tölcsérdiagramot hozhat létre az éves jövedelem alapján csoportokba rendezett ügyfelekről.

![Jelentés megtervezése](media/quickstart-create-powerbi-report/report-server-create-funnel.png)

1. A **Megjelenítések** ablaktáblán kattintson a **Tölcsérdiagram** lehetőségre.
2. Húzza a megszámlálandó mezőt az **Értékek** oszlopba. Ha nem numerikus mezőről van szó, a Power BI Desktop automatikusan hozzáteszi a *Count of* (Száma) kiegészítést.
3. A csoportosítandó mezőt húzza a **Csoport** oszlopba.

További információk a [Power BI-jelentés megtervezéséről](../desktop-report-view.md).

## <a name="step-4-save-your-report-to-the-report-server"></a>4. lépés: A jelentés mentése a jelentéskészítő kiszolgálón
A kész jelentést mentse a 2. lépésben kiválasztott Power BI jelentéskészítő kiszolgálón.

1. A **Fájl** menüben kattintson a**Mentés másként** > **Power BI jelentéskészítő kiszolgáló** elemre.
   
    ![Mentés a jelentéskészítő kiszolgálón](media/quickstart-create-powerbi-report/report-server-save-as-powerbi-report-server.png)
2. Most már megtekintheti a jelentést a webportálon.
   
    ![A jelentés megtekintése a webportálon](media/quickstart-create-powerbi-report/report-server-powerbi-report.png)

## <a name="considerations-and-limitations"></a>Megfontolások és korlátozások
A Power BI jelentéskészítő kiszolgálón és a Power BI szolgáltatásban (http://powerbi.com) tárolt jelentések működése szinte teljesen megegyezik, de bizonyos funkciók eltérnek egymástól.

### <a name="in-a-browser"></a>Böngészőben
A Power BI jelentéskészítő kiszolgálón tárolt jelentések minden vizualizációt támogatnak, köztük:

* Egyéni vizualizációk

A Power BI jelentéskészítő kiszolgálón tárolt jelentések nem támogatják az alábbiakat:

* R vizualizációk
* ArcGIS-térképek
* Útkövetési eszközök

### <a name="in-the-power-bi-mobile-apps"></a>A Power BI-mobilalkalmazásokban
A Power BI jelentéskészítő kiszolgálón tárolt jelentések a [Power BI-mobilalkalmazások](../mobile-apps-for-mobile-devices.md) minden alapvető funkcióját támogatják, köztük:

* [A jelentés telefonos elrendezése](../desktop-create-phone-report.md): A jelentést optimalizálhatja a Power BI-mobilalkalmazásokra. Az optimalizált jelentéseknek különleges ikonjuk ![Jelentés telefonos elrendezésének ikonja](media/quickstart-create-powerbi-report/power-bi-rs-mobile-optimized-icon.png) és elrendezésük van a mobiltelefonon.
  
    ![Mobiltelefonokra optimalizált jelentés](media/quickstart-create-powerbi-report/power-bi-rs-mobile-optimized-report.png)

A Power BI jelentéskészítő kiszolgálón tárolt jelentések nem támogatják a Power BI-mobilalkalmazások alábbi funkcióit:

* R vizualizációk
* ArcGIS-térképek
* Egyéni vizualizációk
* Útkövetési eszközök
* Geofiltering vagy vonalkódok

## <a name="next-steps"></a>További lépések
### <a name="power-bi-desktop"></a>Power BI Desktop
A Power BI Desktop számos nagyszerű erőforrással segíti a jelentéskészítést. Az alábbi hivatkozások jó kiindulási pontot jelentenek.

* [Első lépések a Power BI Desktoppal](../desktop-getting-started.md)
* Interaktív tanulás: [Első lépések a Power BI Desktoppal](../guided-learning/gettingdata.yml#step-2)

### <a name="power-bi-report-server"></a>Power BI jelentéskészítő kiszolgáló
* [A Power BI jelentéskészítő kiszolgálóra optimalizált Power BI Desktop telepítése](install-powerbi-desktop.md)  
* [Felhasználói kézikönyv a Power BI jelentéskészítő kiszolgálóhoz](user-handbook-overview.md)  

További kérdései vannak? [Kérdezze a Power BI-közösséget!](https://community.powerbi.com/)