---
title: "A DirectQuery által támogatott adatforrások a Power BI-ban"
description: "A DirectQuery használatát támogató adatforrások listája."
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
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/24/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 3630d876f3e32cbe981d7fb5bcc38d9da1a257f2
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="data-sources-supported-by-directquery-in-power-bi"></a>A DirectQuery által támogatott adatforrások a Power BI-ban
A **Power BI Desktopban** és a **Power BI szolgáltatásban** számos adatforráshoz csatlakozhat, és hozzáférhet ezek adataihoz. Ez a cikk azt ismerteti, hogy a Power BI mely adatforrásai támogatják a **DirectQuery** néven ismert kapcsolódási módszert. További, a DirectQueryre vonatkozó információkért lásd [**a DirectQuery Power BI-ban történő használatát**](desktop-directquery-about.md) ismertető cikket.

A következő adatforrások támogatják a DirectQueryt a Power BI-ban:

* Amazon Redshift
* Azure HDInsight Spark (bétaverzió)
* Azure SQL Database
* Azure SQL Data Warehouse
* Google BigQuery (bétaverzió)
* IBM Netezza (bétaverzió)
* Impala (2.x-es verzió)
* Oracle Database (12-es és újabb verzió)
* SAP Business Warehouse (bétaverzió)
* SAP HANA
* Snowflake
* Spark (bétaverzió) (0.9-es és újabb)
* SQL Server
* Teradata-adatbázis
* Vertica (bétaverzió)

Azok az adatforrások, amelyek mögött szerepel a **(bétaverzió)** vagy az **(előzetes verzió)**, módosulhatnak, és a használatuk éles környezetben nem támogatott. Az is előfordulhat, hogy akkor sem támogatottak, miután közzétett egy jelentést a **Power BI szolgáltatásban**, és ezért egy közzétett jelentés megnyitása vagy az adatkészlet felderítése hibát okozhat.

Az egyetlen különbség a **(bétaverzió)** és az **(előzetes verzió)** kifejezéssel jelölt adatforrások között, hogy az **(előzetes verziójú)** forrásokat engedélyezni kell Előzetes verziójú funkcióként, mielőtt használni lehetne őket. Egy **(előzetes verziójú)** adatösszekötő engedélyezéséhez lépjen a **Fájl > Lehetőségek és beállítások**, majd a **Beállítások > Beállítások > Előzetes verziójú funkciók** elemhez a **Power BI Desktopban**.

## <a name="on-premises-gateway-requirements"></a>Helyszíni átjáróra vonatkozó követelmények
Az alábbi tábla meghatározza, hogy szükség van-e **helyszíni adatátjáróra** az adott adatforráshoz való csatlakozáshoz, miután közzétett egy jelentést a **Power BI szolgáltatásban**.

| Forrás | Szükség van átjáróra? |
| --- | --- |
| SQL Server |Igen |
| Azure SQL Database |Nem |
| Azure SQL Data Warehouse |Nem |
| SAP HANA |Igen |
| Oracle Database |Igen |
| Teradata-adatbázis |Igen |
| Amazon Redshift |Nem |
| Impala (2.x-es verzió) |Igen |
| Snowflake (előzetes verzió) |Még nem támogatott a **Power BI szolgáltatásban** |
| Spark (bétaverzió) (0.9-es és újabb) |Még nem támogatott a **Power BI szolgáltatásban** |
| Azure HDInsight Spark (bétaverzió) |Még nem támogatott a **Power BI szolgáltatásban** |
| IBM Netezza (bétaverzió) |Még nem támogatott a **Power BI szolgáltatásban** |
| SAP Buisness Warehouse (bétaverzió) |Még nem támogatott a **Power BI szolgáltatásban** |

## <a name="next-steps"></a>Következő lépések
Ha többet szeretne megtudni a DirectQueryről, tekintse át a következő forrásanyagokat:

* [A DirectQuery használata a Power BI-ban](desktop-directquery-about.md)
* [A DirectQuery és az SAP HANA](desktop-directquery-sap-hana.md)
* [A DirectQuery és az SAP BW](desktop-directquery-sap-bw.md)
* [Helyszíni adatátjáró](service-gateway-onprem.md)

