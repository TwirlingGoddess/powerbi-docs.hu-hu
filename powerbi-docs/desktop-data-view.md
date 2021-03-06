---
title: A Power BI Desktop adatnézete
description: A Power BI Desktop adatnézete
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 07/24/2018
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: fad7b8453b6d5d29a1f6c5d9d9ed49b0a8b8a66f
ms.sourcegitcommit: df7a58dae14ef311516c9b3098f87742786f0479
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/27/2018
ms.locfileid: "39280340"
---
# <a name="data-view-in-power-bi-desktop"></a>A Power BI Desktop adatnézete
Az **Adatnézet** segítségével megvizsgálhatja, felderítheti és megismerheti **Power BI Desktop**-modellben lévő adatokat. Az adatnézettel másképp tekintheti meg a táblákat, oszlopokat és adatokat, mint a **Lekérdezésszerkesztőben**. Az adatnézettel a modellbe való betöltésük *után* tekintheti meg az adatokat.

Az adatok modellezésekor előfordulhat, hogy csak meg szeretné tekinteni egy tábla vagy oszlop aktuális tartalmát anélkül, hogy ehhez egy vizualizációt vagy jelentésvásznat kellene létrehoznia akár a sorok szintjéig. Ez akkor igazán hasznos, amikor mértékeket vagy számított oszlopokat hoz létre, vagy amikor azonosítani szeretné az adatok típusát vagy kategóriáját.

Tekintsük meg részletesebben az **Adatnézet** néhány elemét.

![Adatnézet a Power BI Desktopban](media/desktop-data-view/dataview_fullscreen.png)

1. **Adatnézet ikonja** – Az ikon kiválasztásával Adatnézetbe léphet.

2. **Adatrács** – A kijelölt táblát és a benne lévő összes oszlopot és sort jeleníti meg. A **Jelentésnézet** elől elrejtett oszlopok itt szürkén jelennek meg. Jobb gombbal az egyes oszlopokra kattintva elérheti a beállításokat.

3. **Modellezés menüszalag** – Lehetővé teszi a kapcsolatok kezelését, számítások létrehozását és az oszlopok adattípusának, formátumának és adatkategóriájának szerkesztését.

4. **Képletsáv** – Itt adhatja meg a mértékek és a számított oszlopok DAX-képleteit.

5. **Keresés** – A modell tábláinak és oszlopainak keresésére szolgál.

6. **Mezők listája** – Az adatrácsban megtekintendő táblák vagy oszlopok kiválasztására szolgál.

## <a name="filtering-in-data-view"></a>Szűrés Adatnézetben

Az **Adatnézet** lehetővé teszi az adatok szűrését és rendezését is. Mindegyik oszlopnál feltüntetésre kerül a rendezés irányát szemléltető ikon (ha az oszlopra van rendezés alkalmazva).

![Rendezés és szűrés a Power BI Desktop Adatnézetében](media/desktop-data-view/dataview_sort-and-filter.png)

Szűrést alkalmazhat egyes értékekre, vagy az oszlopban található adatokat alapul véve használhatja a speciális szűrés funkciót is. 

> [!NOTE]
> Amikor egy, a felhasználói felülettől eltérő kulturális környezetben hoz létre egy Power BI-modellt (például amerikai angol nyelven, amelyet spanyolul tekint meg), a keresőmező kizárólag szövegmezők esetén jelenik meg az Adatnézet felhasználói felületén.
