---
title: "Könyvjelzők használata a Power BI-ban (előzetes verzió)"
description: "A Power BI Desktop könyvjelzői segítségével elmentheti a jelentések nézeteit és beállításait, valamint történetszerű bemutatókat hozhat létre"
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
ms.date: 10/12/2017
ms.author: davidi
ms.openlocfilehash: e60ff6d06e4ac0cddf398ccfc1d30e4d97e0773c
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/06/2017
---
# <a name="use-bookmarks-to-share-insights-and-build-stories-in-power-bi-preview"></a>Elemzések megosztása és történetek felépítése a Power BI könyvjelzőivel (előzetes verzió)
A Power BI-ban a **könyvjelzők** használatával rögzítheti az egyes jelentésoldalak aktuális nézetkonfigurációját, beleértve a szűréseket és a vizualizációk állapotát, hogy később egyszerűen a könyvjelzőre kattintva visszaállíthassa az adott állapotot. 

Egy tetszőleges sorrendbe rendezett teljes könyvjelzőgyűjteményt is létrehozhat, majd ezeket sorban megnyitva egy olyan bemutatót állíthat össze, amelyben lényegi összefüggések sorozatát mutathatja be, vagy előadhatja azt a történetet, amelyet a vizualizációkkal és a jelentésekkel be szeretne mutatni. 

![A Power BI könyvjelzői](media/desktop-bookmarks/bookmarks_01.png)

A könyvjelzőknek rengeteg felhasználási módja létezik. A segítségükkel nyomon követheti, hogy hol tart épp a jelentések készítésében (a könyvjelzők hozzáadása, törlése és átnevezése nem bonyolult dolog), illetve létrehozhat belőlük egy PowerPoint-szerű bemutatót is, amely a könyvjelzőkön végigléptetve bemutat egy történetet a jelentésen keresztül. Természetesen más alkalmazási területek is elképzelhetőek aszerint, hogy Ön mire szeretné leginkább használni a könyvjelzőket.

### <a name="enable-the-bookmarks-preview"></a>A könyvjelzők előzetes verziójának engedélyezése
Az új **könyvjelzők** funkció a **2017. októberi** kiadással vált elérhetővé a **Power BI Desktopban**, valamint a könyvjelző-kompatibilis jelentésekben a **Power BI szolgáltatásban**. Ennek az előzetes verziójú funkciónak az engedélyezéséhez válassza a **Fájl > Lehetőségek és beállítások > Beállítások > Előzetes verziójú funkciók** lehetőséget, majd jelölje be a **Könyvjelzők** elem melletti jelölőnégyzetet. Miután ezt beállította, újra kell indítania a Power BI Desktopot.

![A könyvjelzők engedélyezése a Beállítások ablakban](media/desktop-bookmarks/bookmarks_02.png)

Miután ezt beállította, újra kell indítania a **Power BI Desktopot**.

## <a name="using-bookmarks"></a>A könyvjelzők használata
A könyvjelzők használatához lépjen a **Nézet** menüszalagra, majd jelölje be a **Könyvjelzők panel** jelölőnégyzetét. 

![A Könyvjelzők panel megjelenítésének bekapcsolása a Nézet menüszalagon.](media/desktop-bookmarks/bookmarks_03.png)

A létrehozott könyvjelzőkhöz a rendszer a következő elemeket menti:

* Az aktuális oldal
* Szűrők
* Szeletelők
* A rendezés iránya
* A részletezés helye
* Láthatóság (az egyes objektumoké, a **Kiválasztás** panel használatával)
* A látható objektumok fókusz vagy **Reflektorfény** módja

A könyvjelzők jelenleg még nem mentik a keresztkiemelési állapotokat. 

Állítson be egy jelentésoldalt úgy, amilyen állapotban a könyvjelzővel menteni szeretné. Miután a jelentésoldalt és a vizualizációkat a kívánt módon elrendezte, a könyvjelző hozzáadásához válassza a **Könyvjelzők** panel **Hozzáadás** gombját. 

![Könyvjelző hozzáadása](media/desktop-bookmarks/bookmarks_04.png)

A **Power BI Desktop** létrehoz egy könyvjelzőt, amelynek egy általános nevet ad. A könyvjelzőket könnyen *átnevezheti*, *törölheti* vagy *frissítheti*, ha a könyvjelző neve melletti három pontra (...) kattint, majd kiválasztja a megfelelő műveletet a megjelenő menüből.

![Könyvjelző almenüjének kiválasztása a három pontra kattintva](media/desktop-bookmarks/bookmarks_05.png)

Miután létrehozott egy könyvjelzőt, a megjelenítéséhez egyszerűen kattintson rá a **Könyvjelzők** panelen. 

## <a name="arranging-bookmarks"></a>A könyvjelzők rendezése
Előfordulhat, hogy a könyvjelzőket nem olyan sorrendben hozza létre, amilyenben aztán be szeretné őket mutatni. Ez nem jelent problémát, mivel a könyvjelzőket könnyedén átrendezheti.

A **Könyvjelzők** panelen egyszerűen húzza át a könyvjelzőket a megfelelő sorrendbe, amint az alábbi képen is látható. A könyvjelzők közötti sárga vonal jelzi a helyet, ahová az elhúzott könyvjelző kerülni fog.

![Könyvjelzők sorrendjének módosítása áthúzással](media/desktop-bookmarks/bookmarks_06.png)

A könyvjelzők sorrendje a könyvjelzők **Nézet** funkciójának használatakor nyer jelentőséget, amint arra a következő szakasz kitér.

## <a name="bookmarks-as-a-slide-show"></a>Diavetítés a könyvjelzőkkel
Ha van több könyvjelzője, amelyeket sorrendben be szeretne mutatni, a **Könyvjelzők** panel **Nézet** gombjának kiválasztásával indíthatja el a diavetítést.

A **Nézet** módban érdemes odafigyelni a következőkre:

1. A könyvjelző neve a könyvjelző címsorában látható a vászon alján.
2. A könyvjelző címsorában lévő nyilakkal léptethet előre és hátra a könyvjelzők között.
3. A **Nézet** módból a **Könyvjelzők** panel **Kilépés** gombjával, vagy a könyvjelzők címsorán található **X** gombbal léphet ki. 

![Könyvjelző címsorának elemei](media/desktop-bookmarks/bookmarks_07.png)

A **Nézet** módban bezárhatja a **Könyvjelzők** panelt (a panel X gombjára kattintva), így több hely marad a bemutatónak. A **Nézet** módban az összes vizualizáció interaktívan kezelhető, és keresztkiemelést is lehet alkalmazni, ahogy a normál használat során is. 

## <a name="visibility---using-the-selection-pane"></a>Láthatóság – a Kiválasztás panel használatával
A könyvjelzőkkel együtt az új **Kiválasztás** panel is bevezetésre kerül. A **Kiválasztás** panel az aktuális oldalon lévő összes objektum listáját jeleníti meg, és lehetővé teszi az egyes objektumok kiválasztását és láthatóságának beállítását. 

![A Kiválasztás panel engedélyezése](media/desktop-bookmarks/bookmarks_08.png)

A **Kiválasztás** panelen kiválaszthatja az egyes objektumokat. Az egyes vizualizációk jobb oldalán lévő szem ikonra kattintva azt is ki- és bekapcsolhatja, hogy az adott objektum látható legyen-e. 

![Kiválasztás panel](media/desktop-bookmarks/bookmarks_09.png)

A könyvjelzők hozzáadásakor a rendszer az egyes objektumok láthatósági állapotát is menti a **Kiválasztás** panelen megadott beállítások szerint. 

Érdemes megjegyezni, hogy a **szeletelők** a láthatósági állapotuktól függetlenül szűrik a jelentésoldalt. Így számos különböző könyvjelzőt hozhat létre különböző szeletelőbeállításokkal, és az adott jelentésoldal sokféleképpen jelenhet meg (és különböző lényegi összefüggésekre mutathat rá) a különböző könyvjelzőkön.

## <a name="bookmarks-for-shapes-and-images"></a>Alakzatok és képek könyvjelzői
Alakzatokat és képeket is hozzárendelhet a könyvjelzőkhöz. Ezzel a funkcióval, ha egy objektumra kattint, megjelenik az adott objektumhoz rendelt könyvjelző. 

Egy könyvjelző objektumhoz rendeléséhez jelölje ki az objektumot, majd válassza a **Hivatkozás** gombot az **Alakzat formázása** panelen, amint az alábbi képen is látható.

![Könyvjelző-hivatkozás hozzárendelése egy objektumhoz](media/desktop-bookmarks/bookmarks_10.png)

Miután **Be** állásba kapcsolta a **Hivatkozás** kapcsolót, kiválaszthatja, hogy az objektum egy hivatkozás vagy könyvjelző legyen-e. Ha a könyvjelzőt választja, megadhatja, hogy a meglévő könyvjelzők közül melyikhez legyen az objektum rendelve.

Az objektumokhoz rendelt könyvjelzőknek számos felhasználási módja van. Létrehozhat egy látványos tartalomjegyzéket a jelentésoldalon, vagy egyszerűen az egyes objektumokra kattintva különböző nézeteket (például különféle vizualizációtípusokat) mutathat be ugyanazokról az adatokról.

A szerkesztési módban Ctrl+kattintással nyithatja meg a hivatkozásokat, a szerkesztési módon kívül pedig elég rákattintani az objektumra. 

## <a name="using-spotlight"></a>A Reflektorfény használata
A könyvjelzőkkel egy időben bevezetett másik funkció a **Reflektorfény**. A **Reflektorfénnyel** felhívhatja például a figyelmet egy adott diagramra, amikor a könyvjelzőket **Nézet** módban mutatja be.

Lássuk, miben különbözik a **Reflektorfény** a **fókusz** módtól.

1. **Fókusz** módban egyetlen vizualizáció tölti ki a teljes vásznat, ha a **fókusz mód** ikonra kattint.
2. A **Reflektorfény** használatával viszont az eredeti méretében emelheti ki a vizualizációt azáltal, hogy az oldalon lévő összes többi vizualizációt majdnem teljesen elhalványítja. 

![A fókusz mód és a reflektorfény összehasonlítása](media/desktop-bookmarks/bookmarks_11.png)

Ha az előző képen látható vizualizáció **fókusz** ikonjára kattintunk, az oldal így fog kinézni:

![fókusz mód](media/desktop-bookmarks/bookmarks_12.png)

Ezzel szemben, ha a vizualizáció menüjében (...) a **Reflektorfény** elemre kattintunk, az oldal így néz majd ki:

![reflektorfény mód](media/desktop-bookmarks/bookmarks_13.png)

Ha egy könyvjelző hozzáadásakor bármelyik mód (fókusz vagy reflektorfény) be van kapcsolva, a könyvjelző megőrzi a beállítást.

## <a name="bookmarks-in-the-power-bi-service"></a>A könyvjelzők a Power BI szolgáltatásban
Ha egy, a **Power BI szolgáltatásban** közzétett jelentés tartalmaz könyvjelzőket, azokat a **Power BI szolgáltatásban** is megtekintheti és használhatja. Ahhoz, hogy a könyvjelző funkció elérhető legyen egy adott jelentéshez a **Power BI szolgáltatásban**, a jelentésben már a közzététel előtt létre kell hozni legalább egy könyvjelzőt.

Ha a jelentés tartalmaz könyvjelzőket, a vonatkozó paneleket a **Nézet > Kiválasztás panel** vagy a **Nézet > Könyvjelzők panel** kiválasztásával jelenítheti meg.

![A Könyvjelzők és a Kiválasztás panel megjelenítése a Power BI szolgáltatásban](media/desktop-bookmarks/bookmarks_14.png)

A **Könyvjelzők panel** ugyanúgy működik a **Power BI szolgáltatásban**, mint a **Power BI Desktopban**. Itt is le tudja játszani a könyvjelzőket diavetítésként a **Nézet** kiválasztásával.

Ügyeljen arra, hogy a könyvjelzők között a könyvjelző szürke címsorán léptethet, és nem a fekete nyilakkal, ez utóbbiak ugyanis a jelentésoldalak, és nem a könyvjelzők közötti váltásra szolgálnak.

## <a name="limitations-and-considerations"></a>Korlátozások és szempontok
A **könyvjelzők** jelenlegi előzetes verziójú kiadásának a használatára vonatkozik néhány korlátozás és egyéb szempont.

* A szűrők *forrásaként* szolgáló egyéni vizualizációkon a könyvjelzők nem használhatók. Ha egyéni vizualizációkkal szűri egy oldal elemeit (például egy gombsorszeletelővel), és aztán egy könyvjelzővel megint megnyitja az oldalt, az oldal ugyan szűrve lehet, de az egyéni vizualizáció nem frissül, és nem mutatja, mi szerint van az oldal szűrve. 
* A könyvjelzők létrehozásakor a jelentéspanel keresztkiemelési állapota *nem* lesz mentve. 
* Ha egy vizualizációt a könyvjelző létrehozását követően ad hozzá a jelentésoldalhoz, a vizualizáció az alapértelmezett állapotában jelenik meg. Ez azt is jelenti, hogy ha egy olyan oldalra vesz fel szeletelőt, ahol már hozott létre könyvjelzőket, a szeletelő az alapértelmezett állapotának megfelelően viselkedik majd.
* Ha a vizualizációkat a könyvjelzők létrehozását követően áthelyezi, a változást a könyvjelzők lekövetik. 
* Ahhoz, hogy a könyvjelző funkció elérhető legyen a **Power BI szolgáltatásban**, a jelentésben már a közzététel idején lennie *kell* legalább egy könyvjelzőnek. Ez minden közzétett jelentésre külön-külön igaz.
* Könyvjelzők a [**Jelentéskészítő kiszolgálóhoz készült Power BI Desktopban**](report-server/quickstart-create-powerbi-report.md) egyelőre nem használhatók, mivel ez a funkció jelenleg előzetes verzióban érhető el.

## <a name="next-steps"></a>Következő lépések
A könyvjelzőkhöz hasonló vagy azokkal együtt használható funkciókkal kapcsolatos részletesebb információkat az alábbi cikkekben talál:

* [Részletezés használata a Power BI Desktopban](desktop-drillthrough.md)
* [Irányítópult-csempe vagy jelentésvizualizáció megjelenítése Fókusz módban](service-focus-mode.md)
