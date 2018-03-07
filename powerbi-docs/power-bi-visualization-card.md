---
title: "Kártyavizualizációk (más néven nagy méretű numerikus csempék)"
description: "Kártyavizualizáció létrehozása a Power BI-ban"
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
ms.date: 12/24/2017
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: f38f3bb19be268cba4745c88aa98d09c080c773e
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="card-visualizations"></a>Kártyavizualizációk
Néha csupán egyetlen szám a legfontosabb, amit nyomon szeretne követni a Power BI-irányítópulton vagy -jelentésben, például az összesített értékesítés, az egy évre vetített piaci részesedés, vagy a lehetőségek száma összesen. Az ilyen típusú vizualizációkat *Kártyáknak* nevezzük. Csakúgy, mint szinte minden natív Power BI-vizualizáció, a Kártyák is a jelentésszerkesztővel vagy a Q&A-val hozhatók létre.

![kártyavizualizáció](media/power-bi-visualization-card/pbi_opptuntiescard.png)

## <a name="create-a-card-using-the-report-editor"></a>Kártyák létrehozása a jelentésszerkesztővel
Ez az útmutatás a Kiskereskedelmi elemzési mintát használja. Annak érdekében, hogy követni tudja a lépéseket, [töltse le a mintát](sample-datasets.md), mely a Power BI szolgáltatásban (az app.powerbi.com webhelyen) vagy a Power BI Desktopban használható.   

1. Kezdjen egy [üres jelentésoldalon](power-bi-report-add-page.md), és válassza a **Store** \> **Open store count** (Üzlet > Nyitva lévő üzletek száma) mezőt. Ha a Power BI szolgáltatást használja, a [Szerkesztési nézetében](service-interact-with-a-report-in-editing-view.md) kell megnyitnia a jelentést.

    A Power BI létrehoz egy oszlopdiagramot ezzel az egy számmal.

   ![](media/power-bi-visualization-card/pbi_rptnumbertilechart.png)
2. A Megjelenítések ablaktáblán kattintson a Kártya ikonra.

   ![](media/power-bi-visualization-card/pbi_changechartcard.png)
6. A vizualizáció az irányítópulton való rögzítéséhez vigye a kurzort a kártya fölé, és válassza a rögzítés ikonját ![](media/power-bi-visualization-card/pbi_pintile.png).

   ![](media/power-bi-visualization-card/power-bi-pin-icon.png)
7. A csempét egy meglévő vagy egy új irányítópultra is rögzítheti.

   * Meglévő irányítópult: válassza ki az irányítópult nevét a legördülő listából.
   * Új irányítópult: írja be az új irányítópult nevét.
8. Válassza a **Rögzítés** lehetőséget.

   Megjelenik egy üzenet (a jobb felső sarok közelében), amely értesíti, hogy sikeresen hozzáadta a vizualizációt az irányítópultjához csempeként.

   ![](media/power-bi-visualization-card/power-bi-pin-success-message.png)
9. Válassza az **Ugrás az irányítópultra** lehetőséget. Itt [szerkesztheti és áthelyezheti](service-dashboard-edit-tile.md) a rögzített vizualizációt.


## <a name="create-a-card-from-the-qa-question-box"></a>Kártya létrehozása a Q&A kérdésmezőben
Kártyák legkönnyebben a Q&A kérdésmezőben hozhatók létre. A Q&A kérdésmező a Power BI szolgáltatásban (az app.powerbi.com webhelyen) irányítópultokon és jelentésekben érhető el. A következő lépések azt írják le, hogyan hozható létre egy Kártya a Power BI szolgáltatás irányítópultjain. Ha a Power BI Desktopban szeretne létrehozni egy kártyát a Q&A-val, a Q&A a Desktophoz készült előzetes verziójának jelentései esetében [ezt az útmutatást kövesse](https://powerbi.microsoft.com/en-us/blog/power-bi-desktop-december-feature-summary/#QandA).

1. Hozzon létre egy [irányítópultot](service-dashboards.md), és [kérje le az adatokat](service-get-data.md). Ebben a példában a [Lehetőségelemzési mintát](sample-opportunity-analysis.md) használjuk.

1. Az irányítópult tetején angolul kezdje beírni a kérdés mezőbe, hogy mire is kíváncsi az adatokkal kapcsolatban. 

   ![](media/power-bi-visualization-card/power-bi-q-and-a-box.png)

>**TIPP**: A Power BI szolgáltatás jelentéseiben, a [Szerkesztési nézetben](service-reading-view-and-editing-view.md) válassza a **Kérdés feltevése** lehetőséget a felső menüsorban. A Power BI Desktop jelentéseiben keressen egy üres területet a jelentésben, majd kattintson rá duplán a kérdésmező megnyitásához.

3. Például írja be a „number of opportunities” (lehetőségek száma) kifejezést a kérdés mezőbe.

   ![](media/power-bi-visualization-card/power-bi-q-and-a.png)

   A kérdésmező javaslatokkal és újrafogalmazásokkal segíti, és végül megjeleníti az összesített számot.  
4. A kártyát a jobb felső sarokban lévő rögzítési ikonnal ![](media/power-bi-visualization-card/pbi_pintile.png) adhatja hozzá egy irányítópulthoz.

   ![](media/power-bi-visualization-card/power-bi-pin.png)
5. A kártyát egy meglévő vagy egy új irányítópulton is rögzítheti csempeként.

   * Meglévő irányítópult: válassza ki az irányítópult nevét a legördülő listából. Csak az aktuális munkaterületeken lévő irányítópultok közül választhat.
   * Új irányítópult: írja be az új irányítópult nevét, és az létrejön a munkaterületen.
6. Válassza a **Rögzítés** lehetőséget.

   A jobb felső sarokban megjelenik a sikert jelző üzenet, amely tájékoztatja arról, hogy a vizualizáció csempeként hozzá lett adva az irányítópulthoz.  

   ![](media/power-bi-visualization-card/power-bi-success.png)
7. Az új csempe megtekintéséhez kattintson az **Ugrás az irányítópultra** lehetőségre. Itt [többek között átnevezheti, átméretezheti és áthelyezheti a csempét az irányítópulton, és hivatkozást adhat hozzá](service-dashboard-edit-tile.md).

   ![](media/power-bi-visualization-card/power-bi-pinned.png)

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
- Ha a kereső mező nem látható, forduljon a rendszerszintű vagy a bérlői rendszergazdához.    
- Ha a Power BI Desktopot használja, és nem jelenik meg a Q&A, amikor duplán kattint egy üres területre egy jelentésben, lehetséges, hogy engedélyeznie kell azt.  Válassza a **Fájl > Lehetőségek és beállítások > Beállítások > Előzetes verziójú funkciók > Q&A** lehetőséget, majd indítsa újra a Power BI Desktopot.


## <a name="next-steps"></a>Következő lépések
[Irányítópult-csempék a Power BI-ban](service-dashboard-tiles.md)

[Irányítópultok a Power BI-ban](service-dashboards.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)
