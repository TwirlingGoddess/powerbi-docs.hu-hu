---
title: Rendszergazdai áttekintés, Power BI jelentéskészítő kiszolgáló
description: Ez a cikk a Power BI jelentéskészítő kiszolgáló rendszergazdai áttekintését nyújtja. A kiszolgáló a Power BI-, mobil- és többoldalas jelentések helyszíni tárolására és kezelésére szolgál.
services: powerbi
documentationcenter: ''
author: markingmyname
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
ms.date: 05/07/2018
ms.author: maghan
ms.openlocfilehash: 52b2c9cac7fd07564480fdbf3a6a91e04e72db11
ms.sourcegitcommit: c29525cbac2e747edb4dd3a1841084bb0ce42582
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/08/2018
ms.locfileid: "33883089"
---
# <a name="admin-overview-power-bi-report-server"></a>Rendszergazdai áttekintés, Power BI jelentéskészítő kiszolgáló
Ez a cikk a Power BI jelentéskészítő kiszolgáló rendszergazdai áttekintését nyújtja. A kiszolgáló a Power BI-, mobil- és többoldalas jelentések helyszíni tárolására és kezelésére szolgál. A cikk bemutatja a Power BI jelentéskészítő kiszolgáló tervezésének, üzembe helyezésének és kezelésének alapelveit, és további információkra mutató hivatkozásokat is tartalmaz.

![](media/admin-handbook-overview/admin-handbook.png)



## <a name="installing-and-migration"></a>Telepítés és migráció
A használatának megkezdéséhez telepítenie kell a Microsoft Power BI jelentéskészítő kiszolgálót. Elérhetők az információk ennek a feladatnak az elvégzéséhez.

Mielőtt elkezdené a Power BI jelentéskészítő kiszolgáló telepítését, a migrációt vagy arra frissítene, vessen egy pillantást a jelentéskészítő kiszolgáló [rendszerkövetelményeire](system-requirements.md).

### <a name="installing"></a>Telepítés
Ha egy új Power BI jelentéskészítő kiszolgálót helyez üzembe, ehhez a következő dokumentum nyújt segítséget. 

[A Power BI jelentéskészítő kiszolgáló telepítése](install-report-server.md)

### <a name="migration"></a>Migráció
Az SQL Server Reporting Serviceshez nem áll rendelkezésre helyben végzett verzióváltás. Ha egy meglévő SQL Server Reporting Services-példánnyal rendelkezik, amelyet Power BI jelentéskészítő kiszolgálóvá szeretne átalakítani, akkor azt migrálnia kell. Migrációra más okokból is szükség lehet. További részletekért tekintse át a migrációra vonatkozó dokumentumot.

[Telepített jelentéskészítő kiszolgáló migrálása](migrate-report-server.md)

## <a name="configuring-your-report-server"></a>A jelentéskészítő kiszolgáló beállítása
A jelentéskészítő kiszolgáló beállításakor számos lehetőség közül választhat. Használni fog SSL-t? E-mail-kiszolgálót konfigurál? Szeretne a Power BI szolgáltatással való integrációt létrehozni a vizualizációk kitűzéséhez?

A beállítások nagy részét a jelentéskészítő kiszolgáló konfigurációkezelőjében kell elvégeznie. További részletekért lásd a [konfigurációkezelő](https://docs.microsoft.com/sql/reporting-services/install-windows/reporting-services-configuration-manager-native-mode) dokumentációját.

## <a name="security"></a>Biztonság
A biztonság és a védelem minden cég számára fontos. A hitelesítésről, engedélyezésről, szerepkörökről és engedélyekről a [biztonsági](https://docs.microsoft.com/sql/reporting-services/security/reporting-services-security-and-protection) dokumentációban olvashat.

## <a name="next-steps"></a>Következő lépések
[A Power BI jelentéskészítő kiszolgáló telepítése](install-report-server.md)  
[A jelentéskészítő kiszolgáló termékkulcsának megkeresése](find-product-key.md)  
[A Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítése](install-powerbi-desktop.md)  
[A Jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

