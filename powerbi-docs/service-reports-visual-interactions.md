---
title: "Vizualizációk jelentésen belüli működésének módosítása"
description: "Dokumentáció a vizualizációk a Microsoft Power BI-jelentésekben előforduló interakcióiról."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: N_xYsCbyHPw
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/25/2017
ms.author: mihart
ms.openlocfilehash: 126bd40e98a88138a2732155f9792d65666e52c7
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="visualization-interactions-in-a-power-bi-report"></a>Vizualizációk interakciói a Power BI-jelentésekben
Alapértelmezés szerint egy jelentésoldal vizualizációi az oldal további vizualizációinak keresztszűréséhez és keresztkijelöléséhez használhatók.
Például egy állam kijelölése egy térkép vizualizációján kiemeli az oszlopdiagramot, és úgy szűri a vonaldiagramot, hogy az csak az adott államra vonatkozó adatokat jelenítse meg.
Lásd: [Szűrés és kiemelés](power-bi-reports-filters-and-highlighting.md).

Az alapértelmezett viselkedés módosításához használja a **Vizualizációs interakciók** vezérlőt. A vizualizációk interakciói csak [Szerkesztő nézetben](service-interact-with-a-report-in-editing-view.md) érhetők el. Ha egy jelentés meg van osztva Önnel, a vizualizációk interakcióihoz nem férhet hozzá.

> [!NOTE]
> A *keresztszűrés* és *keresztkijelölés* kifejezésekkel az itt ismertetett viselkedéseket a **Szűrők** ablaktábla szűrés és kiemelés funkciójától különböztetjük meg.  
> 
> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/N_xYsCbyHPw?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

1. Aktiváljon egy vizualizációt annak kijelölésével.  
2. Kapcsolja be a **vizualizációk interakcióit** a felső menüsávban. Ekkor szűrő- és kiemelőikonok jelennek meg a jelentés lapján, ha a kurzort a többi vizualizáció felé helyezi.
   
    ![](media/service-reports-visual-interactions/pbi-visual-interaction-icon.png)
3. Adja meg, hogy a kijelölt vizualizáció milyen hatással legyen a többire.  
   
   * Ha keresztszűrést szeretne megadni, kattintson a **szűrő** ikonra ![](media/service-reports-visual-interactions/pbi-filter-icon-outlined.png).
   * Ha keresztkiemelést szeretne megadni, kattintson a **kiemelés** ikonra ![](media/service-reports-visual-interactions/pbi-highlight-icon-outlined.png).
   * Ha nem szeretne hatást megadni, kattintson a **nincs hatás** ikonra ![](media/service-reports-visual-interactions/pbi-noimpact-icon-outlined.png).
4. Ha szeretné, ezt megismételheti a jelentés oldalának minden vizualizációjával.

### <a name="next-steps"></a>Következő lépések
[Jelentésszűrők használata](power-bi-how-to-report-filter.md)

[Szűrés és kiemelés a jelentésekben](power-bi-reports-filters-and-highlighting.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

