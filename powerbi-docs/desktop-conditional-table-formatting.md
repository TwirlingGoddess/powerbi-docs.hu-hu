---
title: Feltételes táblázatformázás a Power BI Desktopban
description: Egyéni formázás alkalmazása táblázatokra
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/17/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 70aa61d6a02bea1b7058a68b20718008ace1b8c8
ms.sourcegitcommit: 2a7bbb1fa24a49d2278a90cb0c4be543d7267bda
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/26/2018
ms.locfileid: "34480888"
---
# <a name="conditional-formatting-in-tables"></a>Táblázatok feltételes formázása 
A táblázatok feltételes formázásával a cellák értéke, illetve más értékek vagy mezők alapján határozhat meg egyéni cellaszíneket, akár színátmenetek használatával is. A cellák értékei adatsávokkal is megjeleníthetők. 

A feltételes formázás használatához a Power BI Desktop **Vizualizációk** ablaktáblájának **Mezők** szakaszában kattintson a lefele mutató nyílra a formázással ellátni kívánt **Értékek** területen (vagy kattintson a jobb gombbal a mezőre). A mezők feltételes formázása kizárólag az **Értékek** terület **Mezők** szakaszában kezelhető.

![Feltételes formázás menü](media/desktop-conditional-table-formatting/table-formatting-0-popup-menu.png)

A következő bekezdések ezt a három feltételes formázási lehetőséget ismertetik. Egy táblázatoszlopban egyszerre több lehetőség is használható.

> [!NOTE]
> A táblázatra alkalmazott feltételes formázás felülír minden, a feltételesen formázott cellákra vonatkozó egyéni táblázatstílust.

A vizualizációk feltételes formázásának törléséhez egyszerűen kattintson újra a mezőre a jobb gombbal, válassza a **Feltételes formázás eltávolítása** lehetőséget, majd válassza ki az eltávolítandó formázástípust.

![Feltételes formázás eltávolítása menü](media/desktop-conditional-table-formatting/table-formatting-1-remove.png)

## <a name="background-color-scales"></a>Háttérszínek színskálái

A **Feltételes formázás**, majd a **Háttérszínek színskálái** lehetőséget választva a következő párbeszédpanel jelenik meg.

![Háttérszínek színskálái párbeszédpanel](media/desktop-conditional-table-formatting/table-formatting-1-default-dialog.png)

Kijelölhet egy mezőt az adatmodellből a színezés alapjául, ha megadja a mezőt az **A szín ezen az értéken alapul:** beállításnál. Ezen kívül a kiválasztott mező összesítésének típusát is megadhatja az **Összegzés** értékeként. A színezendő mező az **A szín alkalmazása erre:** alatt van megadva, hogy követni tudja a beállításokat. Szöveges és dátummezőkre is alkalmazhat feltételes formázást, ha a formázás alapjául numerikus értéket választ.

![Színezés mező alapján](media/desktop-conditional-table-formatting/table-formatting-1-apply-color-to.png)

Ha külön színeket szeretne használni adott értéktartományokhoz, jelölje be a **Szabályok szerinti színezés** lehetőséget. Színskála használatához hagyja jelöletlenül a **Szabályok szerinti színezés** jelölőnégyzetet. 

![Háttérszínek színskálái párbeszédpanel](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-dialog.png)

### <a name="color-by-rules"></a>Szabályok szerinti színezés

Ha a **Szabályok szerinti színezés** lehetőséget választja, megadhat egy vagy több értéktartományt, és mindegyikhez beállíthat egy színt.  Minden tartomány egy *Ha az érték* feltétellel kezdődik, és tartozik hozzá egy *és* kapcsolattal megadott feltétel és egy szín.

![Szabályok szerinti színezés értéktartománya](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-if-value.png)

A táblázat egyes tartományokba eső értékű cellái a megadott színnel jelennek meg. A következő ábrán három szabály látható.

![Példa szabályok szerinti színezésre](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules.png)

A példához tartozó táblázat ekkor a következőképpen jelenik meg:

![Példatáblázat szabályok szerinti színezéssel](media/desktop-conditional-table-formatting/table-formatting-1-color-by-rules-table.png)


### <a name="color-minimum-to-maximum"></a>Színezés a minimumtól a maximumig

Megadhatja a *Minimum* és a *Maximum* értékét és a hozzájuk tartozó színeket. A **Széttartó** jelölőnégyzet bejelölése esetén megadhat egy választható *Középértéket* is.

![Széttartás gomb](media/desktop-conditional-table-formatting/table-formatting-1-diverging.png)

A példához tartozó táblázat ekkor a következőképpen jelenik meg:

![Példatáblázat széttartó színezéssel](media/desktop-conditional-table-formatting/table-formatting-1-diverging-table.png)

## <a name="font-color-scales"></a>Betűszínek színskálái

A **Feltételes formázás**, majd a **Betűszínek színskálái** lehetőséget választva a következő párbeszédpanel jelenik meg. A párbeszédpanel hasonló a **Háttérszínek színskálái** panelhez, de nem a cellák háttérszínét, hanem a szöveg színét változtatja meg.

![Betűszínek színskálái párbeszédpanel](media/desktop-conditional-table-formatting/table-formatting-2-diverging.png)

A példához tartozó táblázat ekkor a következőképpen jelenik meg:

![Példatáblázat betűszínek színskáláival színezve](media/desktop-conditional-table-formatting/table-formatting-2-table.png)

## <a name="data-bars"></a>Adatsávok

A **Feltételes formázás**, majd az **Adatsávok** lehetőséget választva a következő párbeszédpanel jelenik meg. 

![Adatsávok párbeszédpanel](media/desktop-conditional-table-formatting/table-formatting-3-default.png)

A **Csak sávok megjelenítése** lehetőség alapértelmezés szerint nincs bejelölve, így a cellában az adatsáv és a tényleges érték is látható.

![Példatáblázat adatsávokkal és értékekkel](media/desktop-conditional-table-formatting/table-formatting-3-default-table.png)

Ha a **Csak sávok megjelenítése** lehetőség be van jelölve, akkor a cellában csak az adatsáv látható.

![Példatáblázat csak adatsávokkal](media/desktop-conditional-table-formatting/table-formatting-3-default-table-bars.png)
