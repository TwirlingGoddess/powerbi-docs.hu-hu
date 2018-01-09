---
title: "A Power BI szolgáltatás jelentéseinek Olvasó és Szerkesztési nézete"
description: "A Power BI szolgáltatás jelentéseinek Olvasó és Szerkesztési nézete közötti különbségek általános áttekintése"
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
ms.date: 12/21/2017
ms.author: mihart
ms.openlocfilehash: 7c0c09bd04eac31bac00e4562853c99befe9715f
ms.sourcegitcommit: 6ea8291cbfcb7847a8d7bc4e2b6abce7eddcd0ea
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/21/2017
---
# <a name="reading-view-and-editing-view-in-power-bi-service-reports"></a>A Power BI szolgáltatás jelentéseinek Olvasó és Szerkesztési nézete
A Power BI szolgáltatásban a jelentések két módban tekinthetők meg és kezelhetők: az Olvasó és a Szerkesztési nézetben (a Power BI Desktopban nem).  

Az Olvasó nézet minden felhasználó számára elérhető, míg a Szerkesztési nézet csak a jelentések létrehozói és tulajdonosai számára érhető el. Az Olvasó nézet a jelentések *felhasználói* számára van kialakítva, vagyis azon munkatársak számára, akik az alkalmazásokban nyitnak meg jelentéseket, vagy akikkel jelentések vannak megosztva. Az Olvasó nézet biztosítja, hogy az adott jelentés minden egyes felhasználója számára ugyanaz a jelentés és ugyanazok a vizualizációk jelenjenek meg, azonos alkalmazott szűrőkkel.  A felhasználók kezelhetik a jelentéseket, azonban nem tudják menteni a módosításokat.

>**MEGJEGYZÉS**: Bizonyos esetekben előfordulhat, hogy a jelentés felhasználói számára a sorszintű biztonság és az adatokra vonatkozó engedélyek miatt eltérő adatok jelennek meg. 

A Szerkesztési nézet csak a jelentés létrehozói számára, vagy azok számára érhető el, akik egy alkalmazás-munkaterület tagjaként vagy rendszergazdájaként a jelentés társtulajdonosai.

## <a name="reading-view"></a>Olvasó nézet

Az Olvasó nézetben nyugodtan kísérletezhet az adatokkal, és egy biztonságos környezetben tárhatja fel őket. Az Olvasó nézet nem annyira interaktív, mint a [Szerkesztő nézet](service-interact-with-a-report-in-editing-view.md), azonban így is sok lehetőséget biztosít az adatok feltárására. Ez például akkor lehet hasznos, ha [megosztanak Önnel](service-share-dashboards.md) egy jelentést, ugyanis az csak Olvasó nézetben nyitható meg.

További tudnivalókért lásd: [A Power BI-jelentések Olvasó nézete](service-interact-with-a-report-in-reading-view.md).

## <a name="editing-view"></a>Szerkesztési nézet
A Power BI Szerkesztési nézetében (az [Olvasás nézethez](service-interact-with-a-report-in-reading-view.md) képest) mélyebbre áshat az adatok közt mezők felvételével és eltávolításával, a vizualizáció típusának a módosításával, új vizualizációk létrehozásával, valamint vizualizációk jelentésbe történő felvételével illetve törlésével.

További tudnivalókért lásd: [A Power BI-jelentések Szerkesztési nézete](service-interact-with-a-report-in-editing-view.md)

## <a name="navigating-between-editing-view-and-reading-view"></a>A Szerkesztési és az Olvasó nézet közötti váltás
Ne feledje, hogy a jelentéseket csak azok létrehozói és tulajdonosai tudják majd Szerkesztési nézetben megnyitni.

1. A jelentések alapértelmezés szerint általában Olvasó nézetben nyílnak meg. Az mutatja, hogy Olvasó nézetben van, hogy megjelenik a **Jelentés szerkesztése** lehetőség. Ha a **Jelentés szerkesztése** lehetőség szürke színnel jelenik meg, nem rendelkezik a jelentés Szerkesztési nézetében való megnyitásához szükséges engedélyekkel.

   ![](media/service-reading-view-and-editing-view/power-bi-edit-report-grey.png)

2. Ha a **Jelentés szerkesztése** lehetőség nem szürke színnel jelenik meg, ezt választva nyithatja meg a jelentést Szerkesztési nézetben. 
   
   ![](media/service-reading-view-and-editing-view/power-bi-edit-report.png)
   
   A jelentés most már Szerkesztési nézetben látható, ugyanazokkal a [megjelenítési beállításokkal](power-bi-report-display-settings.md), melyeket legutóbb használt az Olvasó nézetben.

2. Az Olvasó nézetbe való visszalépéshez válassza az **Olvasó nézet** lehetőséget a felső menüsávban.
   
    ![](media/service-reading-view-and-editing-view/power-bi-reading-view.png)

Számtalan különböző módon kezelheti a jelentéseket az Olvasó nézetben, tovább szeletelve és darabolva az adatokat összefüggések feltárásához és kérdések megválaszolásához.  Ezeket a következő, [Jelentések kezelése az Olvasó nézetben](service-interact-with-a-report-in-editing-view.md) című téma sorolja fel és ismerteti részletesebben.

### <a name="next-steps"></a>Következő lépések
[Jelentések kezelése az Olvasó nézetben](service-interact-with-a-report-in-editing-view.md)    
Vissza a [Power BI-jelentésekhez](service-reports.md)    
További kérdései vannak? [Felteheti azokat a Power BI-közösségnek](http://community.powerbi.com/) 

