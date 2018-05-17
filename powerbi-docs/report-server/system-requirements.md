---
title: A Power BI jelentéskészítő kiszolgáló telepítésének hardver- és szoftverkövetelményei
description: Itt láthatók a Power BI jelentéskészítő kiszolgáló telepítésének és futtatásának minimális hardver- és szoftverkövetelményei.
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
ms.date: 11/01/2017
ms.author: maghan
ms.openlocfilehash: 26710c6a19ea4f9389718bea51ffff82dfadd3eb
ms.sourcegitcommit: 493f160d04ed411ff4741c599adc63ba1f65230f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/07/2018
---
# <a name="hardware-and-software-requirements-for-installing-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgáló telepítésének hardver- és szoftverkövetelményei
Itt láthatók a Power BI jelentéskészítő kiszolgáló telepítésének és futtatásának minimális hardver- és szoftverkövetelményei.

## <a name="processor-memory-and-operating-system-requirements"></a>Processzorra, memóriára és operációs rendszerre vonatkozó követelmények
| Összetevő | Követelmény |
| --- | --- |
| NET-keretrendszer |4.6<br><br>A .NET-keretrendszert [A Windowshoz készült Microsoft .NET-keretrendszert 4.6-os verziója (webes telepítő)](http://support.microsoft.com/kb/3045560) című cikkből telepítheti manuálisan.<br/><br/> A .NET-keretrendszerrel kapcsolatos további információkért, ajánlásokért és útmutatókért tekintse meg [A .NET-keretrendszer 4.6-os verziójának üzembe helyezési útmutatója fejlesztőknek](http://msdn.microsoft.com/library/ee942965\(v=vs.110\).aspx) című cikket.<br/><br/>Windows 8.1 és Windows Server 2012 R2 rendszereken telepítenie kell a [KB2919355](http://support.microsoft.com/kb/2919355) frissítést a .NET-keretrendszer 4.6-os verziójának telepítése előtt. |
| Merevlemez |A Power BI jelentéskészítő kiszolgáló működéséhez legalább 1 GB szabad lemezterület szükséges.<br><br>További lemezterület szükséges a jelentéskészítő kiszolgáló adatbázisát üzemeltető adatbázis-kiszolgálón. |
| Memória |**Minimum:** 1 GB<br/><br/> **Ajánlott:** legalább 4 GB |
| Processzor sebessége |**Minimum:** x64 processzor: 1,4 GHz<br/><br/> **Ajánlott:** 2,0 GHz vagy gyorsabb |
| Processzor típusa |64 bites processzor: AMD Opteron, AMD Athlon 64, Intel Xeon Intel EM64T-támogatással, Intel Pentium IV EM64T-támogatással |
| Operációs rendszer |Windows Server 2016 Datacenter<br><br>Windows Server 2016 Standard<br><br>Windows Server 2012 R2 Datacenter<br><br>Windows Server 2012 R2 Standard<br><br>Windows Server 2012 R2 Essentials<br><br>Windows Server 2012 R2 Foundation<br><br>Windows Server 2012 Datacenter<br><br>Windows Server 2012 Standard<br><br>Windows Server 2012 Essentials<br><br>Windows Server 2012 Foundation<br><br>Windows 10 Home<br><br>Windows 10 Professional<br><br>Windows 10 Enterprise<br><br>Windows 8.1<br><br>Windows 8.1 Pro<br><br>Windows 8.1 Enterprise<br><br>Windows 8<br><br>Windows 8 Pro<br><br>Windows 8 Enterprise |

> [!NOTE]
> A Power BI jelentéskészítő kiszolgáló telepítése csak 64 bites processzorok esetén támogatott.
> 
> 

## <a name="database-server-version-requirements"></a>Az adatbázis-kiszolgáló verziójával kapcsolatos követelmények
A jelentéskészítő kiszolgáló adatbázisának üzemeltetése SQL Serveren történik. Az SQL Server adatbázismotor-példánya helyi vagy távoli példány lehet. A jelentéskészítő kiszolgáló adatbázisának üzemeltetését a következő verziójú SQL Server-adatbázismotorok támogatják:

* SQL Server 2017
* SQL Server 2016
* SQL Server 2014
* SQL Server 2012
* SQL Server 2008 R2
* SQL Server 2008

Ha a jelentéskészítő kiszolgáló adatbázisát egy távoli számítógépen szeretné létrehozni, akkor a kapcsolódáshoz egy tartományi felhasználó fiókja vagy pedig egy hálózati hozzáféréssel rendelkező szolgáltatási fiók szükséges. Ha úgy dönt, hogy egy távoli SQL Server-példányt használ, fontolja meg alaposan, hogy a jelentéskészítő kiszolgáló mely hitelesítő adatokkal kapcsolódjon az SQL Server-példányhoz. További információkért tekintse meg a [Jelentéskészítő kiszolgáló adatbázis-kapcsolatának konfigurációja](https://docs.microsoft.com/sql/reporting-services/install-windows/configure-a-report-server-database-connection-ssrs-configuration-manager) című cikket.

## <a name="considerations"></a>Megfontolandó szempontok
A Power BI jelentéskészítő kiszolgáló az alapvető beállításokat a működéséhez szükséges alapértelmezett értékekkel telepíti. Ehhez a következő követelményeknek kell teljesülniük:

* Rendelkezésre kell állnia egy SQL Server adatbázismotornak a jelentéskészítő kiszolgáló telepítése után, de még a jelentéskészítő kiszolgáló adatbázisának konfigurációja előtt. A jelentéskészítő kiszolgáló adatbázisát, amelyet a Reporting Services konfigurációkezelő fog létrehozni, az adatbázismotor-példány üzemelteti. A tényleges telepítési felületen nem szükséges az adatbázismotor megadása.
* A telepítés futtatásához használt felhasználói fiók tagja kell hogy legyen a helyi Rendszergazdák csoportnak.
* A Reporting Services konfigurációkezelőhöz használt felhasználói fióknak engedéllyel kell rendelkeznie adatbázisok létrehozásához és az adatbázisokhoz történő hozzáféréshez a jelentéskészítő kiszolgáló adatbázisát üzemeltető adatbázismotor-példányon.
* A telepítésnek működnie kell az alapértelmezett értékekkel, hogy bejegyezhesse a jelentéskészítő kiszolgáló és a webes portál elérését biztosító URL-címeket. Ezek az értékek a 80-as port, egy erős helyettesítő, és a **ReportServer** és **Reports** formátumú virtuális könyvtárnevek.

## <a name="read-only-domain-controller-rodc"></a>Írásvédett tartományvezérlő (RODC)
 A jelentéskészítő kiszolgálót csak egy írásvédett tartományvezérlővel (RODC-vel) rendelkező környezetben telepítheti, a Reporting Servicesnek azonban a megfelelő működés érdekében hozzáféréssel kell rendelkeznie egy írható tartományvezérlőhöz. Ha a Reporting Services csak egy írásvédett tartományvezérlőhöz (RODC-hez) fér hozzá, akkor a szolgáltatás adminisztrálása során hibákat tapasztalhat.

## <a name="power-bi-reports-and-analysis-services-live-connections"></a>Power BI-jelentések és az Analysis Services élő kapcsolatai
Élő kapcsolatokat táblázatos vagy többdimenziós példányokhoz használhat. A megfelelő működéshez megfelelő verziójú és kiadású Analysis Services-kiszolgáló szükséges.

| **Kiszolgáló verziója** | **Kötelező termékváltozat** |
| --- | --- |
| 2012 SP1 CU4 vagy újabb |Business Intelligence és Enterprise termékváltozat |
| 2014 |Business Intelligence és Enterprise termékváltozatok |
| 2016 vagy újabb |Standard vagy magasabb szintű termékváltozat |

## <a name="next-steps"></a>Következő lépések
[Felhasználói kézikönyv](user-handbook-overview.md)  
[Rendszergazdai kézikönyv](admin-handbook-overview.md)  
[A Power BI jelentéskészítő kiszolgáló telepítése](install-report-server.md)  
[A Jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

