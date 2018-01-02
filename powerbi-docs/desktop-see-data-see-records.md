---
title: "Adatok és rekordok megtekintés a Power BI Desktop vizualizációiban"
description: "A Power BI Desktop Adatok megjelenítése és Rekordok megjelenítése funkciójának használata a részletek feltárásához"
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 10/09/2017
ms.author: davidi
ms.openlocfilehash: c43ec48d1bd34a5df2578c6cc117dd3e3bbdb64f
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="use-see-data-and-see-records-in-power-bi-desktop"></a>A Power BI Desktop Adatok megjelenítése és Rekordok megjelenítése funkciójának használata
A **Power BI Desktopban** bármelyik vizualizációt részletesen feltárhatja, és megtekintheti az adatok szöveges alakját vagy a kijelölt vizualizáció egyes adatelemeit. Ezeket a szolgáltatásokat időnként *átkattintásnak*, *áthatolásnak* vagy *részletezésnek* is nevezik.

A **Rekordok megjelenítése** segítségével megtekinthet egy vizualizáció kijelölt adatelemének alapjául szolgáló sorokat, az **Adatok megjelenítése** segítségével pedig megtekintheti a vizualizációban használt értékek szöveges verzióját. Az **Adatok megjelenítése** és a **Rekordok megjelenítése** funkciók használatára vonatkoznak bizonyos, a cikk végén tárgyalt korlátozások.

![](media/desktop-see-data-see-records/see-data-see-records_1.png)

## <a name="using-see-data-in-power-bi-desktop"></a>Az Adatok megjelenítése funkció használata Power BI Desktopban
Az **Adatok megjelenítése** gomb az **Adatok/Részletezés** lapon érhető el, a menüszalag **Vizuális eszközök** szakaszán.

![](media/desktop-see-data-see-records/see-data-see-records_2.png)

Az **Adatok megjelenítése** úgy is használható, ha jobb gombbal egy vizualizációra kattint, és a megjelenő menüben kiválasztja az **Adatok megjelenítése** lehetőséget.

![](media/desktop-see-data-see-records/see-data-see-records_3.png)

> [!NOTE]
> A mutatót a vizualizáció egy adatpontja fölé kell vinnie, hogy elérhető legyen a helyi menü.
> 
> 

Amikor kiválasztja az **Adatok megjelenítése** elemet, a **Power BI Desktop** a kiválasztott vizualizációra és adatokra koncentrál, és a vászon területét az adatok vizuális és szöveges megjelenítésének szenteli. A vizualizáció a vászon felső felén jelenik meg, az adatok pedig az alsó felén látszanak, ahogy az alábbi ábrán is látható. Ez a *vízszintes* nézet.

![](media/desktop-see-data-see-records/see-data-see-records_4.png)

A jobb felső sarokban található ikonnal válthat *függőleges nézetre* (vagy vissza *vízszintesre*).

![](media/desktop-see-data-see-records/see-data-see-records_5.png)

A jelentéshez való visszatéréshez válassza a **< Vissza a jelentéshez** lehetőséget a vászon bal felső sarkában.

![](media/desktop-see-data-see-records/see-data-see-records_6.png)

## <a name="using-see-records-in-power-bi-desktop"></a>A Rekordok megjelenítése funkció használata Power BI Desktopban
Azt is megteheti, hogy egy vizualizáció egyik adatelemére koncentrál, és részletesen megvizsgálhatja annak mögöttes adatait. Ha kijelölt egy vizualizációt, két módon használhatja a **Rekordok megjelenítése** funkciót: kapcsolja be a **Rekordok megjelenítése** váltógombot az **Adatok/Részletezés** menüszalagon, és kattintson egy adatelemre, vagy kattintson a jobb gombbal egy adatelemre, és válassza a megjelenő menüben a **Rekordok megjelenítése** lehetőséget.

![](media/desktop-see-data-see-records/see-data-see-records_7.png)

> [!NOTE]
> Ha a kiválasztott vizualizáció nem támogatja a **Rekordok megjelenítése** funkciót, a menüszalagon kiszürkítve jelenik meg a gomb.
> 
> 

Ha kiválasztotta a **Rekordok megjelenítése** lehetőséget, a **Power BI Desktop** arra az egy adatelemre koncentrál, és a vászon területét az elemhez tartozó adatok megjelenítésének szenteli, amint az alábbi ábrán is látható.

![](media/desktop-see-data-see-records/see-data-see-records_8.png)

A jelentéshez való visszatéréshez válassza a **Vissza a jelentéshez** gombot a vászon bal felső sarkában.

## <a name="limitations"></a>Korlátozások
Az **Adatok megjelenítése** vagy a **Rekordok megjelenítése** használatakor figyelembe kell vennie a következő korlátozásokat:

* Csak következő vizualizációtípusok támogatottak:
  * **Sáv**
  * **Oszlop**
  * **Térkép**
  * **Faszerkezetes térkép**
  * **Kartogram**
  * **Torta**
  * **Fánk**
  * **Tölcsér**
* A **Rekordok megjelenítése** nem használható, ha a vizualizáció kiszámított mértéket használ.
* A **Rekordok megjelenítése** nem használható, ha egy élő többdimenziós (multidimensional, MD) modellt használ.

## <a name="next-steps"></a>Következő lépések
A **Power BI Desktopban** sokféle jelentésformázási és adatkezelési szolgáltatás érhető el. A következő forrásanyagok ezekből ismertetnek néhányat:

* [Csoportosítás és dobozolás használata a Power BI Desktopban](desktop-grouping-and-binning.md)
* [Rácsvonalak, rácshoz illesztés, mélységi (Z) index, igazítás és disztribúció használata a Power BI Desktop-jelentésekben](desktop-gridlines-snap-to-grid.md)

