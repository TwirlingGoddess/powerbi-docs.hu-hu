---
title: Elemzések használata a Power BI Desktopban (Előzetes verzió)
description: Növekedések és csökkenések elemzése könnyedén a Power BI Desktopban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/02/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 2b5959049b65d32eebf7f484e8485ff59a10f459
ms.sourcegitcommit: 2a7bbb1fa24a49d2278a90cb0c4be543d7267bda
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/26/2018
ms.locfileid: "34286083"
---
# <a name="use-insights-in-power-bi-desktop-preview"></a>Elemzések használata a Power BI Desktopban (Előzetes verzió)
A **Power BI Desktop** alkalmazáson belül kérheti a diagramokon látható növekedések és csökkenések értelmezését, valamint az adatok gyors, automatikus, részletes elemzését is. Egyszerűen a jobb egérgombbal kattintson egy adatpontra, és válassza az **Elemzés > A csökkenés magyarázata**  lehetőséget (vagy a növekedés magyarázatát, ha az előző oszlop alacsonyabb volt). A rendszer ezt követően a magyarázatot egy könnyen használható ablakban jeleníti meg.

![](media/desktop-insights/insights_01.png)

Az elemzés egy kontextus alapú funkció, amely az előző adatpontokat, például oszlopokat veszi figyelembe.

> [!NOTE]
> Ez a funkció egyelőre előzetes verzióként érhető el, ezért változhat. A **Power BI Desktop** 2017 szeptemberi és az annál újabb verzióiban az elemzés funkció alapértelmezés szerint engedélyezve van és működik (nem kell bejelölnie az előnézeti jelölőnégyzetet az engedélyezéshez).
> 
> 

## <a name="using-insights"></a>Elemzések használata
Az elemzések használatához a jobb egérgombbal kattintson egy oszlopon vagy vonalon található adatpontra, és válassza az **Elemzés > A növekedés magyarázata** lehetőséget (vagy az *A csökkenés magyarázata* lehetőséget, mivel az elemzés az előző adatponthoz viszonyított változást veszi figyelembe).

![](media/desktop-insights/insights_02.png)

A **Power BI Desktop** ezt követően futtatja az adatokon a gépi tanulási algoritmusokat, majd feltölti a növekedést vagy csökkenést leginkább befolyásoló kategóriák leírását és vizualizációját egy ablakba. Ahogy az a következő képen látható, alapértelmezés szerint az elemzéseket *vízesés* vizualizáció formájában adja meg a rendszer.

![](media/desktop-insights/insights_03.png)

A vízesés vizualizáció alján található kis ikonokra kattintva kiválaszthatja, hogy az elemzés pontdiagram, halmozott oszlopdiagram vagy szalagdiagram formájában jelenjen meg.

![](media/desktop-insights/insights_04.png)

A lap tetején található *felfelé mutató hüvelykujj* és *lefelé mutató hüvelykujj* ikonokat használva visszajelzést adhat a vizualizációról és a funkcióról.

Továbbá a vizualizáció tetején található **+** gomb segítségével hozzáadhatja jelentéséhez a kiválasztott vizualizáció ugyanúgy, mintha manuálisan hozta volna létre. Ezt követően tetszőlegesen formázhatja vagy módosíthatja a hozzáadott vizualizációt bármely más, a jelentésében szereplő vizualizációhoz hasonlóan. Csak akkor adhat hozzá egy kiválasztott elemzési vizualizációt, ha a **Power BI Desktopban** szerkeszti a jelentést.

Az elemzéseket akkor használhatja, ha a jelentés olvasási vagy szerkesztési módban van, így azt mind az adatok elemzésére, mind pedig a jelentéshez könnyen hozzáadható vizualizációk létrehozásához is használhatja.

## <a name="considerations-and-limitations"></a>Megfontolandó szempontok és korlátozások
Mivel az elemzés az előző adatponthoz képest bekövetkezett változást veszi alapul, a vizualizáció első adatpontjának kiválasztása esetén az elemzés nem érhető el. 

A következő lista az **elemzések** jelenleg nem támogatott forgatókönyveit tartalmazza:

* Legjobb N szűrők
* Belefoglalási/kizárási szűrők
* Mérték szűrők
* Nem additív mértékek és összesítések
* Érték megjelenítési módja
* Szűrt mértékek (az elemzésekben újabban ezt használjuk a pontdiagramokhoz)
* Az X tengelyen elhelyezkedő kategorikus oszlopok, hacsak nem egy skaláris oszlop szerinti rendezést ír elő. Hierarchia használata esetén a hierarchiában szereplő összes oszlopnak meg kell felelnie az adott feltételnek
* Nem numerikus mértékek

Továbbá az elemzések esetében jelenleg nem támogatottak a következő modelltípusok és adatforrások:

* DirectQuery
* Élő kapcsolat
* Helyszíni Reporting Services
* Beágyazás

## <a name="next-steps"></a>Következő lépések
Ha többet szeretne megtudni a **Power BI Desktopról**, illetve a szoftver használatának kezdeti lépéseiről, tekintse meg a következő cikkeket.

* [Első lépések a Power BI Desktopban](desktop-getting-started.md)
* [Lekérdezések áttekintése a Power BI Desktopban](desktop-query-overview.md)
* [Adatforrások a Power BI Desktopban](desktop-data-sources.md)
* [Csatlakozás adatokhoz a Power BI Desktopban](desktop-connect-to-data.md)
* [Adatok formázása és kombinálása a Power BI Desktoppal](desktop-shape-and-combine-data.md)
* [Gyakori lekérdezési feladatok a Power BI Desktopban](desktop-common-query-tasks.md)   

