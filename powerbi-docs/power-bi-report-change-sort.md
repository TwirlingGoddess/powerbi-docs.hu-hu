---
title: "A diagramok rendezésének módosítása egy Power BI-jelentésben"
description: "A diagramok rendezésének módosítása egy Power BI-jelentésben"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 01/20/2018
ms.author: mihart
ms.openlocfilehash: aeb22c23b0ef22afd44592c1ceb90537878042d9
ms.sourcegitcommit: 2ae323fbed440c75847dc55fb3e21e9c744cfba0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/23/2018
---
# <a name="change-how-a-chart-is-sorted-in-a-power-bi-report"></a>A diagramok rendezésének módosítása egy Power BI-jelentésben
A Power BI-jelentésekben a legtöbb vizualizációt rendezheti a kategóriáinak neve alapján betűrendben vagy az egyes kategóriák számértéke szerint. Ennek a diagramnak a rendezése például áruháznév alapján történt.

![](media/power-bi-report-change-sort/pbi_chartsortcategory.png)

A rendezés könnyedén módosítható egy kategóriáról (store name – üzlet neve) egy értékre (sales per square feet – értékesítés négyzetlábanként).

1. Válassz a ki a három pontot (...) ábrázoló gombot, és válassza a **Rendezés szempontja: Sales Per Sq Ft** lehetőséget.
2. Ha szükséges, a rendezés ikonra ![](media/power-bi-report-change-sort/sorticon.png) kattintva változtassa meg a rendezés módját **Csökkenőre**.

   ![](media/power-bi-report-change-sort/sortby.gif)

   **FIGYELEM**: Nem minden vizualizációt lehet rendezni.  A következő vizualizációkat például nem lehet rendezni: fatérkép, térkép, kartogram, pontdiagram, mérőműszer, kártya, többsoros kártya, vízesés.

<a name="other"></a>
## <a name="sorting-using-other-criteria"></a>Rendezés más feltételek alapján
Néha más mező vagy feltétel használatával szükséges rendezni a vizualizációt.  Rendezhet például hónapok (és nem betűrend) alapján, vagy a teljes számok és nem az egyes számjegyek alapján is (például, 0, 1, 9, 20, nem pedig 0, 1, 20, 9).  

Bizonyos esetekben lehetséges a vizualizációk kívánt feltétel, például hónap szerinti rendezése.  Ha ez nem lehetséges, szükséges lehet a jelentés alapjául szolgáló adatkészlet módosítása. Az alábbiakban néhány megoldást láthat:

* A Power BI Desktopban [használja az Adateszközök modellezése fület az adatok oszloponkénti rendezéséhez](desktop-sort-by-column.md).
* Ha Ön az adatkészlet tulajdonosa, az Excelben adjon hozzá egy, a hónap nevét és számát összefűző oszlopot. Ezt követően frissítse vagy importálja újra az adatkészlet ahhoz, hogy az új oszlop megjelenjen a Mezők területen.
* Győződjön meg róla, hogy az Excelben a számokat tartalmazó oszlopok cellaértéke „egész szám” vagy „tört” jelölésű, és nem „szöveg”.

## <a name="next-steps"></a>Következő lépések
További információk [a Power BI-jelentésekben lévő vizualizációkról](power-bi-report-visualizations.md).

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)
