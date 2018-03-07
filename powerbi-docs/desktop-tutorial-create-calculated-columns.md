---
title: "Oktatóanyag: Számított oszlopok létrehozása a Power BI Desktopban"
description: "Oktatóanyag: Számított oszlopok létrehozása a Power BI Desktopban"
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
ms.date: 12/06/2017
ms.author: davidi
LocalizationGroup: Learn more
ms.openlocfilehash: acdaa95908cd03006170eb06ddfc780c836c64ac
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="tutorial-create-calculated-columns-in-power-bi-desktop"></a>Oktatóanyag: Számított oszlopok létrehozása a Power BI Desktopban
Időnként az elemzett adatok nem tartalmazzák a kívánt eredményhez szükséges mezőt. Ekkor nyernek jelentőséget a számított oszlopok. A számított oszlopok Data Analysis Expressions- (DAX-) képleteket használnak az oszlopok értékeinek meghatározásához. Ezek az értékek bármik lehetnek, akár a modell más részében lévő különböző oszlopokból származó szöveges értékek összeállításáról, akár numerikus érték más értékekből való kiszámításáról van szó. Tegyük fel például, hogy az adatokban van egy Város és egy Állam oszlop (amelyek mezők a Mezők listában), de egyetlen olyan Hely mezőt szeretne, amelyben mindkettő szerepel egyetlen értékként (például Miami, FL). Pontosan erre szolgálnak a számított oszlopok.

A számított oszlopok hasonlóak a mértékekhez, mert mindkettő DAX-képleteken alapul, de a használatuk módja különböző. A mértékeket leggyakrabban a vizualizációk Értékek területén használják egy tábla sorában vagy a vizualizáció Tengely, Jelmagyarázat vagy Csoport területén lévő egyéb mezőkön alapuló eredményszámításhoz. A számított oszlopokat viszont akkor használják, amikor a tábla vagy a Tengely, Jelmagyarázat vagy Csoport terület egy adott sorának az oszloperedményeit szeretnék megjeleníteni.

Ez az oktatóanyag bemutatja, hogyan hozhat létre saját számított oszlopokat a Power BI Desktopban. Olyan Power BI-felhasználóknak szól, akik már elsajátították az összetettebb modellek létrehozásának eljárásait. Ehhez ismernie kell, hogyan importálhat adatokat a Lekérdezéssel, hogyan dolgozhat több kapcsolódó táblával, és hogyan adhat mezőket a jelentésvászonhoz. Ha még csak most ismerkedik a Power BI Desktoppal, mindenképp tekintse át a [Power BI Desktop használatának első lépéseit](desktop-getting-started.md) ismertető témakört.

Az oktatóanyag lépéseinek végrehajtásához töltse le a [Power BI Desktophoz készült Contoso értékesítési mintafájlt](http://download.microsoft.com/download/4/6/A/46AB5E74-50F6-4761-8EDB-5AE077FD603C/Contoso%20Sales%20Sample%20for%20Power%20BI%20Desktop.zip). Ez ugyanaz a mintafájl, amelyet a [Saját mértékek létrehozása a Power BI Desktopban](desktop-tutorial-create-measures.md) című oktatóanyagban is használtunk. Ez már eleve tartalmazza a fiktív Contoso, Inc. vállalat értékesítési adatait. Mivel a fájlban lévő adatok egy adatbázisból lettek importálva, nem tud majd az adatforráshoz kapcsolódni, illetve megtekinteni azt a Lekérdezésszerkesztőben. Miután letöltötte a fájlt a számítógépére, azonnal nyissa is meg azt a Power BI Desktopban.

## <a name="lets-create-a-calculated-column"></a>Számított oszlop létrehozása
Tegyük fel, hogy termékkategóriákat szeretne megjeleníteni termék-alkategóriákkal együtt egyetlen értéken belül a sorokon, például a Mobiltelefonok – Kellékek, Mobiltelefonok – Okostelefonok és PDA-k stb. kategóriákat. Ha a Jelentés nézetben vagy az Adatnézetben (itt a Jelentés nézetet használjuk) megnézzük a terméktáblákat a Mezők listában, láthatjuk, hogy nincs olyan mező, amelyben a kívánt eredmények szerepelnének. Van azonban egy ProductCategory (Termékkategória) mező és egy ProductSubcategory (Termék-alkategória) mező, mindegyik a saját táblájában.

 ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_nonewcol.png)

Létrehozunk egy új számított oszlopot, hogy ezen két oszlop értékeit új értékekké egyesítsük az új oszlop számára. Ehhez két különböző táblából kell egyetlen oszlopban egyesítenünk az adatokat. Mivel DAX-képlettel hozzuk létre az új oszlopot, kihasználhatjuk a már meglévő modell minden képességét, beleértve a már meglévő táblák közötti kapcsolatokat.

### <a name="to-create-a-productfullcategory-column"></a>ProductFullCategory oszlop létrehozása
1.  A Mezők listában kattintson jobb gombbal a **ProductSubcategory** táblára vagy bal gombbal a mellette lévő lefelé mutató nyílra, majd kattintson az **Új oszlop** gombra. Ez biztosítja, hogy az új oszlop a ProductSubcategory táblába kerüljön.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_newcolumn.png)
    
    A képletsáv megjelenik a jelentésvászon vagy az adatrács felső részén. Itt nevezhetjük át az oszlopot, és adhatunk hozzá DAX-képletet.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_newcolumnformula.png)
    
    Alapértelmezés szerint az új oszlopok neve egyszerűen Oszlop lesz. Ha ezt nem nevezzük át, a következő létrehozott mérték a 2. oszlop, 3. oszlop stb. nevet kapja majd. Mi azonban azt szeretnénk, ha az oszlopok könnyen azonosíthatóak lennének, ezért adjunk az új oszlopnak új nevet.
    
2.  Mivel az **Oszlop** név már ki van emelve a képletsávon, csak írja be a **ProductFullCategory** nevet.
    
    Most pedig lássunk hozzá a képlet megadásához. Azt szeretnénk, ha az új oszlopban lévő értékek a ProductCategory táblából származó ProductCategory névvel kezdődnének. Mivel ez az oszlop egy másik, de kapcsolódó táblában található, a [RELATED](https://msdn.microsoft.com/library/ee634202.aspx) függvényt használjuk a lekéréséhez.
    
3.  Az egyenlőségjel után írja be az **R** betűt. Egy lenyíló lista jelenik meg, amely felkínálja az összes R betűvel kezdődő DAX-képletet. Minél több karaktert ad meg, a lista annál jobban leszűkül a kívánt függvényre. A függvény mellett láthatja a függvény leírását. Görgessen le, és válassza a **RELATED** képletet, majd nyomja le az Enter billentyűt.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_1.png)
    
    Egy nyitó zárójel jelenik meg, valamint a RELATED függvénynek átadható oszlopokat tartalmazó javaslati lista. Megjelenik egy leírás és a várt paraméterek részletei is.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_2.png)
    
    A kifejezéseket mindig egy nyitó és egy záró zárójel fogja közre. Esetünkben a kifejezés egyetlen argumentumot tartalmaz, amelyet átadunk a RELATED függvénynek: azt a kapcsolódó oszlopot, amelyből értékeket adunk vissza. Az oszlopok listája automatikusan leszűkül, hogy csak a kapcsolódó oszlopokat jelenítse meg. Ebben az esetben a ProductCategory táblában lévő ProductCategory oszlopot szeretnénk átadni.
    
    Válassza a **ProductCategory[ProductCategory]** elemet, majd írjon be egy záró zárójelet.
    
    > [!TIP]
    > A szintaxishibákat leggyakrabban a hiányzó vagy rossz helyre beírt záró zárójelek okozzák, de a Power BI Desktop gyakran magától hozzáadja őket, ha elfeledkezik róluk.
    > 
    > 
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_3.png)
    
4. Hozzá szeretnénk adni egy kötőjel szimbólumot az egyes értékek elválasztásához, ezért az első kifejezés záró zárójele után írjon be egy szóközt, egy & jelet, egy idézőjelet, egy szóközt, egy kötőjelet (-), egy másik szóközt, egy záró zárójelet és egy másik & jelet. A képletnek most így kell kinéznie:
    
    **ProductFullCategory = RELATED(ProductCategory[ProductCategory]) & " - " &**
    
    > [!TIP]
    > Kattintson a lefelé mutató sávnyílra a képletsáv jobb oldalán a képletszerkesztő kibontásához. Nyomja le az Alt & Enter billentyűkombinációt, hogy lejjebb menjen egy sorral, és a Tab billentyűt az elmozgatáshoz.
    > 
    > 
    
5.  Végül írjon be egy másik nyitó szögletes zárójelet, majd válassza a **[ProductSubcategory]** oszlopot a képlet befejezéséhez. A képletnek így kell kinéznie:
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_5.png)
    
    Megfigyelheti, hogy nem kellett egy másik RELATED függvényt használni a ProductSubcategory oszlopot meghívó második kifejezésben. Ez azért van, mert ez az oszlop ugyanabban a táblában van, amelyben az új oszlopot létrehozzuk. A [ProductCategory] oszlopot a táblanévvel (teljes) vagy anélkül is (nem teljes) beírhatjuk.
    
6.  A képlet befejezéséhez nyomja le az Enter billentyűt, vagy kattintson a képletsávon lévő pipa jelre. A rendszer ellenőrzi a képletet, és hozzáadja a mezők listájához a **ProductSubcategory** táblában.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_pfc_6.png)
    
    Megfigyelhető, hogy a számított oszlopokat speciális ikon jelzi a mezők listájában. Ez az ikon mutatja, hogy az oszlopok képletet tartalmaznak. Csak a Power BI Desktopban jelennek meg ikonnal kiegészülve. A Power BI szolgáltatásban (az Ön Power BI-webhelyén) nem lehet módosítani a képleteket, ezért a számított oszlop mezőit nem kíséri ikon.
    
## <a name="lets-add-our-new-column-to-a-report"></a>Új oszlop hozzáadása a jelentéshez
Most hozzáadhatja az új ProductFullCategory oszlopot a jelentésvászonhoz. Tekintsük meg a SalesAmount (Értékesítés összege) értékét a ProductFullCategory elemei alapján.

Húzza a **ProductFullCategory** oszlopot a **ProductSubcategory** tábláról a jelentésvászonra, majd húzza a **SalesAmount** mezőt a **Sales** tábláról a diagramra.

![](media/desktop-tutorial-create-calculated-columns/calccol_fileds_report_1.png)

## <a name="lets-create-another"></a>Másik oszlop létrehozása
Most már tudja, hogyan hozhat létre számított oszlopot, így könnyen létrehozhat egy másikat.

A Power BI Desktop modellhez készült Contoso értékesítési minta aktív és inaktív áruházakra vonatkozó értékesítési adatokat is tartalmaz. Teljesen egyértelművé szeretnénk tenni az inaktív áruházakhoz megjelenített adatok inaktív mivoltát. Ez azt jelenti, hogy szükségünk van egy Active StoreName (Aktív áruháznév) nevű mezőre. Ehhez létre kell hozni egy másik oszlopot. Azt szeretnénk, hogy amikor egy áruház inaktív, az új Active StoreName oszlop (mint mező) „Inaktívként” jelenítse meg az áruház nevét, az aktív áruházaknak azonban a valódi neve jelenjen meg.

Szerencsére a Stores (Áruházak) táblában van egy Status (Állapot) oszlop, amelyben On (Be) érték szerepel az aktív áruházakhoz és Off (Ki) érték az inaktív áruházakhoz. Tesztelheti a Status oszlopban lévő sorok értékeit, hogy új értékeket hozzon létre az új oszlopban.

### <a name="to-create-an-active-storename-column"></a>Active StoreName (Aktív áruháznév) oszlop létrehozása
1.  Hozzon létre egy új, **Active StoreName** nevű számított oszlopot a **Stores** táblában.
    
    Ehhez az oszlophoz a DAX-képlet minden áruház állapotát ellenőrizni fogja. Ha egy áruház On (Be) állapotú, a képlet kiadja az áruház nevét. Ha Off (Ki) állapotú, a neve „Inaktív” lesz. A logikai [IF](https://msdn.microsoft.com/library/ee634824.aspx) függvényt használjuk az áruházak állapotának teszteléséhez és egy adott, az igaz vagy hamis eredménytől függő érték kiadásához.
    
2.  Kezdje el beírni az **IF** függvényt. A javaslati listában jelennek meg a lehetőségek, amelyek közül választhatunk. Válassza ki az **IF** függvényt.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_1.png)
    
    Az IF első argumentuma egy logikai teszt. Szeretnénk tesztelni, hogy egy áruház állapota „On” (Be) értékű-e.
    
3.  Írjon be egy nyitó szögletes zárójelet **[**, amely lehetővé teszi, hogy oszlopokat válasszunk a Stores táblából. Válassza a **[Status]** lehetőséget.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_2.png)
    
4.  A **[Status]** után közvetlenül írja be az **="On"** kifejezést, majd írjon be egy vesszőt (**,**) a második argumentum beírásához. Az eszköztipp azt javasolja, hogy hozzá kell adni azt az értéket, amit „igaz” eredmény esetén használunk.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_3.png)
    
5.  Ha az áruház On értékű, meg szeretnénk jeleníteni az áruház nevét. Írjon be egy nyitó szögletes zárójelet **[**, és válassza ki a **[StoreName]** oszlopot, majd írjon be egy másik vesszőt, hogy beírhassuk a harmadik argumentumot.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_step5.png)
    
6.  Meg kell adni azt az értéket, amit „hamis” eredmény esetén használunk, amely ebben az esetben az **„Inaktív”**.
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_step6.png)
    
7.  A képlet befejezéséhez nyomja le az Enter billentyűt, vagy kattintson a képletsávon lévő pipa jelre. A rendszer ellenőrzi a képletet, és hozzáadja a mezők listájához a Stores táblában.
    
    A többi mezőhöz hasonlóan használhatja az új Active StoreName oszlopot a vizualizációkban. Ebben a diagramban az On állapotú áruházak egyenként, név szerint jelennek meg, de az Off állapotú áruházak össze vannak csoportosítva, és az Inactive érték alatt jelennek meg. 
    
    ![](media/desktop-tutorial-create-calculated-columns/calccol_activestore_viz.png)
    
## <a name="what-weve-learned"></a>A megismert témák
A számított oszlopok tovább gazdagíthatják az adatokat, és megkönnyíthetik azok elemzését. Megtanultuk, hogyan hozhatók létre számított oszlopok a képletsávval, hogyan használható a javaslatok listája, és mi az új oszlopok elnevezésének a legjobb módja.

## <a name="next-steps"></a>Következő lépések
Ha szeretné a DAX-képleteket részletesebben megismerni, és összetettebb DAX-képletekkel szeretne létrehozni számított oszlopokat, olvassa el a cikket, amely [a DAX alapszintű használatát ismerteti a Power BI Desktopban](desktop-quickstart-learn-dax-basics.md). Ez a cikk a DAX alapvető fogalmaira, a szintaxisra, a függvényekre és a környezet alaposabb megértésére összpontosít.

Mindenképp vegye fel a [Data Analysis Expressions (DAX) referenciát](https://msdn.microsoft.com/library/gg413422.aspx) a kedvencei közé. Ebben találja részletesen leírva a DAX-szintaxist, az operátorokat, valamint a több mint 200 DAX-függvényt.

