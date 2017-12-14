---
title: "Nagy méretű számot tartalmazó csempe létrehozása a Kérdések és válaszok felületről"
description: "Nagy méretű számot tartalmazó csempe létrehozása Power BI-irányítópultokon kérdések feltevésével"
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
ms.date: 09/26/2017
ms.author: mihart
ms.openlocfilehash: 559484c341ec017890a4075a393d5ce211843b5f
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="create-a-big-number-tile-from-qa"></a>Nagy méretű számot tartalmazó csempe létrehozása a Kérdések és válaszok felületről
Néha csupán egyetlen szám a legfontosabb, amit nyomon szeretne követni a Power BI-irányítópulton, például a teljes értékesítés, az egy évre vetített piaci részesedés, vagy a lehetőségek száma. [Nagy méretű számot tartalmazó csempét a Power BI-jelentésekben](power-bi-visualization-big-number-report.md) vagy kérdések feltevésével a Kérdések és válaszok mezőben hozhat létre. Ez a cikk a Kérdések és válaszok mező használatával való létrehozást ismerteti.

![](media/power-bi-visualization-big-number/pbi_opptuntiescard.png)

Ilyen számcsempék legkönnyebben a kérdés mező segítségével hozhatók létre.

1. Hozzon létre egy [irányítópultot](service-dashboards.md), és [kérje le az adatokat](service-get-data.md). Ebben a példában a [Lehetőségelemzési mintát](sample-opportunity-analysis.md) használjuk.
2. Az irányítópult tetején angolul kezdje beírni a kérdés mezőbe, hogy mire is kíváncsi az adatokkal kapcsolatban. Ebben a példában a Lehetőségelemzési mintát használjuk.
   
   ![](media/power-bi-visualization-big-number/power-bi-q-and-a-box.png)
3. Például írja be a „number of opportunities” (lehetőségek száma) kifejezést a kérdés mezőbe.
   
   ![](media/power-bi-visualization-big-number/power-bi-ask.png)
   
   A kérdés mező ekkor javaslatot tesz, és módosítja az értéket a **Showing opportunity count** (Lehetőségek számának megjelenítése) kifejezésre, és megjeleníti a tényleges mennyiséget.  
4. A számcsempét a jobb felső sarokban lévő kitűzési ikonnal ![](media/power-bi-visualization-big-number/pbi_pintile.png) adhatja hozzá az irányítópulthoz. 
   
   ![](media/power-bi-visualization-big-number/power-bi-pin.png)
5. A csempét egy meglévő vagy egy új irányítópultra is rögzítheti. 
   
   * Meglévő irányítópult: válassza ki az irányítópult nevét a legördülő listából. Csak az aktuális munkaterületen lévő irányítópultok közül választhat.
   * Új irányítópult: írja be az új irányítópult nevét, és az létrejön a munkaterületen.
6. Válassza a **Rögzítés** lehetőséget.
   
   A rendszer egy sikert jelző üzenettel (a jobb felső sarokban) tájékoztatja, hogy a vizualizáció csempeként hozzá lett adva az irányítópulthoz.  
   
   ![](media/power-bi-visualization-big-number/power-bi-success.png)
7. Az új csempe megtekintéséhez válassza az **Ugrás az irányítópultra** lehetőséget. Itt [többek közt átnevezheti, átméretezheti és áthelyezheti a csempét az irányítópulton, és hiperhivatkozást adhat hozzá](service-dashboard-edit-tile.md). 
   
   ![](media/power-bi-visualization-big-number/power-bi-pinned.png)

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
Ha a kereső mező nem látható, forduljon a rendszerszintű vagy a bérlői rendszergazdához.

## <a name="next-steps"></a>További lépések
[A Power BI-irányítópultok csempéi](service-dashboard-tiles.md)  
[A Power BI-irányítópultok](service-dashboards.md)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

