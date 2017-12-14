---
title: "Új jelentés létrehozása adatkészletből "
description: "Hozzon létre egy új Power BI-jelentést egy adatkészletből."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: f4afb1eaa1b3012fdbdb0eff35e9eff695cc32e4
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="create-a-new-power-bi-report-by-importing-a-dataset"></a>Új Power BI-jelentés létrehozása adatkészlet importálásával
Már elolvasta a [Jelentések a Power BI-ban](service-reports.md) című cikket, és szeretne létrehozni egy saját jelentést. A jelentések több különböző módon is létrehozhatók. Ebben a cikkben kezdésként egy Excel-adatkészletből egy alapszintű jelentést fogunk létrehozni. Ha már megismerte a jelentés létrehozásának alapjait, akkor a lap alján található **Következő lépések** hivatkozással továbbhaladhat a jelentésekkel kapcsolatos összetettebb témakörökre is.  

> **TIPP**: Ha egy meglévő jelentés másolásával szeretne létrehozni egy új jelentést, tekintse meg a [Jelentés másolása](power-bi-report-copy.md) cikket.
> 
> 

## <a name="import-the-dataset"></a>Adatkészlet importálása
Ha ezzel a módszerrel hoz létre egy jelentést, akkor annak kiindulópontja egy adatkészlet és egy üres jelentésvászon lesz. Ahhoz, hogy követhesse a lépéseket, [töltse le a Kiskereskedelmi elemzési minta Excel-adatkészletét](http://go.microsoft.com/fwlink/?LinkId=529778), és mentse a OneDrive Vállalati verzióra (javasolt) vagy lokálisan a számítógépére.

1. A jelentést a Power BI szolgáltatás egy munkaterületén fogjuk létrehozni, ezért válasszon ki egy meglévő munkaterületet, vagy hozzon létre egy újat.
   
   ![](media/service-report-create-new/power-bi-workspaces2.png)
2. A bal oldali navigációs sávon válassza az **Adatok lekérése** elemet.
   
   ![](media/service-report-create-new/power-bi-get-data3.png)
3. Válassza a **Fájlok** lehetőséget, majd navigáljon arra a helyre, ahova a Kiskereskedelmi elemzési mintát mentette.
   
    ![](media/service-report-create-new/power-bi-select-files.png)
4. Ehhez a feladathoz válassza az **Importálás** lehetőséget.
   
   ![](media/service-report-create-new/power-bi-import.png)
5. Ha megtörtént az adatkészlet importálása, válassza az **Adatkészlet megtekintése** lehetőséget.
   
   ![](media/service-report-create-new/power-bi-view-dataset.png)
6. Ha megtekint egy adatkészletet, azzal tulajdonképpen a jelentésszerkesztőt nyitja meg.  Egy üres vásznat fog látni, és a jelentések készítéséhez szükséges eszközöket.
   
   ![](media/service-report-create-new/power-bi-blank-report.png)

> **TIPP**: Ha nem ismeri a jelentésszerkesztő vásznat, vagy szeretné felfrissíteni ismereteit, [Tekintse át a jelentésszerkesztőt](service-the-report-editor-take-a-tour.md), mielőtt továbbhaladna.
> 
> 

## <a name="add-a-radial-gauge-to-the-report"></a>Mérőműszer felvétele jelentésbe
Most hogy már importáltuk az adatkészletünket, kezdjük el megválaszolni a kérdéseket.  A marketingigazgató tudni szeretné, hogy mennyire állunk közel ahhoz, hogy elérjük az idei év értékesítési célkitűzéseit. A mérőműszer [vizualizáció egy jó választás](power-bi-report-visualizations.md), ha ilyen típusú adatokat szeretnénk megjeleníteni.

1. A Mezők ablaktáblán válassza a **Sales** > **This Year Sales** > **Érték** elemet.
   
    ![](media/service-report-create-new/power-bi-report-step1.png)
2. Konvertálja a vizualizációt egy Mérőműszerré, ehhez válassza a **Megjelenítések** ablaktáblán a Mérőműszer sablont ![](media/service-report-create-new/powerbi-gauge-icon.png).
   
    ![](media/service-report-create-new/power-bi-report-step2.png)
3. Húzza a **Sales** > **This Year Sales** > **Cél** elemet a **Célérték** gyűjtőbe. Úgy látszik, nagyon közel vagyunk a célkitűzésünk eléréséhez.
   
    ![](media/service-report-create-new/power-bi-report-step3.png)
4. Érdemes [menteni a jelentést](service-report-save.md).
   
   ![](media/service-report-create-new/powerbi-save.png)

## <a name="add-an-area-chart-and-slicer-to-the-report"></a>Területdiagram és szeletelő felvétele a jelentésbe
Meg kell válaszolnunk a marketingigazgató újabb kérdéseit. Szeretné tudni, hogy milyenek az idei év értékesítési mutatói a tavalyi évhez képest. És ezt az egyes körzetekre lebontva szeretné látni.

1. Először is csináljunk egy kis helyet a vásznunkon. Válassza ki a Mérőműszert és helyezze a jobb felső sarokba. Ezután fogja meg az egyik sarkát és kicsinyítse le.
2. Szüntesse meg a mérőműszer kijelölt állapotát. A Mezők ablaktáblán válassza a **Sales** > **This Year Sales** > **Érték**, majd a **Sales** > **Last Year Sales** elemeket.
   
    ![](media/service-report-create-new/power-bi-report-step4.png)
3. Konvertálja a vizualizációt egy Területdiagrammá, ehhez válassza a **Megjelenítések** ablaktáblán a Területdiagram sablont ![](media/service-report-create-new/power-bi-areachart-icon.png).
4. Adja hozzá a **Time** > **Period** elemet a **Tengely** gyűjtőhöz.
   
    ![](media/service-report-create-new/power-bi-report-step5.png)
5. A vizualizáció rendezéséhez válassza a három pontot (...), majd a **Rendezés szempontja: Period** lehetőséget.
6. És most vegyük fel a szeletelőt. Válassza ki a vászon egy üres területét, majd a Szeletelő ![](media/service-report-create-new/power-bi-slicer-icon.png)    sablont. Ez felvesz a vásznunkra egy üres szeletelőt.
   
    ![](media/service-report-create-new/power-bi-report-step6.png)    
7. A Mezők ablaktáblán válassza a **District** > **District** elemet. Helyezze át és méretezze át a szeletelőt.
   
    ![](media/service-report-create-new/power-bi-report-step7.png)  
8. A szeletelő használatával mintákat és összefüggéseket kereshet az egyes körzetek szerint.
   
   ![](media/service-report-create-new/power-bi-slicer-video2.gif)  
9. Felvehet további vizualizációkat is.

## <a name="next-steps"></a>Következő lépések
* [Jelentés másolatának létrehozása](power-bi-report-copy.md)
* [Jelentés mentése](service-report-save.md)    
* [Új oldal hozzáadása jelentéshez](power-bi-report-add-page.md)  
* Tudnivalók arról, hogyan történik a [vizualizációk rögzítése egy irányítópulton](service-dashboard-pin-tile-from-report.md)    
* További kérdései vannak? [Felteheti azokat a Power BI-közösségnek](http://community.powerbi.com/)

