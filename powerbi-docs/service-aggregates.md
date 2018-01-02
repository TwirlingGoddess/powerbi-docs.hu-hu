---
title: "Összesítések (összeg, átlag, maximum stb.) a Power BI-ban"
description: "Diagramok összesítésének módosítása a Power BI-ban (összeg, átlag, maximum, stb.)"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: modifying
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/23/2017
ms.author: mihart
ms.openlocfilehash: c1b926e129e8d82edd9c329a51623908c4e7c9e0
ms.sourcegitcommit: 8f72ce6b35aa25979090a05e3827d4937dce6a0d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/27/2017
---
# <a name="aggregates-in-power-bi"></a>Összesítések a Power BI-ban
## <a name="what-is-an-aggregate"></a>Mi az az összesítés?
Néha szükség van egy adott oszlop sorértékeinek matematikai összevonására. Ez a matematikai művelet lehet összeadás, átlagolás, maximumérték meghatározása, darabszám meghatározása, stb. Egy adott oszlop soradatértékeinek összevonását nevezzük összesítésnek. Az ilyen matematikai műveletek eredménye az *összesítési érték*. 

A számmező az az érték, amellyel az összesítést végezzük (összeadás vagy átlagolás) egy adott kategóriamezőhöz kapcsolódóan.  Például „értékesítési összeg termék szerint” vagy „régiónkénti hibák száma”. A számmezőket gyakran **mértékeknek** nevezzük. A Mezők listában a mértékek ∑ szimbólummal vannak jelölve. További információ: [Jelentésszerkesztő – Bevezetés](service-the-report-editor-take-a-tour.md).

Néha egy adott *mérték* valójában *számított mértéknek* minősül. A számított mértékek importálása a Power BI-ban az adatokkal együtt történik (a jelentés alapjául szolgáló adatmodellben vannak meghatározva). Minden számított mértékhez saját nem változtatható képlet tartozik. A használandó összesítés módja nem módosítható, egy összeg például csak összeg lehet. A Mezők listában a *számított mértékek* számológép szimbólummal vannak ellátva. A számított mértékek létrehozásával kapcsolatos további információk: [Mértékek a Power BI Desktopban](desktop-measures.md).

A kategóriamezők ugyan nem számalapúak, de összesíthetőek.  Ha kategóriamezőket helyezünk egy *csak számalapú* gyűjtőbe (például **Értékek** vagy **Elemleírások**), a Power BI képes megszámlálni az egyes kategóriák normál vagy eltérő előfordulásait.  A sztringekkel és a dátumokkal kapcsolatban a Power BI további összevonási lehetőségeket kínál: legkorábbi, legújabb, első és utolsó.  

## <a name="why-dont-aggregates-work-the-way-i-want-them-to"></a>Miért nem az elvártnak megfelelően működnek az összesítések?
Az összesítések használata a Power BI-ban bonyolult lehet – például számmezőről van szó, és a Power BI nem engedélyezi az összesítés módosítását. Vagy esetleg olyan mezőről van szó (például évszám), amelynek nem kellene szerepelnie az összesítésben, csak az ahhoz tartozó előfordulások számát szeretnénk megszámlálni.

Leggyakrabban a problémát az adott mező Power BI-adatkészletben történő kategorizálása okozza. Elképzelhető, hogy a mező kategóriája szöveg, és emiatt nem lehet azt összeadáshoz vagy átlagoláshoz használni. Sajnos [csak az adatkészlet tulajdonosa tudja módosítani a mezők kategóriáját](desktop-measures.md).  

A félreértések elkerülése céljából a cikk végén szerepel egy **Tippek és hibaelhárítás** című szakasz.  Ha ebben nem találja meg a választ, tegye fel kérdését a [Power BI közösségi fórumában](http://community.powerbi.com), ahol gyors választ kaphat közvetlenül a Power BI csapatától.

## <a name="change-how-a-numeric-field-is-aggregated"></a>Számmezők összevonásának módosítása
Tegyük fel, hogy egy diagramban különböző régiókhoz tartozó értékesítési adatok összesítése szerepel, de Ön inkább átlagot számolna. 

1. A jelentés Szerkesztés nézetében adja hozzá a mértéket a vizualizációhoz.
2. Keresse meg az adott mezőt a Megjelenítések ablaktáblán, kattintson a jobb gombbal, majd válassza ki a kívánt összesítési típust. Ha nem látja a kívánt összesítést, forduljon az adatkészlet tulajdonosához. Elképzelhető, hogy a probléma a mező tulajdonos általi kategorizálásából származik.  
   
   ![](media/service-aggregates/aggregate_new.png)
   
   > [!NOTE]
   > A legördülő menüben elérhető lehetőségek a következőktől függenek: 1) a kijelölt mező, illetve 2) a mező adatkészlet-tulajdonos általi kategorizálása.
   > 
   > 

A mezők összesítésekor esetlegesen rendelkezésre álló lehetőségek:

* **Összegzés mellőzése**. A lehetőség használatakor az adott mező egyes értékeit a rendszer különállóként kezeli, és nem összegzi. Gyakran használható, ha olyan számazonosítós oszlopról van szó, amelyet nem kell összeadni.
* **Összeg**. Összeadja a mezőben szereplő összes értéket.
* **Átlag**. Az értékek számtani középértékét számítja ki.
* **Minimum**. A legkisebb értéket mutatja.
* **Maximum**. A legnagyobb értéket mutatja.
* **Darabszám (nem üres).** A nem üres mezőkben lévő értékek darabszámát adja vissza.
* **Darabszám (eltérők).** A mezőkben lévő különböző értékek darabszámát adja vissza.
* **Szórás.**
* **Variancia**.
* **Medián**.  A mediánt (középértéket) mutatja. Ez az az érték, amely hozzá képest ugyanannyi számú kisebb és nagyobb elemmel rendelkezik.  Ha 2 mediánról van szó, a Power BI átlagolja őket.

Nézzük például az alábbi adatokat:

| Ország | Összeg |
|:--- |:--- |
| Amerikai Egyesült Államok |100 |
| Egyesült Királyság |150 |
| Kanada |100 |
| Németország |125 |
| Franciaország | |
| Japán |125 |
| Ausztrália |150 |

Ezek az alábbi eredményeket adnák vissza:

* **Összegzés mellőzése**: minden érték külön jelenik meg
* **Összeg**: 750
* **Átlag**: 125
* **Maximum**:  150
* **Minimum**: 100
* **Darabszám (nem üres):** 6
* **Darabszám (eltérők):** 4
* **Szórás:** 20,4124145...
* **Variancia:** 416,666...
* **Medián:** 125

## <a name="use-a-non-aggregated-field-as-a-numeric-field"></a>Nem összesíthető mező használata számmezőként
Nem összesíthető mezőt is lehet használni számmezőként. Ha például egy Terméknév nevű mezőről van szó, felveheti értékként, majd beállíthatja azt a **Darabszám** vagy a **Darabszám (eltérők)** használatára. 

1. Például választhatja az **Áruház > Lánc** lehetőséget.
   
   ![](media/service-aggregates/count-of-chain-do_not_summarize.png)
2. Ha ilyenkor az összesítést az alapértelmezett **Összesítés mellőzése** lehetőségről a **Darabszám (eltérők)** lehetőségre módosítja, a Power BI megszámlálja a különböző láncokhoz tartozó darabszámot. Ebben az esetben 2 ilyen van: Fashions Direct és Lindseys.
   
   ![](media/service-aggregates/aggregates_count.png)
3. Ha az összesítést a **Darabszám** lehetőségre módosítja, a Power BI a teljes darabszámot adja vissza. Ebben az esetben a **Lánc** 104 tételt tartalmaz. A **Lánc** szűrőként való hozzáadásával láthatja, hogy a Fashions Direct tételhez 37, a Lindseys tételhez pedig 67 sor tartozik.  
   
   ![](media/service-aggregates/count_of_chain_104.png)

## <a name="tips-and-troubleshooting"></a>Tippek és hibaelhárítás
K: Miért nem látható az **Összeg mellőzése** lehetőség?

V: A kijelölt mező valószínűleg számított mérték. Ne feledje, minden számított mértékhez saját nem változtatható képlet tartozik. Nem lehet módosítani a számítást.

K: A mező **számalapú**. Miért csak a **Darabszám** és a **Darabszám (eltérők)** lehetőséget lehet kiválasztani?

V: A valószínű magyarázat az, hogy az adatkészlet tulajdonosa véletlenül vagy szándékosan *nem* számként kategorizálta az adott mezőt. Ha például egy adatkészletben szerepel az **Év** mező, az adatkészlet tulajdonosa szövegként kategorizálhatja azt, mivel valószínű, hogy az **Év** mező csak számlálásra (például az 1974-ben született személyek száma), nem pedig összeadásra vagy átlagolásra szolgál. Ha Ön a tulajdonos, az adatkészletet a Power BI Desktop alkalmazásban nyithatja meg, és a **Modellezés** lapon módosíthatja az adattípust.  

V: Egy másik lehetőség az, hogy az adott mezőt egy olyan *gyűjtőbe* helyezte, amely csak kategóriaértékeket engedélyez.  Ebben az esetben csak a Darabszám és a Darabszám (eltérők) típus érhető el.

V: A harmadik lehetőség pedig az, hogy tengelyen használja az adott mezőt. Például a sávdiagramok tengelyén a Power BI egy sávot jelenít meg mindegyik eltérő értékhez kapcsolódóan – és egyáltalán nem összesíti a mezőértékeket. 

>[!NOTE]
>Az egyetlen kivételt e szabály alól a pontdiagram képviseli, amely *megköveteli* az összesített értékek használatát az X és az Y tengelyeken.


K: Pontdiagramot használok, és szeretném, ha az adott mező *nem* szerepelne az összesítésben.  Hogyan lehet ezt elérni?

V: A **Részletek** gyűjtőbe vegye fel a mezőt, ne az X vagy Y tengelyhez tartozó gyűjtőbe.

K: Számmezők vizualizációhoz való hozzáadásakor azok többsége alapértelmezés szerint összeadásban szerepel, de a rendszer egyes mezőket átlagoláshoz, számláláshoz vagy egyéb összesítéshez használ.  Miért nem mindig ugyanazt az alapértelmezett összesítést használja a rendszer?

V: Az adatkészlet tulajdonosa állíthatja be az egyes mezőkhöz tartozó, alapértelmezett összesítést. Ha Ön az adatkészlet tulajdonosa, az alapértelmezett összesítést a Power BI Desktop **Modellezés** lapján módosíthatja.

K: **Numerikus** mezőt használok. Miért nincsenek összesítési lehetőségek a legördülő menüben?

V: A számológép ikonnal rendelkező mezők *számított mértéknek* minősülnek, és mindegyik számított mérték saját nem módosítható képlettel rendelkezik, amelyet nem lehet módosítani a Power BI szolgáltatásban. A használt számítás lehet egyszerű összesítés, mint például átlagolás vagy összeadás, de lehet bonyolultabb művelet is, mint például „szülőkategóriához való hozzájárulás százaléka” vagy „göngyölített összeg az év kezdete óta”. A Power BI nem összegzi vagy átlagolja az eredményeket, csak újraszámítást végez az egyes adatpontokhoz kapcsolódóan (a nem változtatható képlet használatával).

K: Adatkészlet-tulajdonos vagyok, és azt szeretném, hogy a rendszer egy adott mezőt soha ne használjon összesítéshez.

V: A Power BI Desktop **Modellezés** lapján állítsa be az **Adattípus** lehetőséget **Szöveg** típusra.

K: Nem látom az **Összegzés mellőzése** lehetőséget a legördülő menüben.

V: Próbálja eltávolítani a mezőt, majd vegye fel újra.

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

