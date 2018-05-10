---
title: Részletezés használata a Power BI Desktopban
description: Megtudhatja, hogyan elemezheti részletesen az adatokat új jelentésoldalon a Power BI Desktopban.
services: powerbi
documentationcenter: ''
author: davidiseminger
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 4/10/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: 7be260a5989ffb6a9dc1b72dad90d227e0b6295b
ms.sourcegitcommit: bdb1fee3612bcc66153dcad8c4db2e99fb041014
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/28/2018
---
# <a name="use-drillthrough-in-power-bi-desktop"></a>Részletezés használata a Power BI Desktopban
A **Power BI Desktop** **részletezésével** olyan oldalt hozhat létre a jelentésben, amely adott entitásra összpontosít – például szállítóra, ügyfélre vagy gyártóra. Ezzel az összpontosított jelentésoldallal a felhasználók a jobb gombbal egy adatpontra kattinthatnak más jelentésoldalakon, és áthatolhatnak az összpontosított oldalra az ebben a környezetben szűrt részletek beszerzéséhez.

![](media/desktop-drillthrough/drillthrough_01.png)

## <a name="using-drillthrough"></a>A részletezés használata
1. A **részletezés** használatához hozzon létre egy jelentésoldalt, amely az azon entitástípusról megjeleníteni kívánt vizualizációkat tartalmazza, amelyhez a részletezést készíti. 

    Ha például gyártóknak szeretne áthatoló részletezést nyújtani, érdemes lehet olyan áthatoló részletezési oldalt létrehozni, amely az összes értékesítést, az összes kiszállított egységet, a kategória szerinti értékesítéseket, a régió szerinti értékesítéseket és egyebeket megjelenítő vizualizációkkal rendelkezik. Így amikor ehhez az oldalhoz jelenít meg részletezést, a vizualizációk arra a gyártóra fognak vonatkozni, amelyet kiválasztott.

2. Ezután a részletezési oldalon, a **Vizualizáció** panel **Mezők** szakaszában húzza a **Részletezési szűrők** szakaszra azt a mezőt, amelyhez részletezést szeretne készíteni.

    ![](media/desktop-drillthrough/drillthrough_02.png)

    Amikor egy mezőt a **Részletezési szűrők** szakaszhoz ad, a **Power BI Desktop** automatikusan létrehoz egy *Vissza* gomb vizualizációt. Ez a vizualizáció gombként működik a közzétett jelentésekben, és lehetővé teszi, hogy a jelentést a **Power BI szolgáltatásban** használó felhasználók könnyedén visszatérjenek a jelentésoldalra, amelyről érkeztek (az oldalra, ahol kiválasztották a részletezést).

    ![](media/desktop-drillthrough/drillthrough_03.png)

## <a name="use-your-own-image-for-a-back-button"></a>Saját kép használata vissza gombhoz    
 Mivel a vissza gomb egy kép, lecserélheti ezen vizualizáció képét bármilyen kívánt képre, és az továbbra is vissza gombként fog működni, vagyis a jelentés használói visszatérhetnek az eredeti oldalra.

1. Kattintson a **Kezdőlap** lapon a **Kép** elemre, majd keresse meg a képet, és helyezze a részletező oldalra.
2. Válassza ki az új képet a Részletezés oldalon, és a Kép formázása szakaszban kapcsolja be a **Hivatkozás** csúszkát, és állítsa be a **Típus** értékeként azt, hogy **Vissza**. A kép most már vissza gombként működik.

    ![](media/desktop-drillthrough/drillthrough_05.png)

    Amikor a **részletezési** oldal elkészült, és a felhasználók a jobb gombbal egy adatpontra kattintanak a **Részletezési szűrők** szakaszba helyezett mezőt használó jelentésben, megjelenik egy helyi menü, amely támogatja az áthatolást az adott oldalra.

    ![](media/desktop-drillthrough/drillthrough_04.png)

    Amikor a jelentés felhasználói a részletezést választják, a rendszer szűri az oldalt, hogy megjelenítse azon adatpont információit, amelyre a jobb gombbal kattintottak. Ha például a Contoso (egy gyártó) egyik adatpontjára kattintottak a jobb gombbal, és a részletezést választották, a részletezés oldal, amelyre kerülnek, a Contoso cégre lesz szűrve.

    > [!NOTE]
    > Csak a **Részletezési szűrők** szakaszban lévő mező kerül át a részletező jelentésoldalra. Más környezeti információ nem jelenik meg rajta.
    > 
    > 

Ezek a legfontosabb tudnivalók a **részletezés** jelentésekben való használatáról. Ez nagyszerű mód a részletezési szűrőhöz kiválasztott entitásinformációk kibővített nézetének megjelenítésére.

