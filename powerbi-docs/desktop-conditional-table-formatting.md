---
title: Feltételes táblázatformázás a Power BI Desktopban
description: Egyéni formázás alkalmazása táblázatokra
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
ms.date: 05/08/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 1626c2af5906004b6b4f79f4830f003b96e241fc
ms.sourcegitcommit: 509be8852ba7595b9441c9479224f9dca298b26d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/09/2018
---
# <a name="conditional-formatting-in-tables"></a>Táblázatok feltételes formázása
A táblázatok feltételes formázásával a cellák értéke, illetve más értékek vagy mezők alapján határozhat meg egyéni cellaháttérszínt, és akár színátmeneteket is használhat. A feltételes formázás használatához a Power BI Desktop **Vizualizációk** ablaktáblájának **Mezők** szakaszában kattintson a lefele mutató nyílra a formázással ellátni kívánt **Értékek** területen (vagy kattintson a jobb gombbal a mezőre). A mezők feltételes formázása kizárólag az **Értékek** terület **Mezők** szakaszában kezelhető.

![táblázat feltételes formázása](media/desktop-conditional-table-formatting/table-formatting_1.png)

A megjelenő párbeszédpanelen beállíthatja a színt, valamint a *Minimum* és *Maximum* értékét. A **Széttartó** jelölőnégyzet bejelölése esetén megadhat egy választható *Középértéket* is.

![széttartó színek](media/desktop-conditional-table-formatting/table-formatting_2.png)

Színátmenetet akár az adatmodell egy mezője alapján is létrehozhat. Emellett megadhatja a kijelölt mezőre alkalmazandó összesítés típusát (a kijelölt mező **A szín alkalmazása erre** mezőben látható).

![színek alkalmazása mező alapján](media/desktop-conditional-table-formatting/table-formatting_2b.png)

A táblázatra a fenti lépéseket követve alkalmazott egyéni formázás felülír minden, a feltételesen formázott cellákra vonatkozó egyéni táblázatstílust.

![táblázatformázás](media/desktop-conditional-table-formatting/table-formatting_3.png)

Akár szöveges és dátummezőkre is alkalmazhat feltételes formázást, ha a formázás alapjául numerikus értéket választ. 

A vizualizációk feltételes formázásának törléséhez egyszerűen kattintson újra a mezőre a jobb gombbal, és válassza a **Feltételes formázás eltávolítása** lehetőséget.

![táblázatformázás eltávolítása](media/desktop-conditional-table-formatting/table-formatting_4.png)

