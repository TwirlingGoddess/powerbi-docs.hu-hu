---
title: A Power BI szolgáltatásban nyisson meg egy jelentést Olvasás nézetben vagy Szerkesztés nézetben
description: Power BI-jelentés megnyitása Olvasó vagy Szerkesztő nézetben
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 05/18/2018
ms.author: mihart
ms.openlocfilehash: fe1916b2b287dffd59bf4535cc07e13d10d01321
ms.sourcegitcommit: 70192daf070ede3382ac13f6001e0c8b5fb8d934
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/22/2018
ms.locfileid: "46565797"
---
# <a name="open-a-report-in-power-bi-service-apppowerbicom"></a>Jelentés megnyitása a Power BI szolgáltatásban (az app.powerbi.com webhelyen)
A jelentések elérhetőek a Power BI szolgáltatásban, a Power BI Desktopban, a Power BI-mobilalkalmazásban, sőt a Power BI Embeddedben is. Ebben a cikkben azt feltételezzük, hogy a jelentést a ***Power BI szolgáltatásban*** nyitotta meg.

A Power BI szolgáltatásban a jelentések két módban tekinthetők meg és kezelhetők: az [Olvasó és a Szerkesztési nézetben](end-user-reading-view.md). Az Olvasó nézet minden felhasználó számára elérhető, és speciálisan az adatok *felhasználói* számára lett kialakítva, míg a Szerkesztő nézet csak a jelentések *létrehozói* és tulajdonosai számára érhető el. 

## <a name="open-a-report-from-a-workspace-via-the-reports-content-view-list"></a>Jelentés megnyitása munkaterületről (a **Jelentések** tartalom nézet listájában)

1. Egy munkaterületről kiindulva válassza a **Jelentések** lapot, hogy megjelenítse az adott munkaterület összes jelentését.  
   
   ![Munkaterület Jelentések lapja](./media/end-user-report-open/power-bi-open-report.png)
2. Válassza ki egy jelentés nevét, és nyissa meg Olvasó nézetben.  
   
    ![jelentés az Olvasó nézetben](./media/end-user-report-open/power-bi-reading-view.png)
3. [Az Olvasó nézetben sokféle lehetősége van](end-user-reading-view.md).  Ez egy többoldalas jelentésminta, feltárásához válassza ki az egyes oldalakat a jelentésvászon alján. 

## <a name="open-a-report-from-a-dashboard"></a>Jelentés megnyitása irányítópultról
Sokféleképpen meg lehet nyitni egy jelentést, például egy irányítópultról kiindulva egy, az adott jelentésből létrehozott csempe kiválasztásával.  A csempe kiválasztása megnyitja a jelentést Olvasó nézetben. Annak érdekében, hogy követni tudja a lépéseket, nyissa meg az [Értékesítési és marketing minta irányítópultját](../sample-datasets.md).

1. Nyissa meg az irányítópultot és válasszon ki egy csempét.

   Ha olyan csempét nyit meg, amelyet a [Q&A használatával hoztak létre](../service-dashboard-pin-tile-from-q-and-a.md), akkor a Q&A képernyő is megnyílik. Ha olyan csempét választ, amelyet az [irányítópulton található **Csempe hozzáadása** widget](../service-dashboard-add-widget.md) használatával hoztak létre, akkor megnyitja a widget szerkesztésére szolgáló varázslót.  

2.  Ebben a példában a „Total Units YTD...” (Összes egység az év elejétől...) oszlopdiagram címét választottuk.

    ![irányítópult egy kijelölt csempével](./media/end-user-report-open/power-bi-dashboard.png)

3.  A kapcsolódó jelentés Olvasó nézetben nyílik meg. Figyelje meg, hogy most a „YTD Category” oldalon vagyunk. Ez a jelentésoldal tartalmazza azt az oszlopdiagramot, amelyet az irányítópulton választottunk ki.

    ![megnyitott jelentés az Olvasó nézetben](./media/end-user-report-open/power-bi-report.png)

4. Maradjon az Olvasó nézetben, vagy válassza a **Jelentés szerkesztése** lehetőséget, és nyissa meg a jelentést Szerkesztési nézetben. Ne feledje, hogy csak a szerkesztési jogosultsággal rendelkezők nyithatják meg a jelentést Szerkesztési nézetben.

    ![Jelentésszerkesztő a Jelentés szerkesztése ikonnal](./media/end-user-report-open/power-bi-edit-report.png)

## <a name="create-a-brand-new-report-from-a-dataset"></a>Új jelentés létrehozása adatkészletből
A jelentés megnyitásának van még egy újabb módja is: a megnyitás adathalmazból. Ha adathalmazzal kezd, a jelentésvászon üres lesz, ezért ezt a módszert a jelentések *létrehozóinak* ajánljuk, akik saját adathalmazt használva szeretnének új jelentést létrehozni. A fentiekhez hasonlóan ahhoz, hogy követni tudja a lépéseket, töltse le az [Értékesítési és marketing minta alkalmazását](../sample-datasets.md).

1. Kezdje azon a munkaterületen, amely azt az adathalmazt tartalmazza, amelyet a jelentés alapjául szeretne használni.

   ![bal oldali navigációs ablak az alkalmazás munkaterületeivel](./media/end-user-report-open/power-bi-workspace.png)

2. Válassza az **Adathalmazok** lapot, amivel megjelenítheti a munkaterület összes adathalmazát. Ezt az **Adathalmaz** tartalomnézeti listájának nevezzük.
   
   ![adatkészletek listája](./media/end-user-report-open/power-bi-dataset.png)

1. Keresse meg az adathalmazt, és válassza a **Jelentés létrehozása** ikont, amellyel az adathalmazt Szerkesztési nézetben nyitja meg. A jelentést csak akkor tudja megnyitni, ha szerkesztési jogosultsággal rendelkezik hozzá. 
   
    ![adatkészlet a Jelentés létrehozása ikonnal](./media/end-user-report-open/power-bi-create-report.png)

3. Az adathalmaz megnyílik a jelentésszerkesztőben. A jobb oldalon találja az adatmezőket. Ezeket használva máris elkezdheti a vizualizációk létrehozását. 

   ![A jelentésvászon](./media/end-user-report-open/power-bi-blank-canvas.png)

##  <a name="still-more-ways-to-open-a-report"></a>További lehetőségek a jelentés megnyitására
Ha már otthonosabban mozog a Power BI szolgáltatásban, minden bizonnyal tudni fogja, mely munkafolyamatok a legkényelmesebbek az Ön számára. Íme még néhány további lehetőség a jelentések megnyitásához:
- A bal oldali navigációs panelen válassza a **Kedvencek**, **Legutóbbi**, **Alkalmazások** elemet, majd a **Velem megosztott** lehetőséget. 
- A [Kapcsolódó megtekintése](end-user-related.md) használata
- E-mailben, ha valaki [Önnel osztott meg](../service-share-reports.md) jelentést, vagy ha [Riasztást állít be](../service-set-data-alerts.md).    
- Az [Értesítési központból](end-user-notification-center.md)    
- és még néhány további lehetőség

## <a name="next-steps"></a>Következő lépések
A [Power BI jelentéseiről itt talál](end-user-reports.md) további információkat

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)  

