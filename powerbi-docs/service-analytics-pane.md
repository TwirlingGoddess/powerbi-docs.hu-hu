---
title: "Az Elemzés panel a Power BI szolgáltatásban"
description: "Dinamikus referenciavonalak létrehozása vizualizációkhoz a Power BI szolgáltatásban"
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
ms.date: 05/02/2017
ms.author: mihart
ms.openlocfilehash: 30fc0731f819f063aa04e856e8acc75a69f64a59
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="analytics-pane-in-power-bi-service"></a>Az Elemzés panel a Power BI szolgáltatásban
A **Power BI szolgáltatás** **Elemzés** paneljével dinamikus *referenciavonalak* adhatók a vizualizációkhoz, kiemelve a fontos trendeket vagy elemzési eredményeket.

![](media/service-analytics-pane/power-bi-analytics-pane.png)

> [!NOTE]
> Az **Elemzés** panel csak akkor jelenik meg, ha egy vizualizáció ki van jelölve a jelentés vásznon.
> 
> 

## <a name="using-the-analytics-pane"></a>Az Elemzés panel használata
Az **Elemzés** panelen a dinamikus referenciavonalak következő típusai hozhatók létre (nem minden vonal érhető el minden vizualizációtípushoz):

* Vízszintes konstans vonal
* Függőleges konstans vonal
* Minimum-vonal
* Maximum-vonal
* Átlag-vonal
* Középérték-vonal
* Százalékos érték-vonal

A következő szakaszok bemutatják az **Elemzés** panel és a dinamikus referenciavonalak vizualizációkon való használatát.

A vizualizációkhoz elérhető dinamikus referenciavonalak a következő lépések végrehajtásával jeleníthetők meg:

1. Jelöljön ki vagy hozzon létre egy vizualizációt, majd kattintson a **Megjelenítések** panel **Elemzés** ikonjára ![](media/service-analytics-pane/power-bi-analytics-icon.png).
2. Válassza a kívánt vonaltípus melletti lefelé mutató nyilat a lehetőségek kibontásához. Ebben a példában az **Átlag vonal** van kiválasztva.
   
   ![](media/service-analytics-pane/power-bi-add.png)
3. Új vonal létrehozásához válassza a **+ Hozzáadás** sort. A vonalnak nevet is adhat, ha kétszer a szövegmezőre kattint és begépeli a nevet.
   
   A vonalhoz sok beállítás megadható, például kiválasztható a *színe*, az *átlátszósága*, a *stílusa* és a *helyzete* (a vizualizáció adatelemeihez viszonyítva), és hogy tartozzon-e hozzá címke. Lényeges, hogy kiválaszthatja, melyik **Mérték** legyen a vonal alapja. Ehhez válassza a **Mérték** legördülő listát, amely automatikusan feltöltődik a vizualizáció adatelemeivel. Ebben a példában a *Nyitott üzletek száma* lesz kiválasztva mértéknek, *Átl # Nyitott üzletek* címkével, és néhány egyéni beállítással az alábbiak szerint.
   
   ![](media/service-analytics-pane/power-bi-average-line.png)
4. Ha szeretné, hogy megjelenjen egy adatcímke, húzza az **Adatcímke** kapcsolót a Be állásba. Ilyenkor az adatcímke számos további beállítása is megadható.
5. Figyelje meg az **Elemzés** panel **Átlag vonal** eleme mellett megjelenő számot. Ez adja meg a vizualizáción lévő dinamikus vonalak aktuális számát és típusát. Ha felvesz egy **Konstans vonalat** az üzletek számára kijelölt 9 célértékkel, akkor az **Elemzés** panelen látható, hogy már egy **Konstans vonal** referenciavonal is tartozik a vizualizációhoz.
   
   ![](media/service-analytics-pane/power-bi-reference-lines.png)
   
   Ha a kijelölt vizualizációra nem alkalmazhatók dinamikus referenciavonalak (ebben az esetben egy **Térkép** vizualizáció), akkor a következőt fogja látni az **Elemzés** panelen.
   
   ![](media/service-analytics-pane/power-bi-no-lines.png)

Sokféle érdekes elemzési eredmény kiemelhető az **Elemzés** panel használatával létrehozott dinamikus referenciavonalakkal.

Tervezünk további funkciókat és lehetőségeket, többek között a dinamikus referenciavonalakkal ellátható vizualizációk körének bővítését, ezért látogasson vissza gyakran az újdonságokért.

## <a name="limitations"></a>Korlátozások
A dinamikus referenciavonalak használatának lehetősége a használt vizualizáció típusától függ. Az alábbi lista bemutatja, hogy jelenleg mely dinamikus referenciavonalak mely vizualizációhoz használhatók:

A dinamikus vonalak teljes körűen használhatók az alábbi vizualizációkon:

* Területdiagram
* Vonaldiagram
* Pontdiagram
* Csoportosított oszlopdiagram
* Csoportosított sávdiagram

Az alábbi vizualizációkhoz csak *konstans vonal* vehető fel az **Elemzés** panelen:

* Halmozott terület
* Halmozott sáv
* Halmozott oszlop
* 100%-ig halmozott sáv
* 100%-ig halmozott oszlop

Az alábbi vizualizációkhoz jelenleg csak *trendvonal* érhető el:

* Nem halmozott vonal
* Csoportosított oszlopdiagram

Végül olyan, nem derékszögű koordináta-rendszerben ábrázolt vizualizációk következnek, amelyekhez nem vehető fel dinamikus vonal az **Elemzés** panelen:

* Mátrix
* Tortadiagram
* Gyűrű
* Táblázat

## <a name="next-steps"></a>További lépések
[Az Elemzés panel a Power BI Desktopban](desktop-analytics-pane.md)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

