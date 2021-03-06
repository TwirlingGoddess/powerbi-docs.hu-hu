---
title: A diagramok rendezésének módosítása egy Power BI-jelentésben
description: A diagramok rendezésének módosítása egy Power BI-jelentésben
author: mihart
manager: kvivek
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 05/20/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: dd8eeda3ba2bbc8da49a06199fa00dc3d731faaa
ms.sourcegitcommit: 70192daf070ede3382ac13f6001e0c8b5fb8d934
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/22/2018
ms.locfileid: "46565889"
---
# <a name="change-how-a-chart-is-sorted-in-a-power-bi-report"></a>A diagramok rendezésének módosítása egy Power BI-jelentésben
A Power BI-jelentésekben a legtöbb vizualizációt rendezheti a kategóriáinak neve alapján betűrendben vagy az egyes kategóriák számértéke szerint. Ennek a diagramnak a rendezése például áruháznév alapján történt.

![](media/end-user-change-sort/pbi_chartsortcategory.png)

A rendezés könnyedén módosítható egy kategóriáról (store name – üzlet neve) egy értékre (sales per square feet – értékesítés négyzetlábanként).

1. Válassz a ki a három pontot (...) ábrázoló gombot, és válassza a **Rendezés szempontja: Sales Per Sq Ft** lehetőséget.
2. Ha szükséges, a rendezés ikonra ![](media/end-user-change-sort/sorticon.png) kattintva változtassa meg a rendezés módját **Csökkenőre**.

   ![](media/end-user-change-sort/sortby.gif)

   **FIGYELEM**: Nem minden vizualizációt lehet rendezni.  A következő vizualizációkat például nem lehet rendezni: fatérkép, térkép, kartogram, pontdiagram, mérőműszer, kártya, többsoros kártya, vízesés.

## <a name="saving-changes-you-make-to-sort-order"></a>A rendezési sorrend módosításainak mentése
A Power BI-jelentések megőrzik a szűrőket, a szeletelőket, a rendezést és az adatnézetek egyéb módosításait. Így ha kilép egy jelentésből, majd később visszatér, a módosítások mentve lesznek.  Ha szeretné visszaállítani a módosításokat a jelentés készítőjének beállításaira, válassza a **Visszaállítás alapértelmezettre** lehetőséget a felső menüsorban. 

![megőrzött rendezés](./media/end-user-change-sort/power-bi-reset-to-default.png)

Ha azonban a **Visszaállítás alapértelmezettre** gomb szürke színnel jelenik meg, az azt jelenti, hogy a jelentés készítője letiltotta a módosítások mentésének (megőrzésének) képességét.

<a name="other"></a>
## <a name="sorting-using-other-criteria"></a>Rendezés más feltételek alapján
Néha más mező vagy feltétel használatával szükséges rendezni a vizualizációt.  Rendezhet például hónapok (és nem betűrend) alapján, vagy a teljes számok és nem az egyes számjegyek alapján is (például, 0, 1, 9, 20, nem pedig 0, 1, 20, 9).  

Bizonyos esetekben lehetséges a vizualizációk kívánt feltétel, például hónap szerinti rendezése.  Ha ez nem lehetséges, szükséges lehet a jelentés alapjául szolgáló adatkészlet módosítása. Az alábbiakban néhány megoldást láthat:

* A Power BI Desktopban [használja az Adateszközök modellezése fület az adatok oszloponkénti rendezéséhez](../desktop-sort-by-column.md).
* Ha Ön az adatkészlet tulajdonosa, az Excelben adjon hozzá egy, a hónap nevét és számát összefűző oszlopot. Ezt követően frissítse vagy importálja újra az adatkészlet ahhoz, hogy az új oszlop megjelenjen a Mezők területen.
* Győződjön meg róla, hogy az Excelben a számokat tartalmazó oszlopok cellaértéke „egész szám” vagy „tört” jelölésű, és nem „szöveg”.

## <a name="next-steps"></a>Következő lépések
További információk [a Power BI-jelentésekben lévő vizualizációkról](../visuals/power-bi-report-visualizations.md).

[Power BI – Alapfogalmak](end-user-basic-concepts.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)
