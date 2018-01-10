---
title: "Kibocsátási megjegyzések a Power BI jelentéskészítő kiszolgálóhoz"
description: "Ez a témakör a Power BI jelentéskészítő kiszolgáló korlátait és problémáit írja le."
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
ms.author: maghan
ms.openlocfilehash: aa0f8870396980edfdb85739e0459c365d1e2163
ms.sourcegitcommit: eec6b47970bf69ed30638d1a20051f961ba792f2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/06/2018
---
# <a name="power-bi-report-server-release-notes"></a>Kibocsátási megjegyzések a Power BI jelentéskészítő kiszolgálóhoz
Ez a témakör a Power BI jelentéskészítő kiszolgáló korlátait és problémáit írja le.

A Power BI jelentéskészítő kiszolgáló és a Power BI jelentéskészítő kiszolgálóra optimalizált Power BI Desktop letöltéséhez keresse fel a [Helyszíni jelentéskészítés a Power BI jelentéskészítő kiszolgálóval](https://powerbi.microsoft.com/report-server/) oldalt.

## <a name="october-2017"></a>2017. október
* Importált adatok támogatása a Power BI-jelentésekben
* Excel-munkafüzetek megtekinthetősége a webportálon. Ez az Office Online Server konfigurálásával érhető el.
* Támogatás az új Power BI tábla- és mátrixvizualizációihoz.
* REST API-támogatás

## <a name="june-2017"></a>2017. június
* 2017. júniusra nincs új elem.

## <a name="may-2017"></a>2017. május
* A Power BI jelentéskészítő kiszolgálóval történő együttműködés érdekében a Power BI-jelentéseket a Power BI jelentéskészítő kiszolgálóra optimalizált Power BI Desktoppal kell létrehozni. A Power BI Desktop letöltési hivatkozása a lap tetején található.
* A (táblázatos vagy többdimenziós) Analysis Services esetében a Power BI-jelentések csak az élő kapcsolatokat támogatják.
* Az R vizualizációkhoz nincs támogatás.

**Probléma és ügyfélérintettség:** Ha ugyanazon a számítógépen az SQL Server Reporting Services és a Power BI jelentéskészítő kiszolgáló egyaránt telepítve van, és az egyiket eltávolítja, a jelentéskészítő kiszolgáló konfigurációkezelőjével már nem tud kapcsolódni a megmaradt jelentéskészítő kiszolgálóhoz.

**Megoldáskeresés** A probléma elkerülésére a kiszolgálók egyikének eltávolítása után a következő műveleteket kell végrehajtania.

1. Nyisson meg egy parancssort rendszergazdai módban.
2. Nyissa meg azt a könyvtárat, ahol a megmaradt jelentéskészítő kiszolgáló telepítve van.
   
    *A Power BI jelentéskészítő kiszolgáló alapértelmezett helye: C:\Program Files\Microsoft Power BI Report Server*
   
    *Az SQL Server Reporting Services alapértelmezett helye: C:\Program Files\Microsoft SQL Server Reporting Services*
3. Ezután nyissa meg a következő mappát. Attól függően, hogy melyik kiszolgáló maradt a gépen, ez vagy az *SSRS* vagy az *PBIRS* mappa.
4. Nyissa meg a WMI mappát.
5. Futtassa a következő parancsot:
   
    ```
    regsvr32 /i ReportingServicesWMIProvider.dll
    ```
   
    Ha a következő hibát látja, figyelmen kívül hagyhatja.
   
    ```
    The module "ReportingServicesWMIProvider.dll" was loaded but the entry-point DLLInstall was not found. Make sure that "ReportingServicesWMIProvider.dll" is a valid DLL or OCX file and then try again.
    ```

## <a name="next-steps"></a>További lépések
[A Power BI jelentéskészítő kiszolgáló újdonságai](whats-new.md)  
[Felhasználói kézikönyv](user-handbook-overview.md)  
[Rendszergazdai kézikönyv](admin-handbook-overview.md)  
[Rövid útmutató: A Power BI jelentéskészítő kiszolgáló telepítése](quickstart-install-report-server.md)  
[A Jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

