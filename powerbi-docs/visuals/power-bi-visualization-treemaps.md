---
title: Fatérképek a Power BI-ban
description: Fatérképek a Power BI-ban
author: mihart
manager: kvivek
ms.reviewer: ''
featuredvideoid: IkJda4O7oGs
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 01/23/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: 946746b1c868ca5310edd929434cc852400b5bc3
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/21/2018
ms.locfileid: "46548074"
---
# <a name="treemaps-in-power-bi"></a>Fatérképek a Power BI-ban
A fatérképek a hierarchikus adatokat beágyazott téglalapokként jelenítik meg.  A hierarchia minden egyes szintjét egy színes téglalap (más néven „ág”) jelöli, amely további téglalapokat („leveleket”) tartalmaz.  Egy téglalapon belül a hely lefoglalása a mért mennyiségi értékek alapján, méret szerint rendezve történik – bal oldalt felül találhatók a legnagyobb téglalapok, jobbra alul pedig a legkisebbek.

![](media/power-bi-visualization-treemaps/pbi-nancy_viz_treemap.png)

Ha például az értékesítéseimet elemzem, akkor a ruházati kategóriák, vagyis az **Urban** (Városi), a **Rural** (Vidéki), a **Youth** (Fiatalok) és a **Mix** (Vegyes) kategóriák lehetnének a felső szintű téglalapjaim (ágaim).  A kategória-téglalapjaimon belül a kisebb téglalapok (levelek) az egyes kategóriák ruhagyártóihoz tartoznának, és ezek a kisebb téglalapok az eladási számok alapján lennének méretezve és színezve.  A fenti **Urban** ágban sok Maximus-ruhát értékesítenek, kevesebbet Natura- és Fama-ruhát, és nagyon kevés Leo-ruhát.  Így a fatérképemben az **Urban** ágban a Maximus kapná a legnagyobb téglalapot (a bal felső sarokban), valamivel kisebb téglalapok ábrázolnák a Naturát és a Famát, sok másik téglalap jelölné az egyéb eladott ruhákat, és egy egészen kicsi a Leót.  Az egyes levelek méretének és színének összevetésével más kategóriák eladásaival is összetudnám hasonlítani az eladásokat: minél nagyobb a téglalap és minél sötétebb a szín, annál nagyon értéket képvisel.

## <a name="when-to-use-a-treemap"></a>Mikor érdemes fatérképet használni
A fatérképek használata nagyszerű választás, ha:

* nagy mennyiségű hierarchikus adatot szeretne megjeleníteni;
* egy oszlopdiagram nem tudja hatékonyan kezelni a nagy mennyiségű értéket;
* az egyes részek és az egész közötti arányokat szeretné megjeleníteni;
* a hierarchia egyes kategóriaszintjein belül megfigyelhető eloszlási mintákat szeretné megjeleníteni;
* méret és színek alapján szeretne attribútumokat megjeleníteni;
* mintákat, kiugró adatokat, legfontosabb részvevőket és kivételeket szeretne azonosítani.

### <a name="prerequisites"></a>Előfeltételek
 - Power BI szolgáltatás vagy Power BI Desktop
 - Kiskereskedelmi elemzési minta

## <a name="create-a-basic-treemap"></a>Egyszerű fatérkép létrehozása
Szeretne előbb megnézni valaki mást, ahogyan létrehoz egy fatérképet?  Ugorjon a videóban 2:10-hez, hogy megnézhesse, hogyan hoz létre Amanda egy fatérképet.

<iframe width="560" height="315" src="https://www.youtube.com/embed/IkJda4O7oGs" frameborder="0" allowfullscreen></iframe>

Vagy hozzon létre saját fatérképet. Ez az útmutatás a Kiskereskedelmi elemzési mintát használja. Hogy követni tudja a lépéseket, jelentkezzen be a Power BI szolgáltatásba (ne a Desktopba), és válassza az **Adatok lekérése \> Minták \> Kiskereskedelmi elemzési minta \>  Kapcsolódás \> Ugrás az irányítópultra**  lehetőséget. Vizualizációkat csak akkor hozhat létre jelentésekben, ha jogosultsággal rendelkezik az adatkészlet és a jelentés szerkesztéséhez. A Power BI mintái szerkeszthetőek. Ha azonban mások osztanak meg Önnel jelentést, abban az esetben nem fog tudni új vizualizációkat létrehozni.

1. Nyissa meg a „Kiskereskedelmi elemzési minta” jelentést az „Összes áruház” csempe kiválasztásával.    
2. Nyissa meg a [Szerkesztő nézetet](../service-interact-with-a-report-in-editing-view.md), és válassza ki a **Sales** > **Last Years Sales** mértéket.   
   ![](media/power-bi-visualization-treemaps/treemapfirstvalue_new.png)   
3. Konvertálja a diagramot fatérképpé.  
   ![](media/power-bi-visualization-treemaps/treemapconvertto_new.png)   
4. Húzza az **Item** > **Category** elemet a **Csoport** gyűjtőbe. A Power BI ekkor létrehoz egy fatérképet, ahol a téglalapok méretei az összes értékesítést jelölik, a színeik pedig az egyes kategóriákat.  Lényegében egy olyan hierarchiát hozott létre, amely az összes értékesítés kategóriák szerinti relatív arányát jeleníti meg.  A **Mens** (Férfi) kategóriában található a legtöbb értékesítés, a **Hosiery** (Kötöttáru) kategóriában pedig a legkevesebb.   
   ![](media/power-bi-visualization-treemaps/treemapcomplete_new.png)   
5. Húzza a **Store** > **Chain** elemet a **Részletek** gyűjtőbe a fatérképe kiegészítéséhez. Így már kategóriák és üzletláncok szerint is össze tudja hasonlítani a tavalyi év értékesítéseit.   
   ![](media/power-bi-visualization-treemaps/treemap_addgroup_new.png)
   
   > [!NOTE]
   > A Színtelítettség és a Részletek gyűjtők nem használható egyszerre.
   > 
   > 
5. Helyezze a kurzort egy **Chain** elem fölé, hogy megjelenjen az adott **Kategória** elemleírása.  Ha például a **040-Juniors** téglalapban a **Lindseys** fölé helyezi a kurzort, akkor megjelenik a Juniors (Fiatalok) kategóriában található Lindsey-rész elemleírása.  
   ![](media/power-bi-visualization-treemaps/treemaphoverdetail_new.png)
6. [Vegye fel a fatérképet egy irányítópult-csempeként (rögzítse a vizualizációt)](../consumer/end-user-tiles.md). 
7. [Mentse a jelentést](../service-report-save.md).

## <a name="highlighting-and-cross-filtering"></a>Kiemelés és keresztszűrés
A Szűrők panel használatáról a [Szűrő hozzáadása jelentéshez](../power-bi-report-add-filter.md) című cikk nyújt tájékoztatást.

Egy kategória vagy részlet kijelölése egy fatérképen keresztkiemelést és keresztszűrést végez a jelentés oldalon lévő többi vizualizációval és viszont. Ehhez vagy adjon hozzá egy vizualizációt ugyanehhez az oldalhoz, vagy másolja a fatérképet, és illessze be egy olyan jelentési oldalra, amelyen már találhatók más vizualizációk.

1. A fatérképen válasszon egy kategóriát, vagy válasszon egy láncot egy kategórián belül.  Ez keresztkiemelést végez az oldalon található többi vizualizációval. A **050-Shoes** kiválasztása például megmutatja, hogy a tavalyi év cipőeladásai 3 640 471 $ értéket képviseltek, amelyből 2 174 185 $ a Fashion Directtől származott.  
   ![](media/power-bi-visualization-treemaps/treemaphiliting.png)

2. A **Last Year Sales by Chain** (Előző évi értékesítések üzletlánc szerint) tortadiagramban válassza a **Fashions Direct** szeletet, ezzel keresztszűrést végezhet a fatérképen.  
   ![](media/power-bi-visualization-treemaps/treemapnoowl.gif)    

3. A keresztkiemelések és keresztszűrések használatának módját a [Vizualizációk közötti interakciók Power BI-jelentésekben](../consumer/end-user-interactions.md) című cikk ismerteti.

## <a name="next-steps"></a>Következő lépések
[Vizualizáció rögzítése az irányítópulton](../service-dashboard-pin-tile-from-report.md)  
[Power BI – Alapfogalmak](../consumer/end-user-basic-concepts.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)  

