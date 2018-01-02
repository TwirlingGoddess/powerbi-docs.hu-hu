---
title: "Csoportosítás és dobozolás használata a Power BI Desktopban"
description: "Megismerheti az elemek csoportosításának és dobozolásának folyamatát a Power BI Desktopban"
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: 801adc4ddb22536e46273d2639b4a1f0b9496cca
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="use-grouping-and-binning-in-power-bi-desktop"></a>Csoportosítás és dobozolás használata a Power BI Desktopban
Amikor a **Power BI Desktop** vizualizációkat hoz létre, az adatait az alapul szolgáló adatokban talált értékek alapján adattömbökbe (vagy **csoportokba**) gyűjti. Ez gyakran elegendő is, de lehetnek alkalmak, amikor finomítani szeretné az adattömbök megjelenítését. Előfordulhat például, hogy három termékkategóriát egy nagyobb kategóriában (egy *csoportban*) szeretne elhelyezni. Az is előfordulhat, hogy az eladási adatokat 1 000 000 dollár méretű dobozokban szeretné látni, nem pedig egyenlően elosztva, 923 983 dolláros részekben.

A Power BI Desktopban **csoportosíthatja** az adatokat, és így jobban áttekintheti, elemezheti és feltárhatja a vizualizációkban foglalt adatokat és tendenciákat. A **dobozméretet** is meghatározhatja. A folyamatot, amelynek során az értékeket egyenlő méretű csoportokra osztja, gyakran **dobozolásnak** nevezik, és ez lehetővé teszi az adatok könnyebben értelmezhető vizualizációját.

### <a name="using-grouping"></a>A csoportosítás használata
A **csoportosítás** használatához a CTRL+KATTINTÁSSAL válasszon ki két vagy több elemet egy vizualizáción. Ezután kattintson a jobb gombbal a több kijelölt elem egyikére, és válassza a *Csoport* lehetőséget a megjelenő menüben.

![](media/desktop-grouping-and-binning/grouping-binning_1.png)

Ha létrejött a csoport, a rendszer hozzáadja a vizualizáció **Jelmagyarázat** gyűjtőjéhez, és a **Mezők** listában is megjelenik.

![](media/desktop-grouping-and-binning/grouping-binning_2.png)

Ha már van egy csoportja, egyszerűen szerkesztheti a csoport tagjait. Ehhez kattintson a jobb gombbal a mezőre a **Jelmagyarázat** gyűjtőben vagy a **Mezők** listán, és válassza a *Csoportok szerkesztése* lehetőséget.

![](media/desktop-grouping-and-binning/grouping-binning_3.png)

A megjelenő **Csoportok** ablakban létrehozhat új csoportokat, vagy módosíthatja a meglévőket. A csoportokat *át is nevezheti*. Ehhez kattintson duplán a **Csoportok és tagok** mezőben a **Csoport** címre, és írjon be egy új nevet.

Ebben az ablakban sokféle műveletet elvégezhet a csoportokon. Hozzáadhat elemeket a **Nem csoportosított értékek** listáról egy új vagy egy létező csoporthoz. Új csoport létrehozásához válasszon ki két vagy több elemet (a CTRL+kattintással) a **Nem csoportosított értékek** mezőből, és kattintson a mező alatti **Csoport** gombra.

Hozzáadhat egy nem csoportosított értéket egy létező csoporthoz: csak válassza ki a nem csoportosított értéket, aztán válassza ki a meglévő csoportot, amelybe fel szeretné venni, és kattintson a **Csoport** gombra. Ha el szeretne távolítani egy elemet egy csoportból, válassza ki a **Csoportok és tagok** mezőben, és kattintson a **Csoportosítás megszüntetése** parancsra. Azt is eldöntheti, hogy a nem csoportosított kategóriák bekerüljenek-e az **Egyéb** csoportba, vagy maradjanak csoportosítás nélkül.

![](media/desktop-grouping-and-binning/grouping-binning_4.png)

> [!NOTE]
> A **Mezők** szakasz bármelyik mezőjéhez létrehozhat csoportokat, ehhez nem kell egy meglévő vizualizációból több elemet kijelölnie. Csak kattintson a jobb gombbal a mezőre, és válassza a megjelenő menüben a **Csoport** elemet.
> 
> 

### <a name="using-binning"></a>A dobozolás használata
A dobozméretet a **Power BI Desktop** numerikus és időmezőihez állíthatja be. A dobozolással megfelelő méretűre állíthatja a **Power BI Desktop** által megjelenített adatokat.

Egy dobozméret alkalmazásához kattintson a jobb gombbal egy **Mezőre**, és válassza a **Csoportok** lehetőséget.

![](media/desktop-grouping-and-binning/grouping-binning_5.png)

A **Csoportok** ablakban állítsa be a **Doboz méretét** a kívánt értékre.

![](media/desktop-grouping-and-binning/grouping-binning_6.png)

Amikor az **OK** gombra kattint, észreveheti, hogy megjelenik a **Mezők** panelen egy új mező, amelyhez hozzá van fűzve a *(bins)* (dobozok) kifejezés. Ezután ezt a mezőt ráhúzhatja a vászonra, ha a dobozméretet alkalmazni szeretné egy vizualizációban.

![](media/desktop-grouping-and-binning/grouping-binning_7.png)

Ha működés közben szeretné látni a **dobozolást**, tekintse meg ezt a [videót](https://youtu.be/UXEYSvgvMaQ?t=12m17s).

Mindössze ennyit kell tudni a **csoportosítás** és a **dobozolás** használatáról, hogy a jelentéseiben szereplő vizualizációk pont úgy jelenítsék meg az adatokat, ahogyan szeretné.

