---
title: "Kombinált diagram a Power BI-ban (Oktatóanyag)"
description: "Ez a dokumentáció egy (videót is tartalmazó) oktatóanyag, amely bemutatja, miért érdemes és hogyan lehet kombinált diagramokat készíteni a Power BI-ban."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: lnv66cTZ5ho
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/27/2017
ms.author: mihart
ms.openlocfilehash: c00ba74501a411743036c4514750bccbbae3eb00
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="combo-chart-in-power--tutorial"></a>Kombinált diagram a Power BI-ban (Oktatóanyag)
A kombinált diagramok olyan vizualizációk a Power BI-ban, amelyek egy vonaldiagramot és egy oszlopdiagramot kombinálnak egyetlen elemmé. A két diagram kombinációjával gyorsabban hasonlíthat össze adatokat.

A kombinált diagramoknak egy vagy két Y tengelyük lehet.

## <a name="when-to-use-a-combo-chart"></a>Mikor érdemes kombinált diagramokat használni?
A kombinált diagramok használata nagyszerű választás, ha:

* van egy vonaldiagramja és egy oszlopdiagramja, amelyek ugyanazt az X tengelyt használják;
* több, különböző értéktartományú mértéket szeretne összehasonlítani;
* egyetlen vizualizáción szeretné bemutatni két mérték korrelációját;
* szeretné ellenőrizni, hogy egy mérték elér-e egy adott célt, amelyet egy másik mérték határoz meg;
* kevesebb helyet szeretne felhasználni a vásznon.

## <a name="create-a-basic-single-axis-combo-chart"></a>Egyszerű, egytengelyes kombinált diagram létrehozása
Nézze meg, hogyan hoz létre Will egy kombinált diagramot az Értékesítési és marketing mintát használva.

<iframe width="560" height="315" src="https://www.youtube.com/embed/lnv66cTZ5ho?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>


Egy kombinált diagram létrehozásához jelentkezzen be a Power BI-ba, válassza az **Adatok beolvasása \> Minták \> Kiskereskedelmi elemzési minta** lehetőséget. 

1. A „Retail Analysis Sample” nevű irányítópultján válassza a **Total Stores** (Összes üzlet) csempét a „Retail Analysis Sample” nevű jelentés megtekintéséhez.
2. Válassza a **Jelentés szerkesztése** lehetőséget, hogy megnyissa a jelentést Szerkesztő nézetben.
3. [Adjon hozzá egy új oldalt a jelentéshez](power-bi-report-add-page.md).
4. Hozzon létre egy oszlopdiagramot, amely az idei év értékesítéseit és bruttó árrését jeleníti meg havi bontásban.
   
    a.  A Mezők ablaktáblán válassza ki a **Sales** \> **This Year Sales** > **Érték** elemet.
   
    b.  Húzza a **Sales** \> **Gross Margin This Year** elemet az **Érték** gyűjtőbe.
   
    c.  Adja hozzá a **Time** \> **FiscalMonth** elemet a **Tengely** gyűjtőhöz. 
   
    ![](media/power-bi-visualization-combo-chart/combotutorial1new.png)
5. A vizualizáció jobb felső sarkában válassza a három pontot (...), és válassza ki a **Rendezés szempontja: FiscalMonth** lehetőséget.
6. Konvertálja az oszlopdiagramot kombinált diagrammá. Ha az oszlopdiagram van kiválasztva, a **Megjelenítések** ablaktáblán válassza a **Vonal- és fürtözött oszlopdiagram** lehetőséget.
   
    ![](media/power-bi-visualization-combo-chart/converttocombo_new2.png)
7. A **Mezők** ablaktábláról húzza a **Sales** \> **Last Year Sales** elemet a **Sorértékek** gyűjtőbe.
   
   ![](media/power-bi-visualization-combo-chart/linevaluebucket.png)
   
   A kombinált diagramnak ekkor ehhez hasonlóan kell kinéznie:
   
   ![](media/power-bi-visualization-combo-chart/combochartdone-new.png)

## <a name="create-a-combo-chart-with-two-axes"></a>Kéttengelyes kombinált diagram létrehozása
Ebben a feladatban a bruttó árrést és az értékesítéseket fogjuk összehasonlítani.

1. Hozzon létre egy új vonaldiagramot, amely a Gross Margin % last year (%-os bruttó árrés a tavalyi évben) értéket jeleníti meg havi bontásban.  A bruttó árrés januárban 35% volt, 45%-kal áprilisban volt a legmagasabb, visszaesett júliusban, majd ismét a csúcson volt augusztusban. Vajon hasonló mintát fogunk látunk a tavalyi év és az idei év értékesítéseiben?
   
   ![](media/power-bi-visualization-combo-chart/combo1_new.png)
2. Adja hozzá a **This Year Sales > Érték** és a **Last Year Sales** elemeket a vonaldiagramhoz. A  **Gross Margin % last year** (%-os bruttó árrés a tavalyi évben) skálája sokkal kisebb, mint a **Sales** (Értékesítések) skálája, így nehéz összehasonlítani őket.      
   
   ![](media/power-bi-visualization-combo-chart/flatline_new.png)
3. Hogy a vonaldiagram jobban átlátható és könnyebben értelmezhető legyen, konvertálja vonal- és halmozott oszlopdiagrammá.
   
   ![](media/power-bi-visualization-combo-chart/converttocombo_new.png)
4. Húzza a **Gross Margin% Last Year** elemet az **Oszlopértékekből** a **Sorértékekbe**. A Power BI ekkor létrehoz két tengelyt, így lehetővé teszi, hogy az adatkészletek skálázása eltérő legyen. A bal oldali tengely dollárokat jelöl, a jobb oldali pedig százalékos értéket.
   
   ![](media/power-bi-visualization-combo-chart/power-bi-combochart.png)    

## <a name="add-titles-to-the-axes"></a>Címek felvétele tengelyekhez
1. A Formátum ablaktábla megnyitásához válassza a festőhenger ikont ![](media/power-bi-visualization-combo-chart/power-bi-paintroller.png).
2. Az **Y tengely** kibontásához válassza a lefelé mutató nyilat.
3. Az **Y tengely (Oszlop)** tulajdonságai között állítsa a **Pozíciót** **Balra**, a **Címet** **Be**, a **Stílust** **Csak a cím megjelenítése**, a **Megjelenítési egységeket** pedig **Millió** értékre.
   
   ![](media/power-bi-visualization-combo-chart/power-bi-y-axis-column.png)
4. Győződjön meg arról, hogy az **Y tengely (Oszlop)** tulajdonságai között a **Másodlagos megtekintése** lehetőség **Be** értékre van állítva. Ez a kombinált diagramon belüli vonaldiagram formázási lehetőségeit jeleníti meg.
   
   ![](media/power-bi-visualization-combo-chart/power-bi-show-secondary.png)
5. Az **Y tengely (Sor)** részen hagyja a **Pozíció** tulajdonságot **Jobbra** értéken, kapcsolja **Be** a **Címet**, majd állítsa a **Stílust** **Csak a cím megjelenítése** értékre.
   
   A kombinált diagram ekkor már a címeikkel együtt jeleníti meg a két tengelyt.
   
   ![](media/power-bi-visualization-combo-chart/power-bi-titles-on.png)

Ezután az alábbiakat lehet érdemes elvégezni:

* [Kombinált diagram felvétele irányítópult-csempeként](service-dashboard-tiles.md).
* [Jelentés mentése](service-report-save.md).

## <a name="highlighting-and-cross-filtering"></a>Kiemelés és keresztszűrés
A Szűrők panel használatáról a [Szűrő hozzáadása jelentéshez](power-bi-report-add-filter.md) című cikk nyújt tájékoztatást.

Egy oszlop vagy egy sor kijelölése egy kombinált diagramon keresztszűrést végez a jelentés oldalon lévő többi vizualizáción és viszont.

## <a name="next-steps"></a>Következő lépések
[Vizualizáció hozzáadása jelentéshez](power-bi-report-add-visualizations-i.md)

[Vizualizációk a Power BI-jelentésekben](power-bi-report-visualizations.md)

[Vizualizációk típusai a Power BI-ban](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

[Próbálja ki ingyenesen](https://powerbi.com/)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

