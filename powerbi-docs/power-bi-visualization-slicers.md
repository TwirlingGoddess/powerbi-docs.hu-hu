---
title: "Szeletelő a Power BI-ban (Útmutató)"
description: "Oktatóanyag: szeletelő a Power BI-ban"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: zIZPA0UrJyA
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 03/05/2018
ms.author: v-thepet
LocalizationGroup: Visualizations
ms.openlocfilehash: cfa4c0f17c67a036b7d01744da1b5247345c493a
ms.sourcegitcommit: 4217430c3419046c3a90819c34f133ec7905b6e7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/12/2018
---
# <a name="slicers-in-power-bi-tutorial"></a>Szeletelő a Power BI-ban (Útmutató)
Egy értékesítési igazgató meg szeretné ismerni a teljes részlegre és az egyes körzeti képviselőkre vonatkozó mérőszámokat. Ehhez létrehozhat egy külön jelentést minden képviselőnek, vagy használhat szeletelőt. A szeletelők a jelentés más vizualizációiban szereplő részére szűkítik az adathalmazt. A szeletelő egy alternatív módot kínál a szűrésre.

Ez az útmutató az ingyenes [Kiskereskedelmi elemzési minta](sample-retail-analysis.md) használatával mutatja be a szeletelők létrehozásának és formázásának, valamint jelentés szűrésére való használatának lépéseit. Jó szórakozást a szeletelők formázásának és használatának felfedezéséhez! 

![slicer](media/power-bi-visualization-slicers/slicer2.gif)

## <a name="when-to-use-a-slicer"></a>Mikor érdemes szeletelőt használni?
A szeletelő kitűnően alkalmas a következő célokra:

* Gyakran használt vagy fontos szűrők megjelenítése a jelentésvásznon a könnyebb elérhetőség érdekében.
* Az aktuális szűrt állapot egyszerűbb megjelenítése legördülő lista használata nélkül. 
* Az adattáblák szükségtelen és rejtett oszlopai alapján történő szűrés.
* Jobban szűrt jelentések létrehozása azáltal, hogy a szeletelőket a lényeges vizualizációk mellett helyezi el.

A Power BI-szeletelőkre a következő korlátozások érvényesek:

- A szeletelő nem támogatja a beviteli mezőket.
- A szeletelő nem rögzíthető irányítópulthoz.
- A szeletelők nem támogatják a részletezést.
- A szeletelő nem támogatja a vizualizációszintű szűrőket.

## <a name="create-a-slicer"></a>Szeletelő létrehozása

Ez az útmutató egy listaszeletelő használatát mutatja be. A numerikus és dátum/idő típusú adatokhoz tartományszeletelők rendelhetők. A tartomány-szeletelők létrehozásáról és használatáról [A numerikustartomány-szeletelő használata a Power BI Desktopban](desktop-slicer-numeric-range.md) című cikkből vagy a következő videóból tájékozódhat bővebben.
<iframe width="560" height="315" src="https://www.youtube.com/embed/zIZPA0UrJyA" frameborder="0" allowfullscreen></iframe>

1. A Power BI Desktopban vagy a Power BI szolgáltatásban nyissa meg a [Kiskereskedelmi elemzési mintát](sample-retail-analysis.md) [Szerkesztési nézetben](service-interact-with-a-report-in-editing-view.md), és [adjon hozzá egy új jelentésoldalt](power-bi-report-add-page.md).
2. A Mezők panelen a District (Körzet) szakaszban található **District Manager** (Körzeti képviselő) elem kijelölésével hozzon létre új vizualizációt.
    
    ![új diagram](media/power-bi-visualization-slicers/1-new-vis.png)
    
3. Alakítsa át a vizualizációt szeletelővé. A Vizualizációk ablaktáblán kattintson a **Szeletelő** ikonra ![szeletelő ikon](media/power-bi-visualization-slicers/slicer-icon.png). 
    
    ![szeletelővé alakítás](media/power-bi-visualization-slicers/2-slicer.png)

A Szeletelő ikonnal új szeletelőt is létrehozhat, amelyet úgy tölthet fel adatokkal, hogy kiválaszt hozzá vagy ráhúz egy adatmezőt.

>[!TIP]
>A listaszeletelők elemei az adatok értékei szerint rendezhetők. A szeletelőelemek fordított ábécésorrendben való rendezéséhez kattintson a három pontra (…) a szeletelő jobb felső sarkában, majd válassza a **Rendezés szempontja: DIstrict Manager** lehetőséget. Az alapértelmezett beállítás a növekvő ábécésorrend, de itt váltani lehet a növekvő és a csökkenő sorrend között. 

## <a name="format-the-slicer"></a>A szeletelő formázása
Végezze el a District Manager (Körzeti képviselő) szeletelő vizuális formázását.
1. Jelölje ki a szeletelőt, és a Vizualizációk ablaktáblán válassza a Formázás ikont ![](media/power-bi-visualization-slicers/power-bi-paintroller.png) a formázási beállítások megjelenítéséhez. 
    
    ![formázás](media/power-bi-visualization-slicers/3-format.png)
    
2. A beállítások megjelenítéséhez és szerkesztéséhez kattintson a kategóriák melletti legördülőmenü-nyilakra. 

### <a name="general-options"></a>Általános beállítások
1. A **Körvonal színe** beállításnál adja meg a piros színt, majd módosítsa a **Körvonal vastagsága** értéket 2-re. Ez adja meg a fejléc és az elemek körüli körvonalak és az aláhúzások színét és vastagságát, ha azok engedélyezve vannak. 
2. A Tájolás alapbeállítása a Függőleges. A listaszeletelő ekkor függőleges elrendezésű, és a jelölőnégyzetek az elemek előtt vannak elhelyezve. Ha a **Vízszintes** lehetőséget választja, a szeletelő elemei vízszintesen lesznek elrendezve. Vízszintes tájolással a szövegek, gombok és csempék sokféle módon elrendezhetők a szeletelő méretétől, alakjától és az elemek formázásától függően. 
    
    ![vízszintes](media/power-bi-visualization-slicers/4-horizontal.png)
    
3. Kapcsolja be a **Rugalmas** elrendezést, amely a vízszintesen elrendezett szeletelőelemek méretét és elhelyezkedését a szeletelő méretéhez és alakjához igazítja. Egészen kis méretben a szeletelő szűrőikonná alakul át. 
    
    ![rugalmas](media/power-bi-visualization-slicers/5-responsive.png)
    
    >[!NOTE]
    >A rugalmas elrendezéssel járó módosítások felülírhatják a megadott fejléc- és elemformázási beállításokat. 
    
4. A szeletelő helyzete és mérete numerikus pontossággal is megadható az **X pozíció**, **Y pozíció**, **Szélesség** és **Magasság** mezőben, de a szeletelő közvetlenül a vásznon is áthelyezhető és méretezhető. Így sokféle méret és megjelenés, például egy vízszintes gombsor is előállítható. 

    ![vízszintes gombsor](media/power-bi-visualization-slicers/6-buttons.png)

A vízszintes tájolásról és a rugalmas formázásról az [Átméretezhető rugalmas szeletelő létrehozása a Power BI-ban](power-bi-slicer-filter-responsive.md) című cikk tartalmaz bővebb információt.

### <a name="selection-controls-options"></a>Kijelölési vezérlők beállításai
1. Az összes kijelölése lehetőség megjelenítése alapértelmezés szerint ki van kapcsolva. Kapcsolja **Be**, hogy a szeletelőn megjelenjen az összes elem kijelölésére és az összes kijelölés megszüntetésére alkalmas vezérlőelem. Amikor minden elem ki van jelölve, a kijelölések kattintással egyenként megszüntethetők, így ez nemleges feltételű szűrőként használható. 
    
    ![az összes kijelölése](media/power-bi-visualization-slicers/7-select-all.png)
    
2. Az Egyetlen elem kijelölése lehetőség alapértelmezés szerint be van kapcsolva. Az elemek kattintással egyenként kijelölhetők, a Ctrl billentyű lenyomva tartásával pedig több elem is kijelölhető. Ha az Egyetlen elem kijelölése lehetőséget **Ki** értékre állítja, akkor több elem is kijelölhető a Ctrl billentyű lenyomva tartása nélkül. Ismételt kattintással az elem kijelölése megszüntethető. 

### <a name="header-options"></a>Fejléc beállításai
A szeletelő felső részén az adatmező nevét tartalmazó fejléc alapértelmezés szerint be van kapcsolva. 
1. Formázza a fejléc szövegét. A **Betűszín** legyen piros, a **Betűméret** 14 pt, a **Betűcsalád** pedig Arial Black. 
2. A Körvonal részen válassza a **Csak alsó** lehetőséget. Ennek eredménye aláhúzás lesz az Általános beállítások között megadott vastagságú és színű vonallal. 

### <a name="item-options"></a>Elem beállításai
1. Formázza az elem szövegét és hátterét úgy, hogy a **Betűszín** fekete, a **Háttér** világospiros, a **Betűméret** 10 pt és a **Betűcsalád** Arial legyen. 
2. A Körvonal beállításnál válassza a **Keret** lehetőséget, hogy minden elem köré keretet rajzoljon az Általános beállítások között megadott vonalvastagsággal és színnel. 
    
    ![formázott](media/power-bi-visualization-slicers/8-formatted.png)
    
    >[!TIP]
    >- Vízszintes elrendezés esetén a nem kijelölt elemek a választott szöveg- és háttérszínnel jelennek meg, a kijelöltek pedig a rendszer alapértelmezése szerint általában fekete háttérrel és fehér szöveggel. 
    >- Függőleges elrendezésben az elemek mindig a beállított színekben látszanak, a kijelölt jelölőnégyzetek padig mindig feketék. 

### <a name="other-formatting-options"></a>Egyéb formázási lehetőségek
A további formázási lehetőségek alapértelmezés szerint ki vannak kapcsolva. Ha **Be** vannak kapcsolva: 
- **Cím:** Címsort vesz fel és formáz (a fejlécen kívül és attól függetlenül) a szeletelő felső részén. 
- **Háttér:** Háttérszínt ad meg a teljes szeletelőhöz, és beállítja annak átlátszóságát.
- **Zárolási helyzet:** Átméretezéskor megtartja a szeletelő képarányát.
- **Szegély:** 1 képpont vastagságú szegélyt rajzol a szeletelő köré, és beállítja annak színét. (Ez a szeletelőszegély az általános körvonal-beállításoktól független, azok nincsenek hatással rá.) 

## <a name="sync-and-use-the-slicer-on-other-pages"></a>Szinkronizálás és a szeletelő használata más oldalakon
A Power BI 2018. februári frissítésétől kezdve a szeletelők szinkronizálhatók és egy jelentés bármely – vagy akár az összes – oldalán felhasználhatók. 
1. Jelölje ki a District Manager (Körzeti képviselő) szeletelőt, és válassza Power BI Desktop Nézet menüjének **Szeletelők szinkronizálása** elemét, vagy kapcsolja be a **Szeletelők szinkronizálása** panelt a Power BI szolgáltatásban. Megjelenik a Szeletelők szinkronizálása panel. 
    
    ![szeletelők szinkronizálása](media/power-bi-visualization-slicers/9-sync-slicers.png)
    
2. Jelölje ki az első oszlop **Áttekintés** elemét és a többi oldalt, amellyel a szeletelőt szinkronizálni kívánja, majd kattintson a **Hozzáadás az összeshez** lehetőségre, hogy a szeletelő minden jelentésoldallal szinkronizálva legyen.  
3. A következő oszlopban jelölje ki az **Áttekintés** elemet és a többi oldalt, amelyen a szeletelőt meg kívánja jeleníteni. 
4. Váltson az **Áttekintés** oldalra, és figyelje meg a szeletelőt és annak az oldal más vizualizációira gyakorolt hatását. 
    - Válasszon ki más elemeket, és figyelje meg, hogyan változnak ez alapján az oldal más vizualizációi. Az elemek bármely oldalon történő kijelölése hatással van az összes szinkronizált oldalra.
    - Változtassa meg a szeletelő méretét, alakját, helyzetét és/vagy formázását az Áttekintés oldalon. A szeletelő formázása a többi szinkronizált oldalon nem változik. 

### <a name="control-which-page-visuals-are-affected-by-the-slicer"></a>Az oldal szeletelő által érintett vizualizációinak kijelölése
Alapértelmezés szerint egy jelentésoldalon elhelyezett szeletelő az oldal összes vizualizációját érinti. A **Vizualizációk interakciói** beállítással meggátolhatja, hogy a szeletelő az oldal bizonyos vizualizációira hatással legyen.

1. Az **Áttekintés** oldalon a szeletelő kijelölésével:
    - A Power BI Desktopban kattintson a Vizuális eszközök Formátum menüjére és válassza az **Interakciók szerkesztése** lehetőséget.
    - A Power BI szolgáltatásban gördítse le a **Vizualizációk interakciói** menüt a menüsávon, és kapcsolja be az **Interakciók szerkesztése** lehetőséget. 
    
    A szűrővezérlők az egyéb vizualizációk felett jelennek meg az oldalon. ![szűrővezérlők](media/power-bi-visualization-slicers/filter-controls.png)
    
2. Válassza az egyik vizualizáció feletti a **Nincs** ikont, hogy a szeletelő azt többé ne szűrje. Válassza a **Szűrés** ikont, hogy a szeletelő ismét szűrni kezdje a vizualizációt. 

Az interakciók szerkesztéséről a [Vizuális interakciók a Power BI-jelentésekben](service-reports-visual-interactions.md) című cikkben talál további információkat.

## <a name="next-steps"></a>Következő lépések
[Próbálja ki – ingyenes!](https://powerbi.com/)

Vannak a Power BI továbbfejlesztésére vonatkozó ötletei? [Ötlet beküldése](https://ideas.powerbi.com/forums/265200-power-bi-ideas).

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

[Vizualizáció hozzáadása jelentésekhez](power-bi-report-add-visualizations-i.md)

[Vizualizációk típusai a Power BI-ban](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

