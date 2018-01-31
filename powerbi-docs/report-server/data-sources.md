---
title: "A Power BI-jelentések adatforrásai a Power BI jelentéskészítő kiszolgálón"
description: "A Power BI-jelentések különféle adatforrásokhoz csatlakozhatnak. Az adatok használatának módjától függően eltérő adatforrások érhetők el."
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.openlocfilehash: caa45aab2c31974abb041a82eb2216ebee2eb148
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/30/2018
---
# <a name="power-bi-report-data-sources-in-power-bi-report-server"></a>A Power BI-jelentések adatforrásai a Power BI jelentéskészítő kiszolgálón
A Power BI-jelentések különféle adatforrásokhoz csatlakozhatnak. Az adatok használatának módjától függően eltérő adatforrások érhetők el. Az adatok importálhatók, vagy közvetlenül DirectQuery- vagy élő SQL Server Analysis Services-kapcsolattal lehet lekérdezni azokat.

Ezek az adatforrások a Power BI jelentéskészítő kiszolgálón használt adott Power BI-jelentésekkel kapcsolatosak. A többoldalas jelentésekben támogatott adatforrásokra vonatkozó információkért lásd: [A Reporting Services által támogatott adatforrások](https://docs.microsoft.com/sql/reporting-services/report-data/data-sources-supported-by-reporting-services-ssrs).

> [!IMPORTANT]
> A Power BI Desktop-jelentésben szereplő összes adatforrásnak támogatottnak kell lennie az ütemezett frissítés konfigurálásához.
> 
> 

## <a name="list-of-supported-data-sources"></a>Támogatott adatforrások listája
Más adatforrások is működhetnek annak ellenére, hogy a támogatott listán nem szerepelnek.

| **Adatforrás** | **Gyorsítótárban lévő adatok** | **Ütemezett frissítés** | **Élő lekérdezés/DirectQuery** |
| --- | --- | --- | --- |
| SQL Server-adatbázis |Igen |Igen |Igen |
| SQL Server Analysis Services |Igen |Igen |Igen |
| Azure SQL Database |Igen |Igen |Igen |
| Azure SQL Data Warehouse |Igen |Igen |Igen |
| Excel |Igen |Igen |Nem |
| Hozzáférés az adatbázishoz |Igen |Igen |Nem |
| Active Directory |Igen |Igen |Nem |
| Amazon Redshift |Igen |Nem |Nem |
| Azure Blob Storage |Igen |Igen |Nem |
| Azure Data Lake Store |Igen |Nem |Nem |
| Azure HDInsight (HDFS) |Igen |Igen |Nem |
| Azure HDInsight (HDFS) |Igen |Igen |Nem |
| Azure Table Storage |Igen |Igen |Nem |
| Dynamics 365 (online) |Igen |Nem |Nem |
| Facebook |Igen |Nem |Nem |
| Mappa |Igen |Igen |Nem |
| Google Analytics |Igen |Nem |Nem |
| Hadoop-fájl (HDFS) |Igen |Nem |Nem |
| IBM DB2-adatbázis |Igen |Igen |Nem |
| Impala |Igen |Nem |Nem |
| JSON |Igen |Igen |Nem |
| Microsoft Exchange |Igen |Nem |Nem |
| Microsoft Exchange Online |Igen |Nem |Nem |
| MySQL-adatbázis |Igen |Igen |Nem |
| OData-csatorna |Igen |Igen |Nem |
| ODBC |Igen |Igen |Nem |
| OLE DB |Igen |Igen |Nem |
| Oracle Database |Igen |Igen |Igen |
| PostgreSQL-adatbázis |Igen |Igen |Nem |
| Power BI szolgáltatás |Nem |Nem |Nem |
| R szkript |Igen |Nem |Nem |
| Salesforce-objektumok |Igen |Nem |Nem |
| Salesforce-jelentések |Igen |Nem |Nem |
| SAP Business Warehouse-kiszolgáló |Igen |Igen |Igen |
| SAP HANA-adatbázis |Igen |Igen |Igen |
| SharePoint-mappa (helyszíni) |Igen |Igen |Nem |
| SharePoint-lista (helyszíni) |Igen |Igen |Nem |
| SharePoint Online-lista |Igen |Nem |Nem |
| Snowflake |Igen |Nem |Nem |
| Sybase-adatbázis |Igen |Igen |Nem |
| Teradata-adatbázis |Igen |Igen |Igen |
| Szöveges/CSV |Igen |Igen |Nem |
| Webes |Igen |Igen |Nem |
| XML |Igen |Igen |Nem |
| appFigures (bétaverzió) |Igen |Nem |Nem |
| Azure Analysis Services-adatbázis (bétaverzió) |Igen |Nem |Nem |
| Azure Cosmos DB (bétaverzió) |Igen |Nem |Nem |
| Azure HDInsight Spark (bétaverzió) |Igen |Nem |Nem |
| Common Data Service (bétaverzió) |Igen |Nem |Nem |
| comScore Digital Analytix (bétaverzió) |Igen |Nem |Nem |
| Dynamics 365 for Customer Insights (bétaverzió) |Igen |Nem |Nem |
| Dynamics 365 for Financials (bétaverzió) |Igen |Nem |Nem |
| GitHub (bétaverzió) |Igen |Nem |Nem |
| Google BigQuery (bétaverzió) |Igen |Nem |Nem |
| IBM Informix-adatbázis (bétaverzió) |Igen |Nem |Nem |
| IBM Netezza (bétaverzió) |Igen |Nem |Nem |
| Kusto (bétaverzió) |Igen |Nem |Nem |
| MailChimp (bétaverzió) |Igen |Nem |Nem |
| Microsoft Azure Consumption Insights (bétaverzió) |Igen |Nem |Nem |
| Mixpanel (bétaverzió) |Igen |Nem |Nem |
| Planview Enterprise (bétaverzió) |Igen |Nem |Nem |
| Projectplace (bétaverzió) |Igen |Nem |Nem |
| QuickBooks Online (bétaverzió) |Igen |Nem |Nem |
| Smartsheet |Igen |Nem |Nem |
| Spark (bétaverzió) |Igen |Nem |Nem |
| SparkPost (bétaverzió) |Igen |Nem |Nem |
| SQL Sentry (bétaverzió) |Igen |Nem |Nem |
| Stripe (bétaverzió) |Igen |Nem |Nem |
| SweetIQ (bétaverzió) |Igen |Nem |Nem |
| Troux (bétaverzió) |Igen |Nem |Nem |
| Twilio (bétaverzió) |Igen |Nem |Nem |
| tyGraph (bétaverzió) |Igen |Nem |Nem |
| Vertica (bétaverzió) |Igen |Nem |Nem |
| Visual Studio Team Services (bétaverzió) |Igen |Nem |Nem |
| Webtrends (bétaverzió) |Igen |Nem |Nem |
| Zendesk (bétaverzió) |Igen |Nem |Nem |

> [!IMPORTANT]
> Az adatforrásnál konfigurált sorszintű biztonság működik egyes DirectQuery- (SQL Server, az Azure SQL Database, Oracle és Teradata) és élő kapcsolatokkal, feltéve, hogy a Kerberos megfelelően van konfigurálva a környezetben.
> 
> 

## <a name="next-steps"></a>Következő lépések
Most, hogy kiválasztotta az adatforrást, az abból származó adatokat használva [hozzon létre egy jelentést](quickstart-create-powerbi-report.md).

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

