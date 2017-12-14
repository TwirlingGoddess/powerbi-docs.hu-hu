---
title: "Power BI-vizualizációk optimalizálása bármely méretre"
description: "Itt megismerheti a Power BI Desktopban és a Power BI telefonos alkalmazások Power BI szolgáltatásában lévő vizualizációk optimalizálásának folyamatát."
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
ms.date: 10/13/2017
ms.author: maggies
ms.openlocfilehash: a059c01d6e9e08851434f71a1f36ac096054e291
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="optimize-a-power-bi-visual-for-any-size"></a>Power BI-vizualizációk optimalizálása bármely méretre
Beállíthatja, hogy az irányítópulton vagy a jelentésben lévő vizualizációk *rugalmas* elrendezésűek legyenek, és a képernyő méretétől függően dinamikusan a lehető legtöbb adatot és elemzést jelenítsék meg egyszerre.

A vizualizáció méretének változásával a Power BI átrangsorolja az adatnézet elemeit, például eltávolítja a kitöltéseket, vagy automatikusan áthelyezi a jelmagyarázatot a vizualizáció tetejére, hogy az egyre kisebb méretű vizualizáció változatlanul áttekinthető maradjon. Az ilyen rugalmas elrendezés különösen hasznos a telehonokon futó Power BI mobilalkalmazásban lévő vizualizációk esetében.

![Rugalmas vizualizációk átméretezése](media/desktop-create-responsive-visuals/power-bi-responsive-visual.gif)

Bármely X és Y tengellyel és szeletelőkkel rendelkező vizualizáció esetében bekapcsolható a rugalmasság.

## <a name="turn-on-responsiveness-in-power-bi-desktop"></a>A rugalmasság bekapcsolása a Power BI Desktopban
1. A Power BI Desktop **Nézet** lapján ellenőrizze, hogy **Asztali elrendezésben** van-e.
   
    ![Asztali elrendezés ikon](media/desktop-create-responsive-visuals/power-bi-desktop-layout.png)
2. Válasszon ki egy vizualizációt, majd a **Vizualizációk** ablaktáblán válassza a **Formátum** szakaszt.
3. Bontsa ki az **Általános** elemet, és állítsa a **Rugalmas** kapcsolót **Be** állásba.
   
    ![Rugalmasság bekapcsolva](media/desktop-create-responsive-visuals/power-bi-turn-responsive-on.png)
   
     Ekkor [a telefonra optimalizált jelentések létrehozásakor](desktop-create-phone-report.md) ez a vizualizáció szépen átméreteződik a hozzáadás után.

## <a name="turn-on-responsiveness-in-the-power-bi-service"></a>A rugalmasság bekapcsolása a Power BI szolgáltatásban
Bekapcsolhatja a Power BI szolgáltatás jelentéseiben lévő vizualizáció rugalmasan viselkedjenek. Ehhez szerkesztési jogosultsággal kell rendelkeznie a jelentésben.

1. A Power BI szolgáltatásban ([https://powerbi.com](https://powerbi.com)) válassza a **Jelentés szerkesztése** lehetőséget a jelentésben.
2. Válasszon ki egy vizualizációt, majd a **Vizualizációk** ablaktáblán válassza a **Formátum** szakaszt.
3. Bontsa ki az **Általános** elemet, és állítsa a **Rugalmas** kapcsolót **Be** állásba.
   
    ![Rugalmasság bekapcsolva](media/desktop-create-responsive-visuals/power-bi-turn-responsive-on.png)
   
     Ekkor [az irányítópult telefonos nézetének létrehozásakor](service-create-dashboard-mobile-phone-view.md) ez a vizualizáció szépen átméreteződik a hozzáadás után.

## <a name="next-steps"></a>További lépések
* [A Power BI telefonos alkalmazásokhoz optimalizált jelentések létrehozása](desktop-create-phone-report.md)
* [Power BI-irányítópult telefonos nézetének létrehozása](service-create-dashboard-mobile-phone-view.md)
* [Telefonra optimalizált Power BI-jelentések megtekintése](mobile-apps-view-phone-report.md)
* További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

