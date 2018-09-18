---
title: Power BI-vizualizációk optimalizálása bármely méretre
description: Itt megismerheti a Power BI Desktopban és a Power BI telefonos alkalmazások Power BI szolgáltatásában meglévő jelentésvizualizációk optimalizálásának folyamatát.
author: maggiesMSFT
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 04/13/2018
ms.author: maggies
LocalizationGroup: Create reports
ms.openlocfilehash: d85d4bd60c341ef588cf56b1345f28aa25b810de
ms.sourcegitcommit: 67336b077668ab332e04fa670b0e9afd0a0c6489
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/12/2018
ms.locfileid: "44744087"
---
# <a name="optimize-a-power-bi-visual-for-any-size"></a>Power BI-vizualizációk optimalizálása bármely méretre
Ha létrehoz egy új jelentést, akkor alapértelmezés szerint a vizualizációk *rugalmasak*: dinamikusan módosulnak, hogy a lehető legtöbb adatot jelenítsék meg a képernyő méretétől függően. Régebbi jelentések esetén is beállíthatja, hogy a vizualizációk dinamikusan átméreteződjenek.

A vizualizáció méretének változásával a Power BI átrangsorolja az adatnézet elemeit, például eltávolítja a kitöltéseket, vagy automatikusan áthelyezi a jelmagyarázatot a vizualizáció tetejére, hogy az egyre kisebb méretű vizualizáció változatlanul áttekinthető maradjon. Az ilyen rugalmas elrendezés különösen hasznos a telehonokon futó Power BI mobilalkalmazásban lévő vizualizációk esetében.

![Rugalmas vizualizációk átméretezése](./media/desktop-create-responsive-visuals/power-bi-responsive-visual.gif)

Bármely X és Y tengellyel és szeletelőkkel rendelkező vizualizáció esetében bekapcsolható a rugalmasság.

## <a name="turn-on-responsiveness-in-power-bi-desktop"></a>A rugalmasság bekapcsolása a Power BI Desktopban
1. Régebbi jelentés esetében a Power BI Desktop **Nézet** lapján ellenőrizze, hogy **Asztali elrendezésben** van-e beállítva.
   
    ![Asztali elrendezés ikon](./media/desktop-create-responsive-visuals/power-bi-desktop-layout.png)
2. Válasszon ki egy vizualizációt, majd a **Vizualizációk** ablaktáblán válassza a **Formátum** szakaszt.
3. Bontsa ki az **Általános** elemet, és állítsa a **Rugalmas** kapcsolót **Be** állásba.
   
    ![Rugalmasság bekapcsolva](././media/desktop-create-responsive-visuals/power-bi-turn-responsive-on.png)
   
     Ekkor [a telefonra optimalizált jelentések létrehozásakor](../desktop-create-phone-report.md) ez a vizualizáció szépen átméreteződik a hozzáadás után.

## <a name="turn-on-responsiveness-in-the-power-bi-service"></a>A rugalmasság bekapcsolása a Power BI szolgáltatásban
A rugalmas viselkedést bekapcsolhatja a Power BI szolgáltatás jelentéseiben lévő vizualizációknál is. Ehhez szerkesztési jogosultsággal kell rendelkeznie a jelentésben.

1. A Power BI szolgáltatásban ([https://powerbi.com](https://powerbi.com)) válassza a **Jelentés szerkesztése** lehetőséget.
2. Válasszon ki egy vizualizációt, majd a **Vizualizációk** ablaktáblán válassza a **Formátum** szakaszt.
3. Bontsa ki az **Általános** elemet, és állítsa a **Rugalmas** kapcsolót **Be** állásba.
   
    ![Rugalmasság bekapcsolva](././media/desktop-create-responsive-visuals/power-bi-turn-responsive-on.png)
   
     Ekkor [a jelentés telefonos nézetének létrehozásakor](../desktop-create-phone-report.md) ez a vizualizáció szépen átméreteződik a hozzáadás után.

## <a name="next-steps"></a>Következő lépések
* [A Power BI telefonos alkalmazásokhoz optimalizált jelentések létrehozása](../desktop-create-phone-report.md)
* [Telefonra optimalizált Power BI-jelentések megtekintése](../consumer/mobile/mobile-apps-view-phone-report.md)
* További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

