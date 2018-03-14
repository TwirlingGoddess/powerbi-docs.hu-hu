---
title: "A Power BI szolgáltatásban nyisson meg egy jelentést Olvasás nézetben vagy Szerkesztés nézetben"
description: "Power BI-jelentés megnyitása Olvasó vagy Szerkesztő nézetben"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 03/01/2018
ms.author: mihart
ms.openlocfilehash: c5177f4ccce8e8e274944cdcb539ca65a8f87ca8
ms.sourcegitcommit: 5e1f7d2673efe25c47b9b9f315011055bfe92c8f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/09/2018
---
# <a name="open-a-report-in-power-bi-service-apppowerbicom"></a>Jelentés megnyitása a Power BI szolgáltatásban (az app.powerbi.com webhelyen)
A jelentések elérhetőek a Power BI szolgáltatásban, a Power BI Desktopban, a Power BI-mobilalkalmazásban, sőt a Power BI Embeddedben is. Ebben a cikkben azt feltételezzük, hogy a jelentést a ***Power BI szolgáltatásban*** nyitotta meg.

A Power BI szolgáltatásban a jelentések két módban tekinthetők meg és kezelhetők: az [Olvasó és a Szerkesztési nézetben](service-reading-view-and-editing-view.md). Az Olvasó nézet minden felhasználó számára elérhető, és speciálisan az adatok *felhasználói* számára lett kialakítva, míg a Szerkesztő nézet csak a jelentések *létrehozói* és tulajdonosai számára érhető el. 

## <a name="open-a-report-from-a-workspace-via-the-reports-content-view-list"></a>Jelentés megnyitása munkaterületről (a **Jelentések** tartalom nézet listájában)

1. Egy munkaterületről kiindulva válassza a **Jelentések** lapot, hogy megjelenítse az adott munkaterület összes jelentését.  
   
   ![Munkaterület Jelentések lapja](media/service-report-open/power-bi-open-report.png)
2. Válassza ki egy jelentés nevét, és nyissa meg Olvasó nézetben.  
   
    ![jelentés az Olvasó nézetben](media/service-report-open/power-bi-reading-view.png)
3. [Az Olvasó nézetben sokféle lehetősége van](service-reading-view-and-editing-view.md).  Ez egy többoldalas jelentésminta, feltárásához válassza ki az egyes oldalakat a jelentésvászon alján. 

## <a name="open-a-report-from-a-dashboard"></a>Jelentés megnyitása irányítópultról
Sokféleképpen meg lehet nyitni egy jelentést, például egy irányítópultról kiindulva egy, az adott jelentésből létrehozott csempe kiválasztásával.  A csempe kiválasztása megnyitja a jelentést Olvasó nézetben. Annak érdekében, hogy követni tudja a lépéseket, nyissa meg az [Értékesítési és marketing minta irányítópultját](sample-datasets.md).

1. Nyissa meg az irányítópultot és válasszon ki egy csempét.

   Ha olyan csempét nyit meg, amelyet a [Q&A használatával hoztak létre](service-dashboard-pin-tile-from-q-and-a.md), akkor a Q&A képernyő is megnyílik. Ha olyan csempét választ, amelyet az [irányítópulton található **Csempe hozzáadása** widget](service-dashboard-add-widget.md) használatával hoztak létre, akkor megnyitja a widget szerkesztésére szolgáló varázslót.  

2.  Ebben a példában a „Total Units YTD...” (Összes egység az év elejétől...) oszlopdiagram címét választottuk.

    ![irányítópult egy kijelölt csempével](media/service-report-open/power-bi-dashboard.png)

3.  A kapcsolódó jelentés Olvasó nézetben nyílik meg. Figyelje meg, hogy most a „YTD Category” oldalon vagyunk. Ez a jelentésoldal tartalmazza azt az oszlopdiagramot, amelyet az irányítópulton választottunk ki.

    ![megnyitott jelentés az Olvasó nézetben](media/service-report-open/power-bi-report.png)

4. Maradjon az Olvasó nézetben, vagy válassza a **Jelentés szerkesztése** lehetőséget, és nyissa meg a jelentést Szerkesztési nézetben. Ne feledje, hogy csak a szerkesztési jogosultsággal rendelkezők nyithatják meg a jelentést Szerkesztési nézetben.

    ![Jelentésszerkesztő a Jelentés szerkesztése ikonnal](media/service-report-open/power-bi-edit-report.png)

## <a name="create-a-brand-new-report-from-a-dataset"></a>Új jelentés létrehozása adatkészletből
A jelentés megnyitásának van még egy újabb módja is: a megnyitás adathalmazból. Ha adathalmazzal kezd, a jelentésvászon üres lesz, ezért ezt a módszert a jelentések *létrehozóinak* ajánljuk, akik saját adathalmazt használva szeretnének új jelentést létrehozni. A fentiekhez hasonlóan ahhoz, hogy követni tudja a lépéseket, töltse le az [Értékesítési és marketing minta alkalmazását](sample-datasets.md).

1. Kezdje azon a munkaterületen, amely azt az adathalmazt tartalmazza, amelyet a jelentés alapjául szeretne használni.

   ![bal oldali navigációs ablak az alkalmazás munkaterületeivel](media/service-report-open/power-bi-workspace.png)

2. Válassza az **Adathalmazok** lapot, amivel megjelenítheti a munkaterület összes adathalmazát. Ezt az **Adathalmaz** tartalomnézeti listájának nevezzük.
   
   ![adatkészletek listája](media/service-report-open/power-bi-dataset.png)

1. Keresse meg az adathalmazt, és válassza a **Jelentés létrehozása** ikont, amellyel az adathalmazt Szerkesztési nézetben nyitja meg. A jelentést csak akkor tudja megnyitni, ha szerkesztési jogosultsággal rendelkezik hozzá. 
   
    ![adatkészlet a Jelentés létrehozása ikonnal](media/service-report-open/power-bi-create-report.png)

3. Az adathalmaz megnyílik a jelentésszerkesztőben. A jobb oldalon találja az adatmezőket. Ezeket használva máris elkezdheti a vizualizációk létrehozását. 

   ![A jelentésvászon](media/service-report-open/power-bi-blank-canvas.png)

##  <a name="still-more-ways-to-open-a-report"></a>További lehetőségek a jelentés megnyitására
Ha már otthonosabban mozog a Power BI szolgáltatásban, minden bizonnyal tudni fogja, mely munkafolyamatok a legkényelmesebbek az Ön számára. Íme még néhány további lehetőség a jelentések megnyitásához:
- A bal oldali navigációs panelen válassza a **Kedvencek**, **Legutóbbi**, **Alkalmazások* elemet, majd a **Velem megosztott** lehetőséget. 
- A [Kapcsolódó megtekintése](service-related-content.md) használata
- E-mailben, ha valaki [Önnel osztott meg](service-share-reports.md) jelentést, vagy ha [Riasztást állít be](service-set-data-alerts.md).    
- Az [Értesítési központból](service-notification-center.md)    
- és még néhány további lehetőség

## <a name="next-steps"></a>Következő lépések
A [Power BI jelentéseiről itt talál](service-reports.md) további információkat

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)  

