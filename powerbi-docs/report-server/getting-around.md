---
title: "Alapvető tudnivalók a Power BI jelentéskészítő kiszolgáló webportáljáról"
description: "Ebben a cikkben a Power BI jelentéskészítő kiszolgáló webportálján végzett navigációról és munkáról olvashat."
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 10/12/2017
ms.author: maggies
ms.openlocfilehash: 7d59531bfed80e854bc19b1df00aaf9cce7144d6
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="navigating-the-power-bi-report-server-web-portal"></a>Navigáció a Power BI jelentéskészítő kiszolgáló webportálján
A Power BI jelentéskészítő kiszolgáló webportálja egy helyszíni platform, amely Power BI-, mobil- és többoldalas jelentések és főbb teljesítménymutatók (KPI-k) megtekintésére, tárolására és kezelésére szolgál.

![A jelentéskészítő kiszolgáló webportálja](media/getting-around/report-server-web-portal.png)

A webportál bármelyik korszerű böngészőben megnyitható. A jelentéseket és a főbb teljesítménymutatókat a webportál mappákba rendezi, amelyeket megjelölhet kedvencként. A mappákban Excel-munkafüzeteket is tárolhat. A webportálról elindíthatja a jelentéskészítéshez szükséges eszközöket:

* **Power BI-jelentések** a Power BI Desktop alkalmazással: megtekinthetők a webportálon és Power BI-mobilalkalmazásokban.
* **Többoldalas jelentések** a Jelentéskészítővel: korszerű megjelenésű, rögzített elrendezésű, nyomtatásra optimalizált dokumentumok.
* **Főbb teljesítménymutatók**, amelyek közvetlenül a webportálon készülnek.

A webportálon tallózhat a jelentéskészítő kiszolgáló mappáiban, és adott jelentéseket is megkereshet. Megtekintheti a jelentéseket, az általános jelentéstulajdonságaikat és a jelentéselőzmények közt tárolt korábbi példányaikat. Ha engedélyei lehetővé teszik, feliratkozhat jelentésekre, és kérheti az e-mailben vagy a fájlrendszer egy megosztott mappájába való elküldésüket.

## <a name="web-portal-tasks"></a>A webportálon elérhető műveletek
A webportálon számos művelet végrehajtható, többek között az alábbiak:

* Jelentések megtekintése, keresése, nyomtatása, illetve feliratkozás jelentésekre
* Mappahierarchia létrehozása, védelme és kezelése a kiszolgálón tárolt elemek rendszerezéséhez
* Jelentés-végrehajtási tulajdonságok, jelentéselőzmények és jelentésparaméterek beállítása
* Megosztott ütemezések és megosztott adatforrások létrehozása, hogy kezelhetőbbek legyenek az ütemtervek és az adatforrás-kapcsolatok
* Jelentések küldése nagyszámú címzettnek adatvezérelt előfizetések létrehozásával
* Jelentések újbóli és új célokkal való felhasználása csatolt jelentések létrehozásával
* Gyakran használt eszközök – például a Power BI Desktop (Jelentéskészítő kiszolgáló), a Jelentéskészítő és a Mobiljelentés-publikáló letöltése és megnyitása
* [Főbb teljesítménymutatók (KPI-k) létrehozása](https://docs.microsoft.com/sql/reporting-services/working-with-kpis-in-reporting-services)
* Visszajelzés vagy funkcióigénylés küldése
* [A webportál védjegyezése](https://docs.microsoft.com/sql/reporting-services/branding-the-web-portal)
* [A főbb teljesítménymutatók használata](https://docs.microsoft.com/sql/reporting-services/working-with-kpis-in-reporting-services)
* [A megosztott adatkészletek használata](https://docs.microsoft.com/sql/reporting-services/work-with-shared-datasets-web-portal)

## <a name="web-portal-roles-and-permissions"></a>Webportálszerepkörök és -engedélyek
A webportál böngészőben futó webalkalmazás. Attól függ, hogy milyen lapok, hivatkozások és lehetőségek jelennek meg a webportál megnyitásakor, hogy Önnek milyen jogosultságai vannak a jelentéskészítő kiszolgálón. Ha teljes körű jogosultságokkal rendelkező szerepköre van, minden alkalmazásmenühöz és laphoz hozzáfér, amely a jelentéskészítő kiszolgáló kezeléséhez szükséges. Ha a szerepköre jelentések megtekintését és futtatását teszi lehetővé, akkor csak az ehhez szükséges menüket és lapokat éri el. Szerepkörei az egyes jelentéskészítő kiszolgálókon – sőt, akár egy kiszolgálón belül az egyes jelentésekben és mappákban – eltérőek lehetnek.

## <a name="start-the-web-portal"></a>A webportál megnyitása
1. Nyissa meg a webböngészőt.
   
    A [támogatott webböngészők és verziók](browser-support.md) listáját itt találja.
2. A címsorba írja be a webportál URL-jét.
   
    Ez alapértelmezés szerint a *http://[A számítógép neve]/reports*.
   
    Előfordulhat, hogy a jelentéskészítő kiszolgáló egy adott port használatára van beállítva. Például: *http://[A számítógép neve]:80/reports* vagy *http://[A számítógép neve]:8080/reports*
   
    Amint láthatja, a webportál kategóriákba rendezi az elemeket:
   
   * KPI-k
   * Mobiljelentések
   * Többoldalas jelentések
   * Power BI Desktop-jelentések
   * Excel-munkafüzetek
   * Adatkészletek
   * Adatforrások
   * Erőforrások

## <a name="create-and-edit-power-bi-desktop-reports-pbix-files"></a>Power BI Desktop-jelentések (.pbix-fájlok) létrehozása és szerkesztése
A webportálon megtekintheti, feltöltheti, létrehozhatja és rendszerezheti a Power BI Desktop-jelentéseket, és kezelheti az engedélyeiket.

### <a name="create-a-power-bi-desktop-report"></a>Power BI Desktop-jelentés létrehozása
1. Válassza az **Új** > **Power BI-jelentés** elemet.
   
    ![Új Power BI-jelentés létrehozása](media/getting-around/report-server-web-portal-new-powerbi-report.png)
   
    Megnyílik a Power BI Desktop alkalmazás.
   
    ![A Power BI Desktop alkalmazás](media/getting-around/report-server-powerbi-desktop-start.png)
2. Hozza létre saját Power BI-jelentését. További információt a [Rövid útmutató: Power BI-jelentések](quickstart-create-powerbi-report.md) című cikkben talál.
3. Töltse fel a jelentést a jelentéskészítő kiszolgálóra.

### <a name="edit-an-existing-power-bi-desktop-report"></a>Power BI Desktop-jelentés szerkesztése
1. Válassza a három pont ikont (**...**) a jelentéscsempe jobb felső sarkában, majd kattintson a **Szerkesztés a Power BI Desktopban** parancsra.
   
    ![Szerkesztés a Power BI Desktopban](media/getting-around/report-server-web-portal-pbix-ellipsis.png)
   
    Megnyílik a Power BI Desktop alkalmazás.
2. Hajtsa végre és mentse a módosításokat... [Hogyan?]

## <a name="create-and-edit-paginated-reports-rdl-files"></a>Többoldalas jelentések (.rdl-fájlok) létrehozása és szerkesztése
A webportálon megtekintheti, feltöltheti, létrehozhatja és rendszerezheti a többoldalas jelentéseket, és kezelheti az engedélyeiket.

### <a name="create-a-paginated-report"></a>Többoldalas jelentés készítése
1. Válassza az **Új** > **Többoldalas jelentés** elemet.
   
    Elindul a Jelentéskészítő alkalmazás.
   
    ![Új Jelentéskészítőbeli jelentés](media/getting-around/report-server-report-builder-new.png)
2. Hozza létre saját többoldalas jelentését. Lásd a [Rövid útmutató: Többoldalas jelentések](quickstart-create-paginated-report.md) című cikket.
3. Töltse fel a jelentést a jelentéskészítő kiszolgálóra.

### <a name="edit-an-existing-paginated-report"></a>Többoldalas jelentés szerkesztése
1. Válassza a három pont ikont (...) a jelentéscsempe jobb felső sarkában, majd kattintson a **Szerkesztés a Jelentéskészítőben** parancsra.
   
    ![Szerkesztés a Jelentéskészítőben](media/getting-around/report-server-web-portal-rdl-ellipsis.png)
   
    Elindul a Jelentéskészítő alkalmazás.
2. Hajtsa végre és mentse a módosításokat.

## <a name="upload-and-organize-excel-workbooks"></a>Excel-munkafüzetek feltöltése és rendszerezése
Feltöltheti és rendszerezheti a Power BI Desktop-jelentéseket és Excel-munkafüzeteket, és kezelheti az engedélyeiket. Ezek csoportosítva láthatók a webportálon.

A munkafüzetek a Power BI jelentéskészítő kiszolgálón találhatók, hasonlóan más erőforrásfájlokhoz. Ha rákattint egy munkafüzetre, letölti a helyi asztalra. A változásokat a jelentéskészítő kiszolgálóra történő újbóli feltöltéssel mentheti.

## <a name="manage-items-in-the-web-portal"></a>Elemek kezelése a webportálon
A Power BI jelentéskészítő kiszolgálón Önnek teljes körű jogosultsága van a webportálon tárolt elemek kezelésére. Beállíthat például feliratkozásokat, gyorsítótárazást, pillanatképeket és az egyes többoldalas jelentésekre vonatkozó védelmet.

1. Kattintson a három pontra (...) egy elem jobb felső sarkában, majd a **Kezelés** lehetőségre.
   
    ![Kattintás a Kezelés elemre](media/getting-around/report-server-web-portal-manage-ellipsis.png)
2. Válasszon egy tulajdonságot vagy más beállítást.
   
    ![Tulajdonság kiválasztása](media/getting-around/report-server-web-portal-manage-properties.png)
3. Kattintson az **Alkalmazás** lehetőségre.

További információ [a feliratkozásoknak a webportálon történő kezeléséről](https://docs.microsoft.com/sql/reporting-services/working-with-subscriptions-web-portal).

## <a name="tag-your-favorite-reports-and-kpis"></a>Főbb teljesítménymutatók és jelentések megjelölése kedvencként
A kívánt főbb teljesítménymutatókat és jelentéseket megjelölheti kedvencként. Mivel ezek a központi Kedvencek mappában kapnak helyet, könnyen megtalálhatók mind a webportálon, mind a Power BI-mobilalkalmazásokban. 

1. A kedvencek közé felvenni kívánt főbb jelentésmutató vagy jelentés jobb felső sarkában kattintson a három pontra (**...**), majd a **Hozzáadás a kedvencekhez** elemre.
   
    ![Hozzáadás a Kedvencekhez](media/getting-around/report-server-web-portal-favorite-ellipsis.png)
2. Ha a webportál menüszalagján a **Kedvencek** lehetőségre kattint, ez a csoport is megjelenik a webportál Kedvencek lapján.
   
    ![Kedvencek megtekintése](media/getting-around/report-server-web-portal-favorites.png)
   
    A Power BI-mobilalkalmazásokban kedvenc Power BI-irányítópultjai mellett immár ezeket a kedvenceket is láthatja.
   
    ![Kedvencek megtekintése a mobilalkalmazásban](media/getting-around/power-bi-iphone-faves-report-server.png)

## <a name="hide-or-view-items-in-the-web-portal"></a>Elemek elrejtése és megjelenítése a webportálon
A webportál elemeit elrejtheti, rejtett elemeit pedig megjelenítheti.

### <a name="hide-an-item"></a>Elem elrejtése
1. Kattintson a három pontra (...) egy elem jobb felső sarkában, majd a **Kezelés** lehetőségre.
   
    ![Kattintás a Kezelés elemre](media/getting-around/report-server-web-portal-manage-ellipsis.png)
2. Válassza az **Elem elrejtése** elemet.
   
    ![Elrejtés kiválasztása](media/getting-around/report-server-web-portal-hide-property.png)
3. Kattintson az **Alkalmazás** lehetőségre.

### <a name="view-hidden-items"></a>Rejtett elemek megjelenítése
1. Kattintson a **Csempék** (vagy **Listák**) elemre a jobb felső sarokban, majd a **Rejtett elemek megjelenítése** lehetőségre.
   
    Ekkor megjelennek az elemek. Bár halványítva láthatók, mégis megnyithatók és szerkeszthetők.
   
    ![Rejtett elemek megjelenítése](media/getting-around/report-server-web-portal-show-hidden-grayed.png)

## <a name="search-for-items"></a>Elemek keresése
Ha rákeres egy kifejezésre, minden olyan elem megjelenik a találatok közt, amelyhez hozzáfér. A találatok kategóriákba szedve láthatók: KPI-k, jelentések, adatkészletek stb. Az eredményeket megtekintheti, és felveheti a kedvencek közé.  

![Elemek keresése](media/getting-around/report-server-web-portal-search.png)

## <a name="move-or-delete-items-in-list-view"></a>Elemek áthelyezése és törlése a Lista nézetben
A webportál alapértelmezés szerint Csempe nézetben látható.

Ön azonban Lista nézetre válthat, amelyben egyszerre több elemet is egyszerűen mozgathat vagy törölhet. 

1. Kattintson a **Csempék** > **Lista** elemre.
   
    ![Nézetváltás](media/getting-around/report-server-web-portal-list-view.png)
2. Jelölje ki az elemeket, majd kattintson az **Áthelyezés** vagy a **Törlés** lehetőségre.

## <a name="next-steps"></a>Következő lépések
[Felhasználói kézikönyv](user-handbook-overview.md)  
[Rövid útmutató: Többoldalas jelentések](quickstart-create-paginated-report.md)  
[Rövid útmutató: Power BI-jelentések](quickstart-create-powerbi-report.md)

További kérdései vannak? [Kérdezze a Power BI-közösséget!](https://community.powerbi.com/)

