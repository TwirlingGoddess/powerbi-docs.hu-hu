---
title: "A numerikustartomány-szeletelő használata a Power BI Desktopban"
description: "Megismerheti, hogyan használhatja a szeletelőt a numerikus tartományokra való korlátozásra a Power BI Desktopban"
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
ms.date: 02/05/2018
ms.author: davidi
ms.openlocfilehash: 6d63236254906619f7244db9f57af162a19a70d6
ms.sourcegitcommit: db37f5cef31808e7882bbb1e9157adb973c2cdbc
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2018
---
# <a name="use-the-numeric-range-slicer-in-power-bi-desktop"></a>A numerikustartomány-szeletelő használata a Power BI Desktopban
A **numerikustartomány-szeletelővel** számos különféle szűrőt alkalmazhat az adatmodellek bármely numerikus oszlopára. Választhat, hogy számok **között**, egy számnál **kisebb vagy egyenlő** vagy egy számnál **nagyobb vagy egyenlő** értékekre szűr. Egyszerűnek tűnik, de nagyon hatékony módja az adatok szűrésének.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_2.png)

## <a name="using-the-numeric-range-slicer"></a>A numerikustartomány-szeletelő használata
A numerikustartomány-szeletelőt bármely más szeletelőhöz hasonlóan használhatja. Egyszerűen hozzon létre egy **szeletelő** vizualizációt a jelentéshez, majd válasszon ki egy numerikus értéket a **Mező** értékeként. A következő képen a *UnitPrice* mező van kiválasztva.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_3.png)

Válassza ki a karátot a **numerikustartomány-szeletelő** jobb felső sarkában, és megjelenik egy menü.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_4.png)

Numerikus tartományok esetében a következő három lehetőség közül választhat:

* Között
* Kisebb vagy egyenlő
* Nagyobb vagy egyenlő

Amikor a **Között** lehetőséget választja a menüből, megjelenik egy csúszka, és a számok közé eső numerikus értékekre szűrhet. A csúszka használata mellett a mezőkre kattinthat és be is írhatja az értékeket. Ez kényelmes, amikor adott egész számok alapján szeretne szeletelni, de a szeletelősáv mozgatásának részletessége megnehezíti a pontos szám kiválasztását.

A következő képen a jelentésoldal az 500 és 1500 közötti tartományban lévő *UnitPrice* értékekre van szűrve.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_5.png)

Amikor a **Kisebb vagy egyenlő** lehetőséget választja, eltűnik a csúszkasáv bal oldali (legalacsonyabb értékhez tartozó) fogója, és csak a csúszka felső határát módosíthatjuk. A következő képen 497,17 értékre állítjuk a csúszkasávot.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_6.png)

Végül ha a **Nagyobb vagy egyenlő** lehetőséget választjuk, a csúszkasáv jobb oldali (legmagasabb értékhez tartozó) fogója tűnik el, és az alacsonyabb értéket módosíthatjuk a következő képen látható módon. Most csak a 750,56-nál nagyobb vagy azzal egyenlő *UnitPrice* értékek jelennek meg a jelentésoldal vizualizációiban.

![](media/desktop-slicer-numeric-range/slicer-numeric-range_7.png)

## <a name="snap-to-whole-numbers-with-the-numeric-range-slicer-preview"></a>Egész számhoz illeszkedés a numerikus szeletelőnél (előzetes verzió)

A **Power BI Desktop** 2018. februári kiadásától kezdve a numerikus szeletelő egész számokhoz illeszkedik. Ezzel lehetővé válik, hogy a szeletelőn egyszerűen válasszon ki egész számokat. Az egész számhoz illeszkedés nem vonatkozik a tizedes szűrőkre.


## <a name="limitations-and-considerations"></a>Korlátozások és szempontok
Jelenleg a következő korlátozások és szempontok érvényesek a **numerikustartomány-szeletelőre**

* A **numerikustartomány-szeletelő** jelenleg az adatokban lévő összes alapul szolgáló sorra szűr, nem az összesített értékekre. Ha például egy *Értékesítési összeg* mezőt használ, akkor az *Értékesítési összegen* alapuló összes tranzakcióra szűr, nem a vizualizáció egyes adatpontjai *Értékesítési összegének* összegére.
* Jelenleg nem működik a mértékekkel
* Jelenleg a **numerikustartomány-szeletelő** csak a **Power BI Desktopban** érhető el. Ha a **numerikustartomány-szeletelőt** használó egyik jelentés közzé van téve a **Power BI szolgáltatásban**, a szűrő továbbra is alkalmazva lesz, de listaszeletelőként jelenik meg.

