---
title: "Kapcsolat nézet a Power BI Desktop szolgáltatásban"
description: "Kapcsolat nézet a Power BI Desktop szolgáltatásban"
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
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: aeb58b33d2496da3a05a0faf3882b235b3a6e54f
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/06/2017
---
# <a name="relationship-view-in-power-bi-desktop"></a>Kapcsolat nézet a Power BI Desktop szolgáltatásban
A **Kapcsolat nézet** megjeleníti a modellben szereplő összes táblát, oszlopot és kapcsolatot. Ez különösen hasznos lehet, ha a modellben összetett kapcsolatrendszer áll fenn sok tábla között.

Vizsgáljuk ezt meg.

![](media/desktop-relationship-view/relationshipview_fullscreen.png)

**A.**  Kapcsolat nézet ikonra – rákattintva Kapcsolat nézetben jelenítheti meg a modellt

**B.** Kapcsolat – ha az egérmutatót egy kapcsolat fölé viszi, megjelennek a használt oszlopok. Egy kapcsolatra duplán kattintva megnyithatja azt a **Kapcsolat szerkesztése** párbeszédpanelen. 

A fenti ábrán láthatja, hogy a *Stores* táblán van egy *StoreKey* oszlop, amely kapcsolódik a *Sales* táblához, amelyen szintén van egy *StoreKey* oszlop. Láthatjuk, hogy ez egy *Több az egyhez* (\*:1) kapcsolat, és a vonal közepén található ikon azt jelöli, hogy a Keresztszűrés iránya *Mindkettő*. Az ikonon látható nyíl mutatja a szűrőkörnyezet folyamatának irányát.

További információk a kapcsolatokról: [Kapcsolatok létrehozása és kezelése a Power BI Desktopban](desktop-create-and-manage-relationships.md).
