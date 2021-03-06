---
title: Vizualizáció-, oldal-, részletezési vagy jelentésszűrő hozzáadása jelentéshez
description: Oldalszűrő, vizualizációszűrő vagy jelentésszűrő hozzáadása egy jelentéshez a Power BI-ban
author: maggiesMSFT
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 05/26/2018
ms.author: maggies
LocalizationGroup: Reports
ms.openlocfilehash: 3758415dc41a5f94419193240d4ce71aa4aca1d8
ms.sourcegitcommit: fb1885da7cf11367660edbf7b7346dc039ee9b5d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/26/2018
ms.locfileid: "47187214"
---
# <a name="add-a-filter-to-a-power-bi-service-report-in-editing-view"></a>Szűrő hozzáadása a Power BI szolgáltatás jelentéseihez (Szerkesztési nézetben)
> [!TIP]
> Javasoljuk, hogy először olvassa el a [Power BI- jelentések szűrőivel és kiemeléseivel](power-bi-reports-filters-and-highlighting.md) foglalkozó szakaszt.

A cikkben található példák a Power BI szolgáltatást szemléltetik. Az elvégzendő lépések azonban csaknem teljesen azonosak a Power BI Desktop alkalmazásban is.
> 
> 

## <a name="what-is-the-difference-between-report-filters-in-editing-view-versus-reading-view"></a>Mi a különbség a Szerkesztési nézet és az Olvasás nézet jelentésszűrői között?
A jelentések két módban használhatók: [Olvasás nézetben](consumer/end-user-reading-view.md) és [Szerkesztési nézetben](service-interact-with-a-report-in-editing-view.md).  A szűrési képességek attól függnek, hogy milyen módban van éppen.

* Szerkesztési nézetben hozzáadhat jelentés-, oldal- és vizualizációszűrőket. Ha menti a jelentést, a rendszer a szűrőket is menti. A jelentést Olvasó nézetben megtekintő felhasználók használhatják az Ön által hozzáadott szűrőket.
* Olvasó nézetben használható a jelentésben már szereplő összes jelentés-, részletezés-, oldal- és vizualizációszűrő, de nem lehet új szűrőket hozzáadni. Ugyanakkor a Szűrök panelen végzett módosításokat menti a rendszer a jelentéssel együtt, még akkor is, ha mobilalkalmazásban tekinti meg a jelentést, vagy ha kilép a jelentésből, és később visszatér arra.  

> [!NOTE]
> Ez a cikk azt ismerteti, hogyan hozhatók létre szűrők egy jelentés **Szerkesztési nézetében**.  Az Olvasó nézet szűrőire vonatkozó további információkért tekintse át [a jelentés szűrőinek Olvasó nézetben történő használatával foglalkozó témakört](consumer/end-user-reading-view.md).


## <a name="filters-available-in-the-power-bi-filters-pane"></a>A Power BI *Szűrők* panelén elérhető szűrők
Akár a Desktop alkalmazást, akár a Power BI szolgáltatást használja, a Szűrők panel megjelenik a jelentésvászon jobb oldalán. Ha a Szűrők panel nem látható, válassza a jobb felső sarokban lévő „>” ikont a kibontásához.

A szűrőknek négy különböző típusa létezik.

- **Oldalszűrő:** A jelentésoldal összes vizualizációjára vonatkozik.     
- **Vizualizációszűrő:** A jelentésoldal egy adott vizualizációjára vonatkozik.    
- **Részletezési szűrő:** A jelentés egyetlen entitására vonatkozik.    
- **Jelentésszűrő:** A jelentés összes oldalára vonatkozik.    

    ![a szűrők ablaktáblája Olvasó nézetben](media/power-bi-report-add-filter/power-bi-add-filter-reading-view.png)

Mivel a szűrőket *megőrzi* a rendszer, amikor kilép a jelentésből, a Power BI eltárolja a szűrők, a szeletelők és az adatnézet egyéb módosításait. Így amikor visszatér a jelentéshez, ott folytathatja, ahol abbahagyta. Ha nem szeretné, hogy a rendszer megőrizze a szűrők módosításait, válassza a **Visszaállítás alapértelmezettre** lehetőséget a felső menüsoron.

![a megőrzött szűrők gombja](media/power-bi-report-add-filter/power-bi-reset-to-default.png)

## <a name="add-a-filter-to-a-specific-visualization-aka-visual-filter"></a>Szűrő hozzáadása egy adott vizualizációhoz (vizualizációszűrő)
Ennek 2 módja van: 

* Szűrhet egy, a vizualizáció által már használt mezőt
* Azonosíthat egy mezőt, amelyet a vizualizáció még nem használ, és hozzáadhatja ezt a mezőt közvetlenül a **Vizualizációszint szűrői** gyűjtőhöz.

### <a name="by-filtering-the-fields-already-in-the-visualization"></a>A vizualizációban már szereplő mezők szűrése
1. Nyissa meg a [jelentést Szerkesztési nézetben](consumer/end-user-reading-view.md).
   
   ![](media/power-bi-report-add-filter/power-bi-edit-view.png)
2. Nyissa meg a Megjelenítések, a Szűrők és a Mezők panelt (ha még nincsenek megnyitva).
   
   ![](media/power-bi-report-add-filter/power-bi-display-panes.png)
3. Tegyen aktívvá egy vizualizációt kijelöléssel. A vizualizáció által használt összes mező szerepel a **Mezők** és a **Szűrők** panelen is, a **Vizualizációszint szűrői** fejléc alatt.
   
   ![](media/power-bi-report-add-filter/power-bi-default-visual-filter.png)
4. Ezen a ponton felveszünk egy szűrőt egy, a vizualizáció által már használt mezőhöz. 
   
   * Görgessen le a **Vizualizációszint szűrői** területre, és a nyilat kiválasztva bontsa ki a szűrni kívánt mezőt. Ebben a példában a **StoreNumberName** mezőt szűrjük.
     
      ![](media/power-bi-report-add-filter/power-bi-visual-level-filter.png) 
   * Állítson be **Alapszintű**, **Speciális** vagy **Felső N** szűrésvezérlőket (lásd [a jelentésszűrők használatát](consumer/end-user-report-filter.md) ismertető témakört). Ebben a példában Alapszintű szűrést választunk, és a következő számok jelölőnégyzetét jelöljük ki: 10, 11, 15 és 18.
     
      ![](media/power-bi-report-add-filter/power-bi-basic-filters.png) 
   * A vizualizáció módosul az új szűrőnek megfelelően. Ha menti a jelentést a szűrővel, a jelentés olvasói használhatják a szűrőt Olvasás nézetben: kiválaszthatnak vagy törölhetnek értékeket.
     
      ![](media/power-bi-report-add-filter/power-bi-filter-effect.png)
5. Most vegyünk fel egy teljesen új mezőt a vizualizációhoz vizualizáció szintű szűrőnek.
   
   * A Mezők panelen válassza ki az új vizualizáció szintű szűrőként felvenni kívánt mezőt, és húzza a **Vizualizációszint szűrői területre**.  Ebben a példában a **District Manager** (kerületi vezető) mezőt húzzuk a **Vizualizációszint szűrői** gyűjtőbe, és csak Andrew Mát választjuk ki. 
     
      ![](media/power-bi-report-add-filter/power-bi-andrew.png)
   * Vegye figyelembe, hogy a **District Manager** elemet a rendszer *nem* adta hozzá magához a vizualizációhoz. A vizualizációnak még mindig a **StoreNumberName** mező a tengelye, és a **This Year Sales** (Idei értékesítések) az értéke.  
     
      ![](media/power-bi-report-add-filter/power-bi-visualization.png)
   * A vizualizáció maga viszont úgy van most szűrve, hogy csak Andrew idei értékesítéseit jelenítse meg az adott üzletekhez.
     
     ![](media/power-bi-report-add-filter/power-bi-filtered-andrew.png)

## <a name="add-a-filter-to-an-entire-page-aka-page-view-filter"></a>Szűrő hozzáadása az egész oldalhoz (oldalnézetszűrő)
1. Nyissa meg a [jelentést Szerkesztési nézetben](consumer/end-user-reading-view.md).
2. Nyissa meg a Megjelenítések, a Szűrők és a Mezők panelt (ha még nincsenek megnyitva).
3. A Mezők panelen válassza az új oldalszintű szűrőként hozzáadni kívánt mezőt, és húzza a **Lapszintű szűrők** területre.  
4. Válassza ki a szűrni kívánt értékeket, és állítson be **Alapszintű** vagy **Speciális** szűrésvezérlőket (lásd [a jelentésszűrők használatát](consumer/end-user-report-filter.md) ismertető témakört).
   
   A rendszer a szűrő hatálya alá eső oldalon szereplő összes vizualizációt újrarajzolja, hogy megfeleljenek a módosításnak. 
   
   ![](media/power-bi-report-add-filter/filterpage.gif)

Ha menti a jelentést a szűrővel, a jelentés olvasói használhatják a szűrőt Olvasás nézetben: kiválaszthatnak vagy törölhetnek értékeket.

## <a name="add-a-drillthrough-filter"></a>Részletezési szűrő hozzáadása
A Power BI szolgáltatás és a Power BI Desktop részletezési funkciójával olyan *cél* jelentésoldalt hozhat létre, amely egy adott entitásra összpontosít – például egy szállítóra, ügyfélre vagy gyártóra. A felhasználók a jelentés többi oldalán a jobb gombbal az entitáshoz tartozó adatpontra kattintva eljuthatnak az összpontosított oldalra.

### <a name="create-a-drillthrough-filter"></a>Részletezési szűrő létrehozása
Annak érdekében, hogy követni tudja a lépéseket, nyissa meg az ügyfél-jövedelmezőségi mintát Szerkesztési nézetben. Tegyük fel, hogy egy olyan oldalt szeretne, amely a vezetői üzleti területekre összpontosít.   

1. Adjon a jelentéshez egy új, **Csapatvezető** nevű oldalt. Ez lesz a részletezés *céloldala*.
2. Adjon hozzá vizualizációkat, amelyek nyomon követik a csapatvezetők üzleti területeinek fő mérőszámait.    
3. Vegye fel a Részletezési szűrők szakaszba a **Vezető > Vezető neve** elemet.    
   
    ![](media/power-bi-report-add-filter/power-bi-drillthrough-filter.png)
   
    Észreveheti, hogy a Power BI hozzáad egy vissza nyilat a jelentésoldalhoz.  A vissza nyíl kiválasztásával a felhasználó visszatér a *kiindulási* jelentésoldalra, ahol a részletezés megjelenítése mellett döntött. A vissza nyíl csak Olvasás nézetben működik.
   
     ![](media/power-bi-report-add-filter/power-bi-back-arrow.png)

### <a name="use-the-drillthrough-filter"></a>A részletezési szűrő használata
Lássuk, hogy működik a részletezési szűrő.

1. Kezdjen a **Team Scorecard** (Csapat mutatószáma) jelentésoldalon.    
2. Tegyük fel, hogy Ön Andrew Ma, és úgy szeretné megtekinteni a Csapatvezető jelentésoldalt, hogy az csak a saját adatait mutassa.  A diagram bal felső területén kattintson a jobb gombbal egy zöld adatpontra a Részletezés menüelem megnyitásához.
   
    ![](media/power-bi-report-add-filter/power-bi-drillthrough.png)
3. Válassza a **Részletezés > Csapatvezető** lehetőséget, hogy a **Csapatvezető** jelentésoldalra lépjen. A rendszer szűri az oldalt, hogy megjelenítse azon adatpont információit, amelyre a jobb gombbal kattintott, ami ebben az esetben az Andrew Ma. Csak a Részletezési szűrők szakaszban lévő mező kerül át a részletező jelentésoldalra.  
   
    ![](media/power-bi-report-add-filter/power-bi-drillthrough-executive.png)

## <a name="add-a-filter-to-an-entire-report-aka-report-filter"></a>Szűrő hozzáadása egy teljes jelentéshez (jelentésszűrő)
1. Nyissa meg a [jelentést Szerkesztési nézetben](consumer/end-user-reading-view.md).
2. Nyissa meg a Megjelenítések, a Szűrők és a Mezők panelt (ha még nincsenek megnyitva).
3. A Mezők panelen válassza ki az új jelentésszintű szűrőként felvenni kívánt mezőt, és húzza a **Jelentési szint szűrői** területre.  
4. Válassza ki a szűrni kívánt értékeket (lásd [a jelentésszűrők használatát](consumer/end-user-report-filter.md) ismertető témakört).

    A vizualizációk a jelentés összes oldalán módosulnak az új szűrőnek megfelelően, az aktív oldalt is beleértve. Ha menti a jelentést a szűrővel, a jelentés olvasói használhatják a szűrőt Olvasás nézetben: kiválaszthatnak vagy törölhetnek értékeket.

1. A vissza nyilat kiválasztva térhet vissza az előző jelentésoldalra.

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás

- Bizonyos helyzetekben a vizualizációszintű és az oldalszintű szűrő különböző eredményt adhat.  Például amikor vizualizációszintű szűrőt ad meg, a Power BI az összesített eredményeket szűri.  Az alapértelmezett összesítés a Sum, de [az összesítés típusa módosítható](service-aggregates.md).  

    Amikor ezután oldalszintű szűrőt ad meg, a Power BI összesítés nélkül végzi el a szűrést.  Ennek az az oka, hogy egy oldalon több, különböző típusú összesítést használó vizualizáció is lehet.  Így a rendszer minden egyes adatsorra külön alkalmazza a szűrőt.

- Ha nem látja a Mezők panelt, győződjön meg arról, hogy a jelentés [Szerkesztési nézetében](service-interact-with-a-report-in-editing-view.md) van.    
- Ha nagy mennyiségű módosítást végzett a szűrőkön, és szeretne visszatérni a jelentés készítőjének alapértelmezett beállításaihoz, válassza a **Visszaállítás alapértelmezettre** lehetőséget a felső menüsoron.

## <a name="next-steps"></a>Következő lépések
 [A jelentésszűrők használata](consumer/end-user-report-filter.md)

  [Szűrők és kiemelések a jelentésekben](power-bi-reports-filters-and-highlighting.md)

[Szűrők és kiemelések használata a jelentések Olvasás nézetében](consumer/end-user-reading-view.md)

[A jelentésvizualizációk keresztszűrési és keresztkiemelési viselkedésének módosítása](consumer/end-user-interactions.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

