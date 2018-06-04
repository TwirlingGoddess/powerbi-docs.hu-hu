---
title: SQL Database Auditing tartalomcsomag
description: SQL Database Auditing tartalomcsomag a Power BI-hoz
author: SarinaJoan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/10/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 36351491f7cb99a2e597ef4fd498ef7c38da386e
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34243891"
---
# <a name="sql-database-auditing-content-pack-for-power-bi"></a>SQL Database Auditing tartalomcsomag a Power BI-hoz
Az Azure [SQL Database naplózási szolgáltatásához](http://azure.microsoft.com/documentation/articles/sql-database-auditing-get-started/) készült Power BI-tartalomcsomag segít megérteni az adatbázisban zajló tevékenységet, valamint felismerni azokat az ellentmondásokat és anomáliákat, amelyek üzleti aggályokra adhatnak okot, vagy biztonsági szabálysértések gyanúját vethetik fel. 

Kapcsolódjon a Power BI-hoz készült [SQL Database Auditing tartalomcsomaghoz](https://app.powerbi.com/getdata/services/sql-db-auditing).

>[!NOTE]
>A tartalomcsomag importálja minden olyan táblából az adatokat, amelynek a nevében szerepel az „AuditLogs” kifejezés, és hozzáfűzi egyetlen adatmodelltáblához, amelynek „AuditLogs” a neve. Az adatok a legutóbbi 250 ezer eseményt tartalmazzák, és naponta frissülnek.

## <a name="how-to-connect"></a>A kapcsolódás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs panel alján.
   
   ![](media/service-connect-to-azure-sql-database-auditing/pbi_getdata.png) 
2. Válassza a Szolgáltatások terület Beolvasás gombját.
   
   ![](media/service-connect-to-azure-sql-database-auditing/pbi_getservices.png) 
3. Válassza az **SQL Database Auditing** \> **Beolvasás** elemet.
   
   ![](media/service-connect-to-azure-sql-database-auditing/sqldbaudit.png)
4. A Csatlakozás a következőhöz: SQL Database Auditing ablakban:
   
   - Adja meg az eseménynaplókat tároló Azure Table Storage-fiók nevét vagy URL-címét.
   
   - Adja meg az Önt érdeklő SQL-kiszolgáló nevét. Ha mindegyik kiszolgáló auditnaplóit be szeretné tölteni, a „\*” értéket írja be.
   
   - Adja meg az Önt érdeklő SQL-adatbázis nevét. Ha mindegyik adatbázis auditnaplóit be szeretné tölteni, a „\*” értéket írja be.
   
   - Adja meg az Önt érdeklő eseménynaplókat tartalmazó Azure-tábla nevét. Ha minden olyan tábla auditnaplóit be szeretné tölteni, amelynek a nevében szerepel az „AuditLogs” kifejezés, a „\*” értéket írja be.
   
   >[!IMPORTANT]
   >Azt javasoljuk, hogy mindig írja be egy konkrét tábla nevét még akkor is, ha egyetlen tábla tárol minden auditnaplót, mert így gyorsabb működést érhet el.
   
   - Adja meg, hogy melyik naptól kezdődően érdeklik az auditnaplók. Ha alsó időkorlát nélkül szeretné betölteni az auditnaplókat, a „\*” értéket adja meg, ha a legutóbbi nap auditnaplóit, akkor az „1d” értéket.
   
   - Adja meg, hogy melyik nappal bezárólag érdeklik az auditnaplók. Ha felső időkorlát nélkül szeretné betölteni az auditnaplókat, a „\*” értéket adja meg.
   
   ![](media/service-connect-to-azure-sql-database-auditing/dbauditing_param.png)
5. Hitelesítési módszerként válassza a **Kulcs** lehetőséget, adja meg a **Fiókkulcs** értékét, majd válassza a \> **Bejelentkezés** elemet.
   
   ![](media/service-connect-to-azure-sql-database-auditing/pbi_sqlauditing3.png)
6. Miután a Power BI importálta az adatokat, a bal oldali navigációs ablaktáblán megjelenik egy új irányítópult, egy új jelentés és egy új adatkészlet. Az új elemeket sárga csillag \* jelöli.
   
   ![](media/service-connect-to-azure-sql-database-auditing/pbi_sqldbauditingnewdash.png)

**Hogyan tovább?**

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja a frissítési ütemezést, vagy igény szerint bármikor frissíthet az **Azonnali frissítés** elemre kattintva

## <a name="next-steps"></a>Következő lépések
[Adatbeolvasás a Power BI szolgáltatásban](service-get-data.md)
[Bevezetés a Power BI használatába](service-get-started.md)
