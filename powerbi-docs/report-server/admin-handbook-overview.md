---
title: "A Power BI jelentéskészítő kiszolgáló rendszergazdai kézikönyvének áttekintése"
description: "Üdvözöljük a Power BI jelentéskészítő kiszolgáló rendszergazdai kézikönyvének olvasói között. A kiszolgáló a Power BI-, mobil- és több oldalas jelentések helyszíni tárolására és kezelésére szolgál."
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
ms.openlocfilehash: 6434084ab59cf842544dbcf9e373a8f6985a9ee3
ms.sourcegitcommit: eec6b47970bf69ed30638d1a20051f961ba792f2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/06/2018
---
# <a name="administrator-handbook-overview-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgáló rendszergazdai kézikönyvének áttekintése
Üdvözöljük a Power BI jelentéskészítő kiszolgáló rendszergazdai kézikönyvének olvasói között. A kiszolgáló a Power BI-, mobil- és több oldalas jelentések helyszíni tárolására és kezelésére szolgál.

![](media/admin-handbook-overview/admin-handbook.png)

Ez a kézikönyv segítséget nyújt a Power BI jelentéskészítő kiszolgáló tervezésére, üzembe helyezésére és kezelésére vonatkozó fogalmak megértésében.

## <a name="installing-and-migration"></a>Telepítés és migráció
A használatának megkezdéséhez telepítenie kell a Microsoft Power BI jelentéskészítő kiszolgálót. Elérhetők az információk ennek a feladatnak az elvégzéséhez.

Mielőtt elkezdené a Power BI jelentéskészítő kiszolgáló telepítését, a migrációt vagy arra frissítene, vessen egy pillantást a jelentéskészítő kiszolgáló [rendszerkövetelményeire](system-requirements.md).

### <a name="installing"></a>Telepítés
Ha egy új Power BI jelentéskészítő kiszolgálót helyez üzembe, ehhez a következő dokumentumok nyújtanak segítséget. Rendelkezésre áll a gyors üzembe helyezés az azonnali kezdéshez. Vagy, a részletes leírást megtalálja a telepítési dokumentumban.

* [Gyors üzembe helyezés: A Power BI jelentéskészítő kiszolgáló telepítése](quickstart-install-report-server.md)
* [A Power BI jelentéskészítő kiszolgáló telepítése](install-report-server.md)

### <a name="migration"></a>Migráció
Az SQL Server Reporting Serviceshez nem áll rendelkezésre helyben végzett verzióváltás. Ha egy meglévő SQL Server Reporting Services-példánnyal rendelkezik, amelyet Power BI jelentéskészítő kiszolgálóvá szeretne átalakítani, akkor azt migrálnia kell. Migrációra más okokból is szükség lehet. További részletekért tekintse át a migrációra vonatkozó dokumentumot.

[Telepített jelentéskészítő kiszolgáló migrálása](migrate-report-server.md)

## <a name="configuring-your-report-server"></a>A jelentéskészítő kiszolgáló beállítása
A jelentéskészítő kiszolgáló beállításakor számos lehetőség közül választhat. Használni fog SSL-t? E-mail-kiszolgálót konfigurál? Szeretne a Power BI szolgáltatással való integrációt létrehozni a vizualizációk kitűzéséhez?

A beállítások nagy részét a jelentéskészítő kiszolgáló konfigurációkezelőjében kell elvégeznie. További részletekért lásd a [konfigurációkezelő](https://docs.microsoft.com/sql/reporting-services/install-windows/reporting-services-configuration-manager-native-mode) dokumentációját.

## <a name="security"></a>Biztonság
A biztonság és a védelem minden cég számára fontos. A hitelesítésről, engedélyezésről, szerepkörökről és engedélyekről a [biztonsági](https://docs.microsoft.com/sql/reporting-services/security/reporting-services-security-and-protection) dokumentációban olvashat.

## <a name="next-steps"></a>Következő lépések
[Gyors üzembe helyezés: A Power BI jelentéskészítő kiszolgáló telepítése](quickstart-install-report-server.md)  
[A jelentéskészítő kiszolgáló termékkulcsának megkeresése](find-product-key.md)  
[A Power BI jelentéskészítő kiszolgálóra optimalizált Power BI Desktop telepítése](install-powerbi-desktop.md)  
[A Jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

