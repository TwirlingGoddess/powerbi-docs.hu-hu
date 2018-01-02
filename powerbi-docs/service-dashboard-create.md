---
title: "Power BI-irányítópult létrehozása jelentésből"
description: "Power BI-irányítópult létrehozása jelentésből"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: 
qualityfocus: 
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 05/09/2017
ms.author: mihart
ms.openlocfilehash: dac5628756898a20fe139447bc2d165ba804320c
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="create-a-power-bi-dashboard-from-a-report"></a>Power BI-irányítópult létrehozása jelentésből
Áttekintette [A Power BI-irányítópultok](service-dashboards.md) részben leírtakat, és most saját irányítópultot kíván létrehozni. Az irányítópultok létrehozásának számos különböző módja van: többek között jelentésből, az alapoktól, adatkészletből, illetve egy meglévő irányítópult megkettőzésével is létrehozhatók stb.  Ez a témakör és videó egy új irányítópult létrehozását mutatja egy meglévő jelentésből származó vizualizációk rögzítésével.

> **MEGJEGYZÉS**: Az irányítópult a Power BI szolgáltatás, nem pedig a Power BI Desktop funkciója. Power BI-mobileszközökön csak [megtekinteni és megosztani](mobile-apps-view-dashboard.md) lehet az irányítópultokat, létrehozni nem.
> 
> 

![](media/service-dashboard-create/power-bi-completed-dashboard-small.png)

## <a name="video-create-a-dashboard-by-pinning-visuals-and-images-from-a-report"></a>Videó: Irányítópult létrehozása jelentésből származó vizualizációk és képek rögzítésével
Tekintse meg, ahogy Amanda bemutatja egy új irányítópult létrehozását jelentésből származó vizualizációk rögzítésével. Ezután a videó alatt látható lépeseket követve próbálkozzon meg a feladattal saját maga is a Beszerzéselemzési minta használatával.

<iframe width="560" height="315" src="https://www.youtube.com/embed/lJKgWnvl6bQ" frameborder="0" allowfullscreen></iframe>

## <a name="import-a-dataset-with-a-report"></a>Adatkészlet importálása jelentés használatával
A Power BI egyik mintaként szolgáló adatkészletét fogjuk importálni, majd egy új irányítópult létrehozására felhasználni. Az itt használt minta egy olyan Excel-munkafüzet, amelyben két PowerView-munkalap található. Amikor a Power BI importálja a munkafüzetet, egy adatkészletet és egy jelentést is hozzáad a munkaterülethez.  A rendszer a jelentést automatikusan hozza létre a PowerView-munkalapokból.

1. [Kattintson erre a hivatkozásra](http://go.microsoft.com/fwlink/?LinkId=529784) a Beszerzéselemzési minta Excel-fájl letöltéséhez és mentéséhez. Javasoljuk, hogy a OneDrive Vállalati verziójában mentse azt.
2. Nyissa meg a Power BI szolgáltatást a böngészőben (app.powerbi.com).
3. Válasszon ki egy meglévő munkaterületet, vagy hozzon létre egy új alkalmazás-munkaterületet.
4. A bal oldali navigációs panelen válassza az **Adatok lekérése** lehetőséget.
   
    ![](media/service-dashboard-create/power-bi-get-data3.png)
5. Válassza a **Fájlok** lehetőséget.
   
   ![](media/service-dashboard-create/power-bi-select-files.png)
6. Keresse meg a helyet, ahová a Beszerzéselemzési minta Excel-fájlját mentette. Jelölje ki azt, és válassza a **Kapcsolódás** lehetőséget.
   
   ![](media/service-dashboard-create/power-bi-connectnew.png)
7. Ehhez a gyakorlathoz válassza az **Importálás** lehetőséget.
   
    ![](media/service-dashboard-create/power-bi-import.png)
8. A sikert jelző üzenet megjelenésekor az **x** jelre kattintva zárja be azt.
   
   ![](media/service-dashboard-create/power-bi-view-datasetnew.png)

### <a name="open-the-report-and-pin-some-tiles-to-a-dashboard"></a>A jelentés megnyitása, és néhány csempe rögzítése az irányítópulton
1. Ugyanazon a munkaterületen maradva kattintson a **Jelentések** lapra. Megjelenik az újonnan importált jelentés egy sárga csillaggal. A megnyitásához kattintson a jelentés nevére.
   
    ![](media/service-dashboard-create/power-bi-reports.png)
2. A jelentés [Olvasás nézetben](service-interact-with-a-report-in-reading-view.md) nyílik meg. Figyelje meg, hogy két lap található alul: a Discount Analysis (Kedvezményelemzés) és a Spend Overview (Költségvetés áttekintése) lapok. Minden egyes lap a jelentés egy-egy oldalát jelképezi.
   
    ![](media/service-dashboard-create/power-bi-reading-view.png)
3. A rendelkezésre álló beállítások megjelenítéséhez húzza a mutatót a vizualizáció fölé. A vizualizációnak az irányítópulthoz történő hozzáadásához kattintson a rögzítés ![](media/service-dashboard-create/power-bi-pin-icon.png) ikonra.
   
    ![](media/service-dashboard-create/power-bi-hover.png)
4. Mivel most egy új irányítópultot hozunk létre, válassza az **Új irányítópult** lehetőséget, és adjon meg egy nevet. 
   
   ![](media/service-dashboard-create/power-bi-pin-tile.png)
5. A **Rögzítés** lehetőség kiválasztásakor a Power BI az aktuális munkaterületen létrehoz egy új irányítópultot. A **Rögzítve az irányítópulton** üzenet megjelenésekor válassza az **Ugrás az irányítópultra** lehetőséget. Ha a rendszer felkéri a jelentés mentésére, válassza a **Mentés** lehetőséget.
   
     ![](media/service-dashboard-create/power-bi-pin-success.png)
6. A Power BI ekkor megnyitja az új irányítópultot, ahol egy csempe (az imént rögzített vizualizáció) található. 
   
   ![](media/service-dashboard-create/power-bi-pinned.png)
7. A jelentéshez való visszatéréshez kattintson a csempére. Rögzítsen még néhány csempét az irányítópulton. Ha a **Rögzítés az irányítópulton** ablak megjelenik, ezúttal válassza a **Meglévő irányítópult** lehetőséget.  
   
   ![](media/service-dashboard-create/power-bi-existing-dashboard.png)

Gratulálunk, létrehozta az első irányítópultját! Most, hogy már rendelkezik irányítópulttal, számos további lehetőség nyílik meg.  Próbálja ki az alábbiakban javasolt **Következő lépések** egyikét, vagy próbálkozzon saját maga.   

## <a name="next-steps"></a>Következő lépések
* [Csempék átméretezése és áthelyezése](service-dashboard-edit-tile.md)
* [Információk az irányítópult csempéiről](service-dashboard-tiles.md)
* [Az irányítópult megosztása alkalmazás létrehozásával](service-create-distribute-apps.md)
* [Power BI – Alapfogalmak](service-basic-concepts.md)
* [A Power BI-irányítópultok](service-dashboards.md)
* [Tippek a tökéletes irányítópult megtervezéséhez](service-dashboards-design-tips.md)

További kérdései vannak? [Forduljon a Power BI közösségéhez](http://community.powerbi.com/)

