---
title: Beágyazott hierarchiák feliratainak használata a Power BI Desktopban
description: Beágyazott hierarchiák feliratainak használata a Power BI Desktopban
services: powerbi
documentationcenter: ''
author: davidiseminger
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 05/02/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 974194cb04701e2dc21814a0945227ad9c4b770c
ms.sourcegitcommit: f679c05d029ad0765976d530effde744eac23af5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/04/2018
---
# <a name="use-inline-hierarchy-labels-in-power-bi-desktop"></a>Beágyazott hierarchiák feliratainak használata a Power BI Desktopban
A **Power BI Desktop** támogatja a **beágyazott hierarchiák feliratainak** használatát. Ez azon két funkció egyike, amelyek a részletes hierarchikus kibontást javítják. A jelenleg fejlesztés alatt álló második funkció az egymásba ágyazott hierarchiák feliratainak használata (érdemes figyelnie, mert gyakran frissítünk).   

## <a name="how-inline-hierarchy-labels-work"></a>A beágyazott hierarchiák feliratainak működése
A beágyazott hierarchiák feliratai segítségével megtekintheti a hierarchiák feliratait, ha **Az összes kibontása** funkcióval kibontja a vizualizációkat. A hierarchiák feliratainak az egyik nagy előnye, hogy lehetőség van **rendezésre** a különböző hierarchiák feliratai szerint a hierarchikus adatok kibontása során.

### <a name="using-the-built-in-expand-all-feature-without-sorting-by-hierarchy-labels"></a>A beépített Összes kibontása funkció használata (hierarchiák feliratai szerinti rendezés nélkül)
Mielőtt megnézzük a beépített hierarchiák feliratainak a működését, tekintsük át **Az összes kibontása** funkció alapértelmezett viselkedését. Ez lehetővé teszi, hogy megértsük (és értékeljük), mennyire hasznosak lehetnek a beépített hierarchiák feliratai.

Az alábbi képen egy éves értékesítési adatokat tartalmazó sávdiagram látható. Ha jobb gombbal rákattint, kiválaszthatja **Az összes kibontása** lehetőséget.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_4.png)

**Az összes kibontása** lehetőség kiválasztása után a vizualizáció kibontja a dátum hierarchiát *Évtől* kezdve *Negyedévig*, ahogy az alábbi képen látható.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_5.png)

Megfigyelheti, hogy az *Év* és *Negyedév* feliratok egymásba ágyazva jelennek meg. Ez a feliratozási séma folytatódik, ha **Az összes kibontása** lehetőséget használja a hierarchia aljáig.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_6.png)

Így viselkedik a beépített *Dátum* hierarchia, ami olyan mezőkhöz társul, amelyekben *dátum/idő* adattípus van. Lépjünk a következő szakaszra, és nézzük meg, hogy miben más az új beépített hierarchiák felirata funkció.

### <a name="using-inline-hierarchy-labels"></a>A beágyazott hierarchiák feliratainak használata
Az alábbiakban bemutatunk egy másik diagramot olyan adatokkal, amelyek közt informális hierarchiáik vannak. Az alábbi vizualizációban van egy oszlopdiagram a **SalesAmount** (Értékesítés összege) értékét mutatja, és a *Color* (Szín) értéket használjuk tengelyként. Ezekben az adatokban a *Color* (Szín) és a *Class* (Osztály) informális hierarchiát alkotnak. Innen újra kiválaszthatja *Az összes kibontása* lehetőséget, és részletes elemzést indíthat a hierarchiában.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_7.png)

Ha kiválasztja **Az összes kibontása** lehetőséget, megjelenik a következő szint a hierarchiák feliratainak beépített megjelenítésével. Alapértelmezés szerint a beépített hierarchiák a mértékérték alapján vannak rendezve, ebben az esetben a **SalesAmount** alapján. Ha a beépített hierarchiák feliratai be vannak kapcsolva, rendezheti ezeket az adatokat hierarchia szerint is a felső sarokban található három pont (**...**) kiválasztásával, majd a **Rendezés szempontja > Color Class** lehetőség kiválasztásával, az alábbi képen látható módon.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_8.png)

A **Color Class** kiválasztása után az adatok rendezése a kiválasztott informális hierarchia szerint történik az alábbi képen látható módon.

![](media/desktop-inline-hierarchy-labels/inlinehierarchy_9.png)

> [!NOTE]
> A beépített hierarchiák feliratai funkció még nem teszi lehetővé a beépített időhierarchia érték szerinti rendezését. Csak hierarchia szerint rendezhető.
> 
> 

## <a name="troubleshooting"></a>Hibaelhárítás
Lehetséges, hogy a vizualizációk kibontott beágyazott hierarchiaszint szerinti állapotban maradnak. Egyes esetekben előfordulhat, hogy néhány vizualizáció abban a módban marad, amelybe kibontotta azokat, és ilyenkor a felhatolás nem működik. Ez a következő lépések végrehajtása esetén történhet (a hiba javítása a következő lépések *alatt* található):

Lépések, amelyektől kibontott állapotban maradhatnak a vizualizációk:

1. Engedélyezi a **beágyazott hierarchiák feliratai** funkciót
2. Létrehoz néhány hierarchiákkal rendelkező vizualizációt
3. Ezután **Az összes kibontása** funkciót használja, és menti a fájlt
4. Ezt követően *letiltja* a **beágyazott hierarchiák feliratai** funkciót, és újraindítja a Power BI Desktopot
5. Ezután megnyitja újra a fájlt

Ha végrehajtja ezeket a lépéseket, és a vizualizációk kibontott nézetben ragadnak, a következőket teheti a hiba elhárításához:

1. Engedélyezze újra a **beágyazott hierarchiák feliratai** funkciót, majd indítsa újra a Power BI Desktopot
2. Nyissa meg újra a fájlt, és hatoljon vissza az érintett vizualizáció(k) tetejére
3. Mentse a fájlt
4. Tiltsa le a **beágyazott hierarchiák feliratai** funkciót, majd indítsa újra a Power BI Desktopot
5. Nyissa meg újra a fájlt

Másik lehetőségként egyszerűen törölheti és újra létrehozhatja a vizualizációt.

