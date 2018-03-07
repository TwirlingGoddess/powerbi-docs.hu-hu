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
ms.date: 05/30/2017
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 619f694e6e3ed167a14262994c1c978d5b4ea2e0
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="slicers-in-power-bi-service-tutorial"></a>Szeletelő a Power BI szolgáltatásban (Útmutató)
Az értékesítési igazgató meg szeretné ismerni a teljes részlegre és az egyes körzeti képviselőkre vonatkozó mérőszámokat. Ehhez létrehozhat egy külön jelentésoldalt minden képviselőnek, vagy használhat szeletelőt. A szeletelők az oldal más vizualizációiban szereplő részére szűkítik az adathalmazt.  A szeletelő egy alternatív módot kínál a szűrésre.

![](media/power-bi-visualization-slicers/slicer2.gif)

## <a name="when-to-use-a-slicer"></a>Mikor érdemes szeletelőt használni?
A szeletelő kiváló választást jelent a következő célokra.

* A gyakran használt vagy fontos szűrők megjelenítésére a jelentésvásznon a könnyebb elérhetőség érdekében.
* Az aktuális szűrt állapot egyszerűbb megjelenítésére, anélkül, hogy a legördülő listából kellene kiválasztani a szűrési részleteket.
* A nem szükséges oszlopok elrejtésére oly módon, hogy továbbra is használni lehessen azokat a szűréshez – szűkebb, letisztultabb táblákat téve lehetővé.
* Jobban szűrt jelentések létrehozására – mivel a szeletelők szövegen kívüli objektumok, a jelentés azon érdekes részei mellé helyezheti őket, amelyekre fel kívánja hívni a felhasználók figyelmét.

## <a name="create-a-slicer"></a>Szeletelő létrehozása
<iframe width="560" height="315" src="https://www.youtube.com/embed/zIZPA0UrJyA" frameborder="0" allowfullscreen></iframe>


1. Nyissa meg a [Kiskereskedelmi elemzési minta](sample-retail-analysis.md) elemet [Szerkesztő nézetben](service-interact-with-a-report-in-editing-view.md) és [adjon hozzá egy új oldalt a jelentéshez](power-bi-report-add-page.md).
2. A Mezők ablaktáblán válassza a **District (Körzet) > District Manager (Körzeti képviselő)** elemet.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_chartfirst.png)
3. Alakítsa át a vizualizációt szeletelővé. A Megjelenítések ablaktáblán kattintson a Szeletelő ikonra.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_select.png)

## <a name="format-the-slicer"></a>A szeletelő formázása
1. A kiválasztott szeletelővel a Megjelenítések ablaktáblán válassza a festőhenger ikont ![](media/power-bi-visualization-slicers/power-bi-paintroller.png) a formázási beállítások megjelenítéséhez.
2. Válassza az **Általános > Körvonal színe** lehetőséget, majd a sötétkék színt, és módosítsa a **Súly** értékét **6**-ra.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_outline2.png)
3. A **Kijelölési vezérlők**, szakaszban alapértelmezés szerint **Az összes kijelölése** **Ki** van kapcsolva, az **Egyetlen elem kijelölése** pedig **Be**. Ez azt jelenti, hogy egyszerre egynél több név kijelöléséhez a CTRL billentyűt kell használni. Kapcsolja **Be** **Az összes kijelölése** beállítást, az **Egyetlen elem kijelölése** beállítást pedig **Ki**.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_selectioncontrols2.png)
   
   * Figyelje meg, hogy a szeletelő most már rendelkezik egy **Az összes kijelölése** lehetőséggel a lista tetején. Az összes név kijelöléséhez kapcsolja **Az összes kijelölése** lehetőséget ki vagy be, vagy jelölje ki az egyik nevet.
   * Így immár egynél több nevet is kijelölhet a CTRL billentyű használata nélkül.
4. Az **Elemek** beállításban adja meg a 14 pontos szövegméretet.  Győződjön meg arról, hogy a munkatársai észreveszik a szeletelőt.
5. Végezetül állítsa be a **Betűszínt** sötétvörösre.  Ez megkülönbözteti a kijelölt neveket a nem kijelölt nevektől a szeletelőn.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_font2.png)
6. Jó szórakozást a szeletelőkhöz elérhető egyéb lehetőségek felfedezéséhez!

## <a name="use-the-slicer-in-a-report"></a>A szeletelő használata a jelentésekben
1. Vegyen fel néhány további vizualizációt a jelentésoldalról, vagy nyissa meg a [Kiskereskedelmi elemzési minta jelentést](sample-retail-analysis.md) és válassza a **District Monthly Sales** (Körzeti havi értékesítés) lapot.
   
    ![](media/power-bi-visualization-slicers/power-bi-retail-sample.png)
2. A jelentésoldalt szeletelje fel Carlos számára. Figyelje meg, ahogyan a vizualizációk a beállításoknak megfelelően frissítülnek.
   
    ![](media/power-bi-visualization-slicers/slicer2.gif)
3. A szeletelőt rendezze betűrendbe a körzeti képviselő vezetékneve szerint.  A szeletelő jobb felső sarkában kattintson a folytatást jelző pontokra (...) és válassza **District Manager** (Körzeti képviselő) elemet.
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_sort2.png)
   
    ![](media/power-bi-visualization-slicers/pbi_slicer_sorted.png)

## <a name="control-what-effect-the-slicer-has-on-other-visuals-on-the-page"></a>A szeletelő hatásának szabályozása az oldalon lévő egyéb vizualizációkra
Azt szeretné, hogy a jelentésoldalon csak a vizualizációk némelyikére szűrjön a szeletelő?  Használja a **Látványelem-interakciók** vezérlőt ennek beállítására.

**Megjegyzés:**: Ha nem látja a **Látványelem-interakciók** vezérlőt, keresse meg az ikonját ![](media/power-bi-visualization-slicers/power-bi-slicer-visual-interactions.png). Ha ezt sem látja, ellenőrizze, hogy a jelentés [szerkesztőnézetében](service-reading-view-and-editing-view.md) van-e.

1. Jelölje ki a szeletelőt, hogy aktív legyen, és a menüsorban kattintson a **Látványelem-interakciók** elemre.
   
    ![](media/power-bi-visualization-slicers/pbi-slicer-interactions.png)
2. A szűrővezérlők az egyéb vizualizációk felett jelennek meg az oldalon. Ha a szeletelőnek vizualizációt kell szűrnie, kattintson a **Szűrő** ikonra.  Ha a szeletelő nincs hatással a vizualizációra, kattintson a **Nincs** ikonra.
   
    ![](media/power-bi-visualization-slicers/filter-controls.png)

További információkért lásd: [Vizuális interakciók a Power BI-jelentésekben](service-reports-visual-interactions.md).

## <a name="considerations-and-troubleshooting-slicers-in-power-bi"></a>Szeletelők a Power BI-ban – szempontok és hibaelhárítás
A Power BI-ban a szeletelők használatára a következő korlátozások vonatkoznak:

1. A szeletelő nem támogatja a beviteli mezőket.
2. Egyetlen szeletelő nem használható a teljes jelentésen keresztül. A szeletelők csak az aktuális oldalra vannak hatással.
3. A szeletelő nem rögzíthető irányítópulthoz.
4. A szeletelők nem támogatják a részletezést.    
5. A szeletelő nem támogatja a vizualizáció szintű szűrőket.

Vannak a Power BI továbbfejlesztésére vonatkozó ötletei? [Ötlet beküldése](https://ideas.powerbi.com/forums/265200-power-bi-ideas).

## <a name="next-steps"></a>Következő lépések
 [Vizualizáció hozzáadása jelentéshez](power-bi-report-add-visualizations-i.md)

 [Vizualizációk típusai a Power BI-ban](power-bi-visualization-types-for-reports-and-q-and-a.md)

 [Power BI – Alapfogalmak](service-basic-concepts.md)

[Próbálja ki ingyenesen](https://powerbi.com/)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

