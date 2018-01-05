---
title: "A Power BI jelentéskészítő kiszolgáló böngészőtámogatása"
description: "Ismerje meg, hogy a böngészők mely verziói támogatják a Power BI jelentéskészítő kiszolgáló és a Jelentésmegjelenítő vezérlők kezelését és megtekintését."
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 11/01/2017
ms.author: asaxton
ms.openlocfilehash: 3e146417c78c7c95221c37051eda08a7b8497012
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="browser-support-for-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgáló böngészőtámogatása
Ismerje meg, hogy a böngészők mely verziói támogatják a Power BI jelentéskészítő kiszolgáló és a Jelentésmegjelenítő vezérlők kezelését és megtekintését.

## <a name="browser-requirements-for-the-web-portal"></a>A webportál böngészőkövetelményei
Az alábbiakban látható a webportál támogatott böngészőinek jelenlegi listája.

**Microsoft Windows**  
*Windows 7, 8.1, 10; Windows Server 2008 R2, 2012, 2012 R2*

* Microsoft Edge (+)
* Microsoft Internet Explorer 11
* Google Chrome (+)
* Mozilla Firefox (+)

**Apple OS X**  
*OS X 10.9–10.11*

* Apple Safari (+)
* Google Chrome (+)
* Mozilla Firefox (+)

**Apple iOS**  
*iOS 9 rendszerű iPhone és iPad*

* Apple Safari (+)

**Google Android**  
*Android 4.4 (KitKat) vagy újabb rendszerű telefonok és táblagépek*

* Google Chrome (+)
  
  **(+)** Legfrissebb verziójú nyilvánosan elérhető kiadás

## <a name="browser-requirements-for-the-report-viewer-web-control-2015"></a>A Jelentésmegjelenítő webes vezérlő böngészőkövetelményei (2015)
Az alábbiakban látható a Jelentésmegjelenítő webes vezérlő támogatott böngészőinek jelenlegi listája. A Jelentésmegjelenítő a jelentések webportálon keresztül történő megtekintését támogatja.

**Microsoft Windows**  
*Windows 7, 8.1, 10; Windows Server 2008 R2, 2012, 2012 R2*

* Microsoft Edge (+)
* Microsoft Internet Explorer 11
* Google Chrome (+)
* Mozilla Firefox (+)

**Apple OS X**  
*OS X 10.9–10.11*

* Apple Safari (+)
  
  **(+)** Legfrissebb verziójú nyilvánosan elérhető kiadás

### <a name="authentication-requirements"></a>Hitelesítési követelmények
Ahhoz, hogy az ügyfélkérelem sikeres lehessen, a jelentéskészítő kiszolgálónak kezelnie kell a böngészőkre jellemző hitelesítési sémákat. Az alábbi táblázatban láthatók a Windows rendszeren futó böngészők által támogatott alapértelmezett hitelesítési típusok.

| **Böngésző típusa** | **Támogatott** | **Böngésző alapértelmezése** | **Kiszolgáló alapértelmezése** |
| --- | --- | --- | --- |
| **Microsoft Edge** (+) |Negotiate, Kerberos, NTLM, Alapszintű |Negotiate |Igen. Az alapértelmezett hitelesítési beállítások működnek Edge-ben. |
| **Microsoft Internet Explorer** |Negotiate, Kerberos, NTLM, Alapszintű |Negotiate |Igen. Az alapértelmezett hitelesítési beállítások működnek Internet Explorerben. |
| **Google Chrome**(+) |Negotiate, NTLM, Alapszintű |Negotiate |Igen. Az alapértelmezett hitelesítési beállítások működnek Chrome-ban. |
| **Mozilla Firefox**(+) |NTLM, Alapszintű |NTLM |Igen. Az alapértelmezett hitelesítési beállítások működnek Firefoxban. |
| **Apple Safari**(+) |NTLM, Alapszintű |Alapszintű |Igen. Az alapértelmezett hitelesítési beállítások működnek Safariban. |

 **(+)** Legfrissebb verziójú nyilvánosan elérhető kiadás

### <a name="script-requirements-for-viewing-reports"></a>Jelentés megtekintésének parancsfájl-követelményei
A jelentésmegjelenítő használatához a böngészőben konfigurálni kell a parancsfájlok futtatását.

Ha a parancsfájlok nincsenek engedélyezve, akkor a jelentés megnyitásakor egy, az alábbihoz hasonló hibaüzenetet jelenik meg:

```
Your browser does not support scripts or has been configured to not allow scripts to run. Click here to view this report without scripts
```

 Ha azt a lehetőséget választja, hogy parancsfájl-támogatás nélkül tekinti meg a jelentést, akkor a jelentés HTML-ben fog megjelenni, és nem lesznek elérhetők a jelentésmegjelenítési képességek, például a jelentés eszköztára vagy a dokumentumtérkép.

> [!NOTE]
> A jelentés eszköztára a HTML-megjelenítő összetevő része. Az eszköztár alapértelmezetten a böngészőben megjelenített jelentések tetején helyezkedik el. A jelentésmegjelenítő funkciói segítségével többek között kereshet a jelentésben található információk között, görgethet egy adott oldalra vagy módosíthatja az oldal méretét a megtekintés céljának megfelelően. A jelentés eszköztárával vagy a HTML-megjelenítővel kapcsolatban további tudnivalókat a [HTML-megjelenítő és Jelentési eszköztár](https://docs.microsoft.com/sql/reporting-services/html-viewer-and-the-report-toolbar) című cikkben talál.
> 
> 

## <a name="browser-support-for-report-viewer-web-server-controls-in-visual-studio"></a>A Visual Studióban használt Jelentésmegjelenítő webes kiszolgálóvezérlő támogatott böngészői
A Jelentésmegjelenítő webes kiszolgálóvezérlő használatával jelentési funkciók ágyazhatók be ASP.NET-webalkalmazásokba. A Jelentésmegjelenítő webes vezérlő beszerzésével kapcsolatban további tudnivalókat [A Reporting Services integrálása a Jelentésmegjelenítő webes vezérlő használatával – Első lépések](https://docs.microsoft.com/sql/reporting-services/application-integration/integrating-reporting-services-using-reportviewer-controls-get-started) című cikkben talál.

Olyan böngészőt használjon, amelyikben a parancsfájlok használata engedélyezve van. Ha a böngésző nem képes parancsfájlokat futtatni, akkor a jelentés nem lesz megtekinthető.

**Microsoft Windows**  
*Windows 7, 8.1, 10; Windows Server 2008 R2, 2012, 2012 R2*

* Microsoft Edge (+)
* Microsoft Internet Explorer 11
* Google Chrome (+)
* Mozilla Firefox (+)
  
  **(+)** Legfrissebb verziójú nyilvánosan elérhető kiadás

## <a name="next-steps"></a>Következő lépések
[Rendszergazdai kézikönyv](admin-handbook-overview.md)  
[Gyors üzembe helyezés: Power BI jelentéskészítő kiszolgáló telepítése](quickstart-install-report-server.md)  
[A jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)
