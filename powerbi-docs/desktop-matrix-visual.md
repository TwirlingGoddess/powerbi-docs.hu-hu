---
title: "A mátrixvizualizáció használata a Power BI Desktopban"
description: "Megismerheti, hogy a mátrixvizualizáció hogyan teszi lehetővé a lépcsőzetes elrendezéseket és a részletes kiemelést a Power BI Desktopban"
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
ms.date: 02/05/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: de40c8ee25c5facc1c4396c807d38784c11e8bca
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="use-the-matrix-visual-in-power-bi-desktop"></a>A Mátrix vizualizáció használata a Power BI Desktopban
A **Mátrix** vizualizációval mátrixvizualizációkat (más néven *táblákat*) hozhat létre a **Power BI Desktop** jelentéseiben, és egyéb vizualizációk mellett keresztkiemelést alkalmazhat a mátrix elemei között. Továbbá kiválaszthat sorokat, oszlopokat vagy egyetlen cellát is, és keresztkiemeléssel láthatja el őket. Végül az elrendezési terület jobb kihasználásának érdekében, a mátrixvizualizáció támogatja a lépcsőzetes elrendezést.

![](media/desktop-matrix-visual/matrix-visual_2a.png)

A mátrix számos funkcióval rendelkezik, amelyeket a cikk következő szakaszaiban be is mutatunk.

> [!NOTE]
> A **Power BI Desktop** 2017 júliusi kiadása óta a mátrix- és táblavizualizációk az alkalmazott **Jelentési téma** stílusát tükrözik (beleértve a színeket is). Előfordulhat, hogy nem ezeket a színeket szeretné használni a mátrixvizualizációban. Ezt a **Jelentési téma** konfigurációjában módosíthatja. A témákról szóló további információkért tekintse meg a [**jelentési témák a Power BI Desktopban történő használatát**](desktop-report-themes.md) ismertető szakaszt.
> 
> 

## <a name="understanding-how-power-bi-calculates-totals"></a>Hogyan számítja ki a Power BI az összegeket?

A **Mátrix** vizualizáció használatának ismertetése előtt fontos megérteni, hogy a Power BI hogyan számítja ki a táblázatok és mátrixok összegeit és részösszegeit. Az összegeket és részösszegeket tartalmazó sorok esetén a mögöttes adatok összes sorának mértéke adja az összeget, *nem* csak a látható vagy megjelenített sorok értékeinek összege. Ez azt jelenti, hogy az összeget tartalmazó sorban a várttól eltérő értékek szerepelhetnek. 

Tekintse meg az alábbi **Mátrix** vizualizációkat. 

![](media/desktop-matrix-visual/matrix-visual_3.png)

Ebben a példában a jobb szélső **Mátrix** vizualizáció minden sora az egyes értékesítő/dátum kombinációk *összegét* mutatja. Azonban mivel egy értékesítő több dátummal együtt is szerepel, a számok többször is előfordulhatnak. A mögöttes adatok pontos formája, valamint a látható adatok egyszerű összeadása így nem felel meg egymásnak. Ez egy gyakori trend akkor, ha az összegzett érték egy egy-a-többhöz kapcsolat egyéni oldalán áll.

Az összegek és a részösszegek megtekintésekor vegye figyelembe, hogy ezek az értékek a mögöttes adatokon alapulnak, és nem kizárólag a látható értékeken. 


## <a name="using-drill-down-with-the-matrix-visual"></a>Lehatolás használata a Mátrix vizualizációval
A **Mátrix** vizualizációval számos érdekes, korábban nem elérhető lehatolási tevékenység hajtható végre. Például a lehatolás sorok, oszlopok vagy külön szakaszok és cellák használatával. Vessünk egy pillantást ezek működésére.

### <a name="drill-down-on-row-headers"></a>Sorazonosítókon végzett lehatolás
Amikor a **Vizualizációk** ablaktáblán több mezőt ad hozzá a **Mezők** terület **Sorok** szakaszához, engedélyezi a mátrixvizualizáció sorain végzett lehatolást. Ez hasonlít egy hierarchia létrehozásához, amely utána lehetővé teszi a hierarchián keresztül való lehatolást (majd felhatolást) és az adatok elemzését minden szinten.

Az alábbi képen a **Sorok** szakasz egy *Kategória* és egy *Alkategória* részt tartalmaz, létrehozva egy csoportosítást (vagy hierarchiát) a részletezhető sorokban.

![](media/desktop-matrix-visual/matrix-visual_4.png)

Ha a vizualizáció a **Sorok** szakaszban csoportosítást tartalmaz, a vizualizáció megjeleníti a *részletezés* és *kibontás* ikont a vizualizáció bal felső sarkában.

![](media/desktop-matrix-visual/matrix-visual_5.png)

Az egyéb vizualizációk részletezési és kibontási viselkedéséhez hasonlóan, ha ezekre a gombokra kattint, akkor lehetőség nyílik a lehatolásra (vagy felhatolásra) a hierarchián keresztül. Ebben az esetben lehatolhatunk a *Kategóriából* az *Alkategóriához*, ahogy az alábbi képen is látható, ahol a „lehatolás egy szinttel” ikon (a lefelé mutató villa) lett kiválasztva.

![](media/desktop-matrix-visual/matrix-visual_6.png)

Az ikonok használatán kívül a jobb gombbal is kattinthat bármelyik sorazonosítóra, és részletes elemzést végezhet, ha kiválasztja ezt a lehetőséget a megjelenő menüből.

![](media/desktop-matrix-visual/matrix-visual_7.png)

Figyelje meg, hogy van néhány lehetőség a megjelenő menüben, amely különböző eredményekhez vezet:

A **Részletes elemzés** kiválasztása kibontja az *ahhoz* a sorszinthez tartozó mátrixot, *kivéve* az egyéb összes sorfejlécet, annak a sorazonosítónak a kivételével, amelyre a jobb gombbal kattintott. Az alábbi képen a *Számítógépekre* a jobb gombbal kattintottak, és a **Részletes elemzés** lett kiválasztva. Figyelje meg, hogy egyéb legfelső szintű sorok már nem jelennek meg a mátrixban. Ez egy hasznos funkció, amely a **keresztkiemelés** szakaszban válik igazán hasznossá.

![](media/desktop-matrix-visual/matrix-visual_8.png)

Ha a **Felhatolás** ikonra kattintunk, visszajutunk az előző, legfelső szintű nézethez. Ha ezután a **Következő szint megjelenítése** lehetőséget választja a helyi menüből, megjelenik a következő szinten (ebben az esetben az *Alkategória* mezőben) lévő elemek betűrendbe szedett listája, a magasabb szintű hierarchia-kategorizálás nélkül.

![](media/desktop-matrix-visual/matrix-visual_8a.png)

Ha a bal felső sarokban található **Felhatolás** ikonra kattintunk, hogy a mátrix megjelenítse a legfelső szintű kategóriákat, majd a jobb gombbal ismét kattintunk, és kiválasztjuk a **Kibontás a következő szintre** elemet, a következő jelenik meg:

![](media/desktop-matrix-visual/matrix-visual_9.png)

A **Belefoglalás** és a **Kizárás** menüelemet is használhatja annak a sornak (és bármely alkategóriának) a kizáráshoz (vagy eltávolításához) a mátrixból, amelyre a jobb gombbal kattintott.

### <a name="drill-down-on-column-headers"></a>Oszlopfejléceken végzett lehatolás
A Sorokon végzett lehatoláshoz hasonlóan, az **Oszlopokon** is végezhet lehatolást. Az alábbi képen két mező található az **Oszlopok** mező területén, egy ahhoz hasonló hierarchiát létrehozva, amilyet a sorokhoz használtunk a cikk korábbi szakaszában. Az **Oszlopok** mező területén az *Osztály* és a *Szín* található.

![](media/desktop-matrix-visual/matrix-visual_10.png)

A **Mátrix** vizualizációban, ha a jobb gombbal az oszlopra kattintunk, megjelenik a lehatolás elvégzésének lehetősége. Az alábbi képen a jobb gombbal kattintottunk a *Deluxe* elemre, és kiválasztottuk a **Részletes elemzést**.

![](media/desktop-matrix-visual/matrix-visual_11.png)

A **Részletes elemzés** kiválasztása után, megjelenik a *Deluxe* oszlophierarchiájának következő szintje, ami ebben az esetben a *Szín*.

![](media/desktop-matrix-visual/matrix-visual_12.png)

A helyi menü többi eleme ugyanúgy működik az Oszlopok, ahogy a sorok esetében (lásd az előző szakaszt: **Sorazonosítókon végzett lehatolás**). **Megjelenítheti a következő szintet**, **kibonthat a következő szintre**, és a sorokhoz hasonlóan **belefoglalhatja** vagy **kizárhatja** az oszlopokat.

> [!NOTE]
> A lehatolás és felhatolás ikonjai a mátrixvizualizáció bal felső sarkában csak a sorokra vonatkoznak. Ha oszlopokon szeretne lehatolást végezni, a helyi menüt kell használnia (a jobb gombbal kattintva).
> 
> 

## <a name="stepped-layout-with-matrix-visuals"></a>Lépcsőzetes elrendezés mátrixvizualizációkkal
A **Mátrix** vizualizáció automatikusan behúzza egy hierarchia alkategóriáit minden szülő alatt, és ezt **lépcsőzetes elrendezésnek** hívjuk.

A mátrixvizualizáció *eredeti* verziójában az alkategóriák egy teljesen külön oszlopban jelentek meg, több helyet foglalva a vizualizációban. Az alábbi képen az eredeti **mátrix**vizualizáció egy táblája látható. Figyelje meg, hogy az alkategóriák egy teljesen külön oszlopban vannak.

![](media/desktop-matrix-visual/matrix-visual_14.png)

Az alábbi képen a **Mátrix** vizualizáció látható **lépcsőzetes elrendezéssel**. Figyelje meg, hogy a *Számítógépek* kategória saját, kis mértékben behúzott alkategóriákkal rendelkezik (Számítógép-kiegészítők, Asztali számítógépek, Laptopok, Monitorok stb.), ezzel átláthatóbb és tömörebb vizualizációt biztosít.

![](media/desktop-matrix-visual/matrix-visual_13.png)

A **lépcsőzetes elrendezés** beállításait egyszerűen módosíthatja. Ha a **Mátrix** vizualizáció van kiválasztva, a **Vizualizációk** ablaktábla **Formátum** szakaszában (festőhenger ikon) bontsa ki a **Sorazonosítók** szakaszt. Két lehetőség érhető el: a **Lépcsőzetes elrendezés** váltógomb (amely ki- vagy bekapcsolja ezt az elrendezést) és a **Lépcsőzetes elrendezés behúzása** (a behúzás mértékét adja meg képpontokban).

![](media/desktop-matrix-visual/matrix-visual_15.png)

Ha kikapcsolja a **Lépcsőzetes elrendezést**, az alkategóriák egy másik oszlopban jelennek meg, nem pedig a szülőkategória alatt behúzva.

## <a name="subtotals-with-matrix-visuals"></a>Részösszegek a mátrixvizualizációkkal
A részösszegeket a soroknál és oszlopoknál is ki- vagy bekapcsolhatja a mátrixvizualizációkban. Az alábbi képen látható, hogy a sorok részösszegei **be** vannak kapcsolva.

![](media/desktop-matrix-visual/matrix-visual_20.png)

A **Vizualizációk** ablaktábla **Formátum** szakaszában (festőhenger ikon) bontsa ki a **Részösszegek** kártyát, és állítsa a **Sorok részösszegei** csúszkát a **Ki** beállításra. Ha így tesz, a részösszegek nem jelennek meg.

![](media/desktop-matrix-visual/matrix-visual_21.png)

Ugyanez a folyamat vonatkozik az oszlopok részösszegeire.

## <a name="cross-highlighting-with-matrix-visuals"></a>Keresztkijelölés a mátrixvizualizációkkal
A **Mátrix** vizualizációval a mátrix bármely eleme kiválasztható a keresztkijelölés alapjaként. Válasszon ki egy oszlopot a **Mátrixban**, ez az oszlop ki lesz emelve csakúgy, mint a jelentés lapon látható bármely egyéb vizualizáció. Ez az egyéb vizualizációk és egy adatpont kiválasztásának közös funkciója volt, de már a **Mátrix** vizualizációnál is elérhető.

Továbbá a Ctrl+kattintás is használható a keresztkijelöléshez. Például az alábbi képen alkategóriák egy gyűjteménye lett kiválasztva a **Mátrix** vizualizációból. Figyelje meg, hogy a vizualizációból ki nem választott elemek kiszürkítve jelennek meg, és az oldalon található egyéb vizualizációk a **Mátrix** vizualizációban végzett kijelöléseket tükrözik.

![](media/desktop-matrix-visual/matrix-visual_16.png)

## <a name="shading-and-font-colors-with-matrix-visuals"></a>Árnyékolás és betűtípus mátrixvizualizációkkal
A **Mátrix** vizualizációval **feltételes formázást** (színek és árnyékolás) alkalmazhat a mátrixban található cellák hátterére, valamint magára a szövegre és az értékekre is.

Feltételes formázás alkalmazásához a következő lehetőségek közül választhat, ha ki van választva egy mátrixvizualizáció:

* A **Mezők** ablaktáblán kattintson a jobb gombbal a Mezőre, és a menüből válassza a **Feltételes formázás** elemet.
  
  ![](media/desktop-matrix-visual/matrix-visual_17.png)
* Vagy a **Formátum** ablaktáblán bontsa ki a **Feltételes formázás** kártyát, és állítsa a **Háttérszínek színskálái** vagy a **Betűszínek színskálái** csúszkát **Be** állapotúra. Bármelyik bekapcsolása után megjelenik a *Speciális vezérlők* hivatkozása, amely lehetővé teszi a színek és a színformátum értékeinek testreszabását.
  
  ![](media/desktop-matrix-visual/matrix-visual_18.png)

Bármelyik módszerrel ugyanaz az eredmény érhető el. A *Speciális vezérlők* kiválasztása az alábbi párbeszédpanelt jeleníti meg, amely lehetővé teszi a módosítások végrehajtását:

![](media/desktop-matrix-visual/matrix-visual_19.png)

## <a name="next-steps"></a>Következő lépések

Az alábbi cikkeket is érdekesnek találhatja:

* [Rácsvonalak és rácshoz illesztés használata Power BI Desktop-jelentésekben](desktop-gridlines-snap-to-grid.md)
* [Adatforrások a Power BI Desktopban](desktop-data-sources.md)
* [Adattípusok a Power BI Desktopban](desktop-data-types.md)

 