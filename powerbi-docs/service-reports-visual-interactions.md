---
title: "Vizualizációk jelentésen belüli működésének módosítása"
description: "Dokumentáció a vizualizációk a Microsoft Power BI szolgáltatás jelentéseiben és a Power BI Desktop-jelentésekben előforduló interakcióiról."
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
ms.date: 01/10/2018
ms.author: mihart
ms.openlocfilehash: a7c4db0044772c28a3cb7a62649de3001945246c
ms.sourcegitcommit: afd6e9e6f8b192b26486cd04d2cbc9de046911b3
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/11/2018
---
# <a name="visualization-interactions-in-a-power-bi-report"></a>Vizualizációk interakciói a Power BI-jelentésekben
Ha rendelkezik szerkesztési engedéllyel a jelentéshez, akkor a **Vizualizáció-interakciókkal** határozhatja meg, hogy a jelentésoldal vizualizációi milyen hatással legyenek egymásra. 

Alapértelmezés szerint egy jelentésoldal vizualizációi az oldal további vizualizációinak keresztszűréséhez és keresztkijelöléséhez használhatók.
Például egy állam kijelölése egy térkép vizualizációján kiemeli az oszlopdiagramot, és úgy szűri a vonaldiagramot, hogy az csak az adott államra vonatkozó adatokat jelenítse meg.
Lásd: [Szűrés és kiemelés](power-bi-reports-filters-and-highlighting.md). Ha pedig olyan vizualizációkkal is rendelkezik, amelyek támogatják a [részletes vizsgálatot](power-bi-visualization-drill-down.md), akkor alapbeállítás szerint egy adott vizualizáció részletező elemzése nem lesz hatással a jelentésoldal többi vizualizációjára. Mindkét alapértelmezett viselkedés módosítható azonban, és az interakciók az egyes vizualizációkra vonatkozóan beállíthatóak.

Ez a cikk azt mutatja be, hogyan használhatók a **vizualizáció-interakciók** a Power BI szolgáltatásban [Szerkesztési módban](service-interact-with-a-report-in-editing-view.md), valamint a Power BI Desktopban. Ha egy jelentés meg van osztva Önnel, a vizualizációk interakcióinak beállítását nem módosíthatja.

> [!NOTE]
> A *keresztszűrés* és *keresztkijelölés* kifejezésekkel az itt ismertetett viselkedéseket a **Szűrők** ablaktábla szűrés és kiemelés funkciójától különböztetjük meg.  
> 
> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/N_xYsCbyHPw?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

1. Aktiváljon egy vizualizációt annak kijelölésével.  
2. Jelenítse meg a **Vizualizáció-interakciók** beállításait.
    - A Power BI szolgáltatásban válassza a jelentés menüsorából a legördülő listát.

       ![](media/service-reports-visual-interactions/power-bi-visual-interaction.png)

    - A Desktopban válassza a **Formázás > Interakciók** lehetőséget.

        ![](media/service-reports-visual-interactions/pbi-visual-interaction-desktop.png)

3. Ha be szeretné kapcsolni a vizualizáció-interakciók vezérlőit, válassza az **Interakciók szerkesztése** lehetőséget. A Power BI a jelentésoldal összes többi vizualizációjához keresztszűrési és keresztkiemelési ikonokat ad hozzá.
   
    ![](media/service-reports-visual-interactions/power-bi-icons-on.png)
3. Adja meg, hogy a kijelölt vizualizáció milyen hatással legyen a többire.  Ha szeretné, ezt megismételheti a jelentés oldalának minden vizualizációjával.
   
   * Ha keresztszűrést szeretne megadni, kattintson a **szűrő** ikonra ![](media/service-reports-visual-interactions/pbi-filter-icon-outlined.png).
   * Ha keresztkiemelést szeretne megadni, kattintson a **kiemelés** ikonra ![](media/service-reports-visual-interactions/pbi-highlight-icon-outlined.png).
   * Ha nem szeretne hatást megadni, kattintson a **nincs hatás** ikonra ![](media/service-reports-visual-interactions/pbi-noimpact-icon-outlined.png).

4. A részletező elemzés vezérlőinek bekapcsolásához válassza a **Más vizualizációk részletező szűrése** lehetőséget.  Ha most egy vizualizációt részletesen elemez, akkor a jelentésoldal többi vizualizációja is változik majd, és tükrözi az aktuális elemzési kiválasztást. 

   ![](media/service-reports-visual-interactions/drill2.gif)

### <a name="next-steps"></a>Következő lépések
[A jelentésszűrők használata](power-bi-how-to-report-filter.md)

[Szűrés és kiemelés a jelentésekben](power-bi-reports-filters-and-highlighting.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

