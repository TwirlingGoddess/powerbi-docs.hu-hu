---
title: 'Rövid útmutató: A Power BI jelentéskészítő kiszolgáló telepítése'
description: A Power BI jelentéskészítő kiszolgáló telepítése nagyon gyorsan elvégezhető. Mindössze néhány perc szükséges a letöltéstől a telepítésig és a konfigurálásig.
services: powerbi
documentationcenter: ''
author: maggiesMSFT
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 03/19/2018
ms.author: maggies
ms.openlocfilehash: 625864384f73260ec0f62b74ff9a95e966289da0
ms.sourcegitcommit: 93e7362fc47319959b6992dfd037effdf831d010
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/21/2018
---
# <a name="quickstart-install-power-bi-report-server"></a>Rövid útmutató: A Power BI jelentéskészítő kiszolgáló telepítése
A Power BI jelentéskészítő kiszolgáló telepítése nagyon gyorsan elvégezhető. Mindössze néhány perc szükséges a letöltéstől a telepítésig és a konfigurálásig.

Az alábbiakban egy rövid áttekintést olvashat, amely alapján gyorsan üzembe helyezhet egy új jelentéskészítő kiszolgálót. A jelentéskészítő kiszolgálók telepítéséről részletesebb információt [A Power BI jelentéskészítő kiszolgáló telepítése](install-report-server.md) című részben talál.

## <a name="video-install-power-bi-report-server"></a>Videó: A Power BI jelentéskészítő kiszolgáló telepítése

<iframe width="640" height="360" src="https://www.youtube.com/embed/zacaEb9A4F0?showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="before-you-begin"></a>Előkészületek
Javasoljuk, hogy a Power BI jelentéskészítő kiszolgáló telepítése előtt tekintse át a [Power BI jelentéskészítő kiszolgáló telepítésének hardver- és szoftverkövetelményeit](system-requirements.md).

## <a name="step-1-download"></a>1. lépés: Letöltés

A Power BI jelentéskészítő kiszolgáló, illetve a Power BI jelentéskészítő kiszolgálóra optimalizált Power BI Desktop letöltéséhez nyissa meg a [Helyszíni jelentéskészítés a Power BI jelentéskészítő kiszolgálóval](https://powerbi.microsoft.com/report-server/) című lapot, és válassza az **Ingyenes próbaverzió letöltése** lehetőséget.

Az utasításokat követve töltse le a Power BI jelentéskészítő kiszolgáló telepítési fájljait. 

![A Power BI jelentéskészítő kiszolgáló letöltése](media/quickstart-install-report-server/download-pbireportserver.png)

## <a name="step-2-run-installer"></a>2. lépés: A telepítő futtatása
Futtassa a letöltött PowerBIReportServer.exe fájlt, és végezze el a telepítési képernyők lépéseit. Kiválaszthatja a telepítési útvonalat, valamint a telepíteni kívánt kiadást. A 180 nap után lejáró értékelés, fejlesztői kiadás vagy termékkulcs megadása közül választhat.

![A Power BI jelentéskészítő kiszolgáló telepítése](media/quickstart-install-report-server/pbireportserver-install.png)

## <a name="step-3-configure-the-server"></a>3. lépés: A kiszolgáló konfigurálása
A telepítés elvégzése után futtassa a Configuration Managert a kiszolgáló beállításának befejezéséhez. Létre kell hoznia egy ReportServer katalógus-adatbázist, és meg kell erősítenie a webes portál és a webszolgáltatás URL-címeit is.

![A Power BI jelentéskészítő kiszolgáló konfigurálása](media/quickstart-install-report-server/pbireportserver-configure.png)

## <a name="step-4-browse-to-web-portal"></a>4. lépés: A webes portál megnyitása böngészőben
Most, hogy befejezte a konfigurálási folyamatot, egy böngészőben megnyithatja a kiszolgáló webes portálját. Alapértelmezés szerint a cím a következő: `http://localhost/reports`. A gépnevet is használhatja az alapértelmezett localhost helyett, feltéve, hogy semmilyen tűzfaltípus nem akadályozza ebben.

![Power BI jelentéskészítő kiszolgáló webes portálja](media/quickstart-install-report-server/web-portal.png)

## <a name="next-steps"></a>További lépések
[Rendszergazdai kézikönyv](admin-handbook-overview.md)  
[A jelentéskészítő kiszolgáló termékkulcsának megkeresése](find-product-key.md)  
[A Power BI jelentéskészítő kiszolgáló telepítése](install-report-server.md)  
[A Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítése](install-powerbi-desktop.md)  
[A Power BI jelentéskészítő kiszolgáló böngészőtámogatása](browser-support.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

