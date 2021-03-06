---
title: Feltételes táblázatformázás a Power BI Desktopban
description: Egyéni formázás alkalmazása táblázatokra
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 08/06/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 324a9b7f8a3718c6da0efb7533751d88dd717bcf
ms.sourcegitcommit: 67336b077668ab332e04fa670b0e9afd0a0c6489
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/12/2018
ms.locfileid: "44728088"
---
# <a name="conditional-formatting-in-tables"></a>Táblázatok feltételes formázása 
A táblázatok feltételes formázásával a cellák értéke, illetve más értékek vagy mezők alapján határozhat meg egyéni cellaszíneket, akár színátmenetek használatával is. A cellák értékei adatsávokkal is megjeleníthetők. 

A feltételes formázás használatához a Power BI Desktop **Vizualizációk** ablaktáblájának **Mezők** szakaszában kattintson a lefele mutató nyílra a formázással ellátni kívánt **Értékek** területen (vagy kattintson a jobb gombbal a mezőre). A mezők feltételes formázása kizárólag az **Értékek** terület **Mezők** szakaszában kezelhető.

![Feltételes formázás menü](media/desktop-conditional-table-formatting/table-formatting-0-popup-menu.png)

A következő bekezdések ezeket feltételes formázási lehetőségeket ismertetik. Egy táblázatoszlopban egyszerre több lehetőség is használható.

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

## <a name="color-formatting-by-field-value"></a>Formázás színekkel mezőérték szerint

Használható mérték vagy színt meghatározó oszlop is akár szöveges, akár hexadecimális értékkel, amellyel megadható egy táblázat vagy mátrixvizualizáció betűjének vagy hátterének színe. Adott mezőhöz egyéni logikát is létrehozhat, és ezzel alkalmazhatja a kívánt színt a betűre vagy a háttérre.

Az alábbi táblázatban például minden termékmodellhez egy adott szín van társítva. 

![ProductName mező színnevekkel](media/desktop-conditional-table-formatting/conditional-table-formatting_01.png)

Ha a cellát a mezőérték alapján szeretné formázni, válassza a **Feltételes formázás** párbeszédpanelt az adott vizualizáció *Szín* oszlopára való kattintással, majd a menüből válassza a **Háttérszín** lehetőséget. 

![Háttérszín kiválasztása a menüben](media/desktop-conditional-table-formatting/conditional-table-formatting_02.png)

A megjelenő párbeszédpanelen a **Formázás a következő szerint** legördülő területen válassza a **Mezőérték** lehetőséget, ahogy az alábbi képen látható.

![Formázás Mezőérték szerint](media/desktop-conditional-table-formatting/conditional-table-formatting_03.png)

Ez a folyamat megismételhető a betűszínre is, és a vizualizációban ennek eredményeképpen a **color** oszlop színét használó egyszínű kitöltés lesz alkalmazva, ahogyan az alábbi képen látható.

![Formázás Mezőérték szerint](media/desktop-conditional-table-formatting/conditional-table-formatting_04.png)

Létrehozható egy üzleti logikára épülő DAX-számítás is, amely a megadott feltételeknek megfelelően más-más hexadecimális kódokat ad vissza. Ez általában egyszerűbb eljárás, mint több szabályt létrehozni a feltételes formázás párbeszédpaneljében. Tekintse meg az alábbi képen a *ColorKPI* mezőt.

![DAX-számítások](media/desktop-conditional-table-formatting/conditional-table-formatting_05.png)

Ezt követően a **Háttérszínhez** a mezőértéket az alábbiak szerint állíthatja be.

![Mezőszín beállítása KPI alapján](media/desktop-conditional-table-formatting/conditional-table-formatting_06.png)

Az eredmények pedig az alábbi mátrix szerint jelennek majd meg.

![Mátrixvizualizáció KPI-értékeken alapuló színnel](media/desktop-conditional-table-formatting/conditional-table-formatting_07.png)

A fantáziáját és egy kis DAX-ot felhasználva számtalan egyéb változatot is létrehozhat.

## <a name="next-steps"></a>Következő lépések
További információkat a következő cikkekben talál:  

* [Tippek és trükkök a színformázáshoz a Power BI-ban](visuals/service-tips-and-tricks-for-color-formatting.md)  

