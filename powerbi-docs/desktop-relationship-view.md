---
title: Kapcsolat nézet a Power BI Desktop szolgáltatásban
description: Kapcsolat nézet a Power BI Desktop szolgáltatásban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/02/2018
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: 58886dc1ae5490113d4d0ba9af00d16aefecbe71
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
---
# <a name="relationship-view-in-power-bi-desktop"></a>Kapcsolat nézet a Power BI Desktop szolgáltatásban
A **Kapcsolat nézet** megjeleníti a modellben szereplő összes táblát, oszlopot és kapcsolatot. Ez különösen hasznos lehet, ha a modellben összetett kapcsolatrendszer áll fenn sok tábla között.

Vizsgáljuk ezt meg.

![](media/desktop-relationship-view/relationshipview_fullscreen.png)

**A.**  Kapcsolat nézet ikonra – rákattintva Kapcsolat nézetben jelenítheti meg a modellt

**B.** Kapcsolat – ha az egérmutatót egy kapcsolat fölé viszi, megjelennek a használt oszlopok. Egy kapcsolatra duplán kattintva megnyithatja azt a **Kapcsolat szerkesztése** párbeszédpanelen. 

A fenti ábrán láthatja, hogy a *Stores* táblán van egy *StoreKey* oszlop, amely kapcsolódik a *Sales* táblához, amelyen szintén van egy *StoreKey* oszlop. Láthatjuk, hogy ez egy *Több az egyhez* (\*:1) kapcsolat, és a vonal közepén található ikon azt jelöli, hogy a Keresztszűrés iránya *Mindkettő*. Az ikonon látható nyíl mutatja a szűrőkörnyezet folyamatának irányát.

További információk a kapcsolatokról: [Kapcsolatok létrehozása és kezelése a Power BI Desktopban](desktop-create-and-manage-relationships.md).

