---
title: "Az Azure SQL Data Warehouse használata DirectQueryvel"
description: "Az Azure SQL Data Warehouse használata DirectQueryvel"
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
ms.date: 08/10/2017
ms.author: maghan
LocalizationGroup: Data from databases
ms.openlocfilehash: 6d7cb2161702b844866af66896dbadb35ad801ed
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="azure-sql-data-warehouse-with-directquery"></a>Az Azure SQL Data Warehouse használata DirectQueryvel
Ha DirectQueryvel csatlakozik az Azure SQL Data Warehouse-hoz, dinamikus jelentéseket hozhat létre az Azure SQL Data Warehouse-ban tárolt adatokat és metrikákat használva. DirectQuery használata esetén a rendszer valós idejű lekérdezéseket küld az Azure SQL Data Warehouse-ba az adatok feltárásakor. Ez a módszer az SQL Data Warehouse méreteit is tekintve lehetővé teszi, hogy percek alatt hozzunk létre dinamikus jelentéseket akár több terabájtnyi adatból is. Ezenkívül a **Megnyitás Power BI-ban** gomb lehetővé teszi, hogy a felhasználók közvetlenül is csatlakoztathassák a Power BI-t az SQL Data Warehouse-hoz anélkül, hogy külön be kellene írniuk az ehhez szükséges információt.

Az SQL Data Warehouse-összekötő használatakor:

* A kapcsolódáskor a teljes szervernevet adja meg (részletes információkat lejjebb talál)
* Győződjön meg arról, hogy a kiszolgálóra vonatkozó tűzfalszabályok között konfigurálva van az „Azure-szolgáltatások hozzáférésének engedélyezése”
* A rendszer minden olyan művelet végrehajtásakor, mint amilyen például az oszlopok vagy szűrők felvétele, közvetlenül az adattárházat kérdezi le
* A csempéket körülbelül 15 percenként frissíti. A frissítést nem szükséges ütemezni.  Ezen a csatlakozáskor lehet módosítani, a Speciális beállítások között.
* DirectQueryvel elért adatkészletek esetén a Q&A nem használható
* a sémák változtatásait nem veszi át automatikusan a rendszer

Ezek a korlátozások és megjegyzések a termék folyamatos fejlesztése következtében valószínűleg változni fognak. A csatlakozás részletes lépései alább olvashatók.

## <a name="using-the-open-in-power-bi-button"></a>A „Megnyitás Power BI-ban” gomb használata
Az SQL Data Warehouse és a Power BI között a legegyszerűbben az Azure betekintő portálon elérhető **Megnyitás Power BI-ban** gombot használva mozoghat. Ez a gomb lehetővé teszi, hogy fennakadások nélkül kezdhessen új irányítópultokat létrehozni a Power BI-t használva.

1. Kiindulásképpen lépjen az SQL Data Warehouse-példányhoz az Azure betekintő portálon. Vegye figyelembe, hogy az SQL Data Warehouse jelenleg még csak az Azure betekintő portálról érhető el.
2. Kattintson a **Megnyitás Power BI-ban** gombra
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/openinpowerbi.png)
3. Ha a rendszer nem tudja közvetlenül beléptetni, vagy nem rendelkezik Power BI-fiókkal, akkor be kell jelentkeznie.
4. Ezután az SQL Data Warehouse kapcsolódási oldalára kerül, ahol a különböző mezők már ki lesznek töltve az SQL Data Warehouse adataival. Adja meg hitelesítő adatait, majd a kapcsolat létrehozásához kattintson a Kapcsolódás lehetőségre.

## <a name="connecting-through-power-bi"></a>Kapcsolódás Power BI-jal
Az SQL Data Warehouse a Power BI Adatok lekérése oldaláról is elérhető. 

1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs panel alján.  
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/getdatabutton.png)
2. Az **Adatbázisok** csempén kattintson a **Beolvasás** lehetőségre.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/databases.png)
3. Válassza az **SQL Data Warehouse** \> **Kapcsolódás** lehetőséget.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/azuresqldatawarehouseconnect.png)
4. Adja meg a kapcsolódáshoz szükséges információkat. A **Paraméterek megkeresése** szakaszban olvashat arról, hol találja meg a szükséges adatokat az Azure Portalon.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/servername.png)
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/servernamewithadvanced.png)
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/username.png)
   
   > [!NOTE]
   > A felhasználónévnek az Azure SQL Data Warehouse-példányhoz definiált egyik felhasználó nevének kell lennie.
   > 
   > 
5. Az új csempére vagy a csillaggal jelölt újonnan létrehozott adatkészletre kattintva kezdje meg az adatkészlet feltárását. Az adatkészlet neve meg fog egyezni az adatbázis nevével.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/dataset2.png)
6. Ön mindegyik táblát és oszlopot feltárhatja. Amikor kiválaszt egy oszlopot, a rendszer egy lekérdezést küld az adatforráshoz, és dinamikusan létrehozza a vizualizációt. A szűrőket szintén az adattárházba küldött lekérdezésekké alakítja a rendszer. Ezek a vizualizációk menthetők egy új jelentésbe, és kitűzhetők az irányítópultra.
   
    ![](media/service-azure-sql-data-warehouse-with-direct-connect/explore3.png)

## <a name="finding-parameter-values"></a>Paraméterértékek megkeresése
A teljes szervernevet és adatbázisnevet az Azure betekintő portálon találhatja meg. Vegye figyelembe, hogy az SQL Data Warehouse jelenleg még csak az Azure betekintő portálról érhető el.

![](media/service-azure-sql-data-warehouse-with-direct-connect/azureportal.png)

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)  
[Adatbeolvasás a Power BI-ban](service-get-data.md)  
[Az Azure SQL Data Warehouse](https://azure.microsoft.com/en-us/documentation/services/sql-data-warehouse/)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

