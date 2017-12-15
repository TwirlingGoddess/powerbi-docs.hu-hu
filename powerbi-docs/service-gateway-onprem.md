---
title: "Helyszíni adatátjáró"
description: "Ez egy áttekintés a Power BI-hoz készült helyszíni adatátjáróhoz. Ezt az átjárót használhatja DirectQuery-adatforrásokon történő munkához. Helyszíni adatokkal rendelkező felhőbeli adatkészletek frissítésére is használhatja ezt az átjárót."
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 11/27/2017
ms.author: davidi
ms.openlocfilehash: 4693349715e7a38ae936318e9a8750e0b2f3fab0
ms.sourcegitcommit: 7742f952c20695dfb475f74965c0065b02c01521
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/29/2017
---
# <a name="on-premises-data-gateway"></a>Helyszíni adatátjáró
A helyszíni adatátjárók hídként működnek, és gyors és biztonságos adatátvitelt biztosítanak a helyszíni (nem a felhőben található) adatok és a Power BI, a Microsoft Flow, a Logic Apps és a PowerApps szolgáltatások között.

Egy átjárót egyszerre több szolgáltatással is használhat. Ha Power BI-t és PowerAppset is használ, használhatja mindkettőhöz ugyanazt az átjárót. Ez a bejelentkezéshez használt fióktól függ.

> [!NOTE]
> A helyszíni adatátjárók adattömörítést és átviteltitkosítást végeznek minden módban.
> 
> 

<!-- Shared Requirements Include -->
[!INCLUDE [gateway-onprem-requirements-include](./includes/gateway-onprem-requirements-include.md)]

### <a name="limitations-of-analysis-services-live-connections"></a>Az Analysis Services élő kapcsolatainak korlátozásai
Élő kapcsolatokat táblázatos vagy többdimenziós példányokhoz használhat.

| **Kiszolgáló verziója** | **Szükséges termékváltozat** |
| --- | --- |
| 2012 SP1 CU4 vagy újabb |Business Intelligence és Enterprise termékváltozatok |
| 2014 |Business Intelligence és Enterprise termékváltozatok |
| 2016 |Standard vagy magasabb szintű termékváltozat |

* Cellaszintű formázási és fordítási funkciók nem támogatottak.
* Műveletek és elnevezett készletek nem érhetők el a Power BI számára, de kapcsolódhat műveleteket és elnevezett készleteket is tartalmazó többdimenziós kockákhoz, és létrehozhat vizualizációkat és jelentéseket.

<!-- Shared Install steps Include -->
[!INCLUDE [gateway-onprem-datasources-include](./includes/gateway-onprem-datasources-include.md)]

## <a name="download-and-install-the-on-premises-data-gateway"></a>Helyszíni adatátjáró letöltése és telepítése
Az átjáró letöltéséhez válassza a Letöltés menü alatt található **Data Gateway** (Adatátjáró) lehetőséget. Töltse le a [helyszíni adatátjárót](http://go.microsoft.com/fwlink/?LinkID=820925).

![](media/service-gateway-onprem/powerbi-download-data-gateway.png)

<!-- Shared Install steps Include -->
[!INCLUDE [gateway-onprem-install-include](./includes/gateway-onprem-install-include.md)]

## <a name="install-the-gateway-in-personal-mode"></a>Átjáró telepítése személyes módban
> [!NOTE]
> A személyes mód csak a Power BI-jal fog működni.
> 
> 

A személyes átjáró telepítése után indítsa el a **Power BI Gateway – Personal beállítási varázslót**.

![](media/service-gateway-onprem/personal-gateway-launch-configuration.png)

Ezután jelentkezzen be a Power BI-ba, hogy regisztrálja az átjárót a felhőszolgáltatáshoz.

![](media/service-gateway-onprem/personal-gateway-signin.png)

A Windows-szolgáltatást futtató Windows-felhasználó felhasználónevét és jelszavát is adja meg. Nem kötelező a saját Windows-fiókját megadnia. Az átjáró szolgáltatást ez a felhasználói fiók fogja futtatni.

![](media/service-gateway-onprem/personal-gateway-windows-service.png)

A telepítés befejezését követően, nyissa meg a Power BI-ban az adatkészletek részt, hogy meggyőződjön arról, hogy adott meg hitelesítési adatokat a helyszíni adatforrásaihoz.

<a name="credentials"></a>

## <a name="storing-encrypted-credentials-in-the-cloud"></a>Titkosított hitelesítő adatok felhőbeli tárolása
Amikor hozzáad egy adatforrást az átjáróhoz, meg kell adnia az adatforrás hitelesítő adatait. Az adatforrás felé irányuló összes lekérdezés ezeket a hitelesítő adatokat fogja használni. A hitelesítő adatok titkosítása egy biztonságos aszimmetrikus titkosítással még a felhőbe kerülésük előtt megtörténik, így az adatokat a felhőben nem lehet visszafejteni. Amikor az adatforráshoz hozzáférnek, a hitelesítő adatok visszafejtését a helyszíni átjárót futtató számítógép végzi.

<!-- Account and Port information -->
[!INCLUDE [gateway-onprem-accounts-ports-more](./includes/gateway-onprem-accounts-ports-more.md)]

<!-- How the gateway works -->
[!INCLUDE [gateway-onprem-how-it-works-include](./includes/gateway-onprem-how-it-works-include.md)]

## <a name="troubleshooting"></a>Hibaelhárítás
Ha problémába ütközik az átjáró telepítése vagy konfigurálása során, tekintse meg a [Helyszíni adatátjárók hibaelhárítása](service-gateway-onprem-tshoot.md) című cikket. Ha úgy gondolja, hogy a probléma a tűzfalával kapcsolatos, tekintse meg a hibaelhárítási cikk [tűzfal vagy proxy](service-gateway-onprem-tshoot.md#firewall-or-proxy) szakaszát.

Ha úgy gondolja, hogy proxyval kapcsolatos problémákba ütközött, tekintse meg a [Proxybeállítások konfigurálása Power BI-átjárókhoz](service-gateway-proxy.md) című cikket.

## <a name="next-steps"></a>Következő lépések
[Adatforrások kezelése – Analysis Services](service-gateway-enterprise-manage-ssas.md)  
[Adatforrások kezelése – SAP HANA](service-gateway-enterprise-manage-sap.md)  
[Adatforrások kezelése – SQL Server](service-gateway-enterprise-manage-sql.md)  
[Adatforrások kezelése – Oracle](service-gateway-onprem-manage-oracle.md)  
[Adatforrások kezelése – Importálás és ütemezett frissítés](service-gateway-enterprise-manage-scheduled-refresh.md)  
[Helyszíni adatátjáró – részletes](service-gateway-onprem-indepth.md)  
[Helyszíni adatátjáró (személyes mód) – a személyes átjáró új verziója](service-gateway-personal-mode.md)
[Helyszíni adatátjáró proxybeállításainak konfigurálása](service-gateway-proxy.md)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

