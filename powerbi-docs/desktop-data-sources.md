---
title: "Adatforrások a Power BI Desktopban"
description: "Adatforrások a Power BI Desktopban"
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: complete
qualitydate: 04/29/2016
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/24/2018
ms.author: davidi
ms.openlocfilehash: 42acbc0823f798ee0c0d762fc124c0f371494bd9
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/25/2018
---
# <a name="data-sources-in-power-bi-desktop"></a>Adatforrások a Power BI Desktopban
A Power BI Desktoppal különböző forrásokból származó adatokhoz csatlakozhat. Az elérhető adatforrások teljes listája az oldal alján látható.

Az adatokhoz való csatlakozáshoz válassza a **Kezdőlap** menüszalag **Lekérdezés** lehetőségét. A lefelé mutató nyíl vagy a gomb **Lekérdezés** feliratának kiválasztásával megjelenik a **Leggyakoribb** adattípusok menüje, ahogyan az a következő képen látható.

![](media/desktop-data-sources/data-sources_1.png)

A **Továbbiak...** lehetőség a **Leggyakoribb** menüből való kiválasztásakor megjelenik a **Lekérdezés** ablak. A **Lekérdezés** ablakot (a **Leggyakoribb** menü kihagyásával) a **Lekérdezés** **ikongomb** közvetlen kiválasztásával is megjelenítheti.

![](media/desktop-data-sources/data-sources_2.png)

> [!NOTE]
> A Power BI csapata folyamatosan bővíti a **Power BI Desktop** és a **Power BI szolgáltatás** számára elérhető adatforrásokat. Ezért gyakran láthatja majd a fejlesztés alatt álló adatforrások előzetes verzióit *bétaverzió* vagy *előzetes verzió* felirattal. A *bétaverzió* vagy *előzetes verzió* felirattal ellátott adatforrások támogatása és működése korlátozott, használatuk éles környezetben nem ajánlott.
> 
> 

## <a name="data-sources"></a>Adatforrások
Az adattípusok a következő kategóriákba vannak csoportosítva:

* Összes
* Fájl
* Adatbázis
* Azure
* Online szolgáltatások
* Egyéb

A **Mind** kategória az összes kategóriába tartozó adatkapcsolat-típusokat tartalmazza.

A **Fájl** kategória a következő adatkapcsolatokat biztosítja:

* Excel
* Szöveg/CSV
* XML
* JSON
* Mappa
* SharePoint-mappa

A következő képen a **Lekérdezés** ablak látható, amelyen a **Fájl** kategória ki van választva.

![](media/desktop-data-sources/data-sources_3.png)

> [!NOTE]
> A Power BI Desktop korábbi verzióiban a **CSV** és a **Szöveg** külön adatkapcsolat-típusnak számított. Ezek az adatösszekötők mostantól együtt alkotják a **CSV/Szöveg** kategóriát.
> 
> 

Az **Adatbázis** kategória a következő adatkapcsolatokat biztosítja:

* SQL Server-adatbázis
* Access-adatbázis
* SQL Server Analysis Services-adatbázis
* Oracle Database
* IBM DB2-adatbázis
* IBM Informix-adatbázis (bétaverzió)
* IBM Netezza (bétaverzió)
* MySQL-adatbázis
* PostgreSQL-adatbázis
* Sybase-adatbázis
* Teradata-adatbázis
* SAP HANA-adatbázis
* SAP Business Warehouse-kiszolgáló
* Amazon Redshift
* Impala
* Google BigQuery (bétaverzió)
* Snowflake

> [!NOTE]
> Egyes adatbázis-összekötőket engedélyezni kell a **Fájl > Lehetőségek és beállítások > Beállítások** elem, majd az **Előzetes verziójú funkciók** lehetőség kiválasztásával és az adott összekötő engedélyezésével. Ha a fentiekben említett összekötők nem jelennek meg itt, és használni kívánja őket, ellenőrizze az **Előzetes verziójú funkciók** beállításait. Vegye figyelembe azt is, hogy a *bétaverzió* vagy *előzetes verzió* felirattal ellátott adatforrások támogatása és működése korlátozott, használatuk éles környezetben nem ajánlott.
> 
> 

A következő képen a **Lekérdezés** ablak látható, amelyen az **Adatbázis** kategória ki van választva.

![](media/desktop-data-sources/data-sources_4.png)

Az **Azure** kategória a következő adatkapcsolatokat biztosítja:

* Azure SQL Database
* Azure SQL Data Warehouse
* Azure Analysis Services-adatbázis (bétaverzió)
* Azure Blob-tároló
* Azure Table Storage
* Azure Cosmos DB (bétaverzió)
* Azure Data Lake Store
* Azure HDInsight (HDFS)
* Azure HDInsight Spark (bétaverzió)

A következő képen a **Lekérdezés** ablak látható, amelyen az **Azure** kategória ki van választva.

![](media/desktop-data-sources/data-sources_5.png)

Az **Online szolgáltatások** kategória a következő adatkapcsolatokat biztosítja:

* Power BI szolgáltatás
* SharePoint Online-lista
* Microsoft Exchange Online
* Dynamics 365 (online)
* Dynamics 365 for Financials (bétaverzió)
* Common Data Service (bétaverzió)
* Microsoft Azure – használati elemzés (bétaverzió)
* Visual Studio Team Services (bétaverzió)
* Salesforce-objektumok
* Salesforce-jelentések
* Google Analytics
* appFigures (bétaverzió)
* comScore Digital Analytix (bétaverzió)
* Dynamics 365 for Customer Insights (bétaverzió)
* Facebook
* GitHub (bétaverzió)
* Kusto (bétaverzió)
* MailChimp (bétaverzió)
* Mixpanel (bétaverzió)
* Planview Enterprise (bétaverzió)
* Projectplace (bétaverzió)
* QuickBooks Online (bétaverzió)
* Smartsheet
* SparkPost (bétaverzió)
* SQL Sentry (bétaverzió)
* Stripe (bétaverzió)
* SweetIQ (bétaverzió)
* Troux (bétaverzió)
* Twilio (bétaverzió)
* tyGraph (bétaverzió)
* Webtrends (bétaverzió)
* Zendesk (bétaverzió)

A következő képen a **Lekérdezés** ablak látható, amelyen az **Online szolgáltatások** kategória ki van választva.

![](media/desktop-data-sources/data-sources_6b.png)

Az **Egyéb** kategória a következő adatkapcsolatokat biztosítja:

* Vertica (bétaverzió)
* Web
* SharePoint-lista
* OData-adatcsatorna
* Active Directory
* Microsoft Exchange
* Hadoop-fájl (HDFS)
* Spark (bétaverzió)
* R-szkript
* ODBC
* OLE DB
* Üres lekérdezés

A következő képen a **Lekérdezés** ablak látható, amelyen az **Egyéb** kategória ki van választva.

![](media/desktop-data-sources/data-sources_7a.png)

> [!NOTE]
> Jelenleg nem lehetséges olyan egyéni adatforrásokhoz csatlakozni, amelyek védelmét az Azure Active Directory biztosítja.
> 
> 

## <a name="connecting-to-a-data-source"></a>Csatlakozás adatforráshoz
Egy adott adatforráshoz való csatlakozáshoz válassza ki azt a **Lekérdezés** ablakban, majd válassza a **Kapcsolódás** lehetőséget. A következő képen a **Web** lehetőség van kiválasztva az **Egyéb** adatkapcsolat-kategórián belül.

![](media/desktop-data-sources/data-sources_7b.png)

Ekkor megjelenik egy, az adott adatkapcsolatra jellemző csatlakozási ablak. Ha hitelesítő adatok szükségesek, a rendszer ezek megadására kéri. A következő képen a Web típusú adatforráshoz való csatlakozáshoz szükséges URL-cím megadása látható.

![](media/desktop-data-sources/datasources_fromwebbox.png)

Az URL-cím vagy az erőforrás csatlakozási adatainak megadása után kattintson az **OK** gombra. A Power BI Desktop csatlakozik az adatforráshoz, és megjeleníti az elérhető adatforrásokat a **Kezelőben**.

![](media/desktop-data-sources/datasources_fromnavigatordialog.png)

Az adatokat betöltheti a **Kezelő** panel alján található **Betöltés** gombbal, vagy szerkesztheti a lekérdezést az adatok betöltése előtt a **Szerkesztés** gombbal.

Ilyen egyszerűen csatlakozhat adatforrásokhoz a Power BI Desktopban. Egyre több adatforrás közül választhat, és a lista folyamatosan bővül, ezért érdemes gyakran visszatérnie.

## <a name="next-steps"></a>Következő lépések
A Power BI Desktop műveletek és lehetőségek széles tárházát tartalmazza. A program képességeivel kapcsolatos további információkért lásd az alábbi forrásanyagokat:

* [Első lépések a Power BI Desktopban](desktop-getting-started.md)
* [Lekérdezések áttekintése a Power BI Desktopban](desktop-query-overview.md)
* [Adattípusok a Power BI Desktopban](desktop-data-types.md)
* [Adatok formázása és kombinálása a Power BI Desktoppal](desktop-shape-and-combine-data.md)
* [Gyakori lekérdezési feladatok a Power BI Desktopban](desktop-common-query-tasks.md)    

