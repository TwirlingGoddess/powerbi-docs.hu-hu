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
ms.openlocfilehash: b5da2bf43f2d38e0828571e2b9d404feb615ac69
ms.sourcegitcommit: 312390f18b99de1123bf7a7674c6dffa8088529f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2018
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

1. Saját kép vissza gombként történő használatához helyezzen egy képi elemet a részletező oldalra.
2. Jelölje ki a képi elemet, és állítsa a **Vissza gomb** csúszkát bekapcsolt állásba. A kép most már vissza gombként működik.

    ![](media/desktop-drillthrough/drillthrough_05.png)

    Amikor a **részletezési** oldal elkészült, és a felhasználók a jobb gombbal egy adatpontra kattintanak a **Részletezési szűrők** szakaszba helyezett mezőt használó jelentésben, megjelenik egy helyi menü, amely támogatja az áthatolást az adott oldalra.

    ![](media/desktop-drillthrough/drillthrough_04.png)

    Amikor a jelentés felhasználói a részletezést választják, a rendszer szűri az oldalt, hogy megjelenítse azon adatpont információit, amelyre a jobb gombbal kattintottak. Ha például a Contoso (egy gyártó) egyik adatpontjára kattintottak a jobb gombbal, és a részletezést választották, a részletezés oldal, amelyre kerülnek, a Contoso cégre lesz szűrve.

    > [!NOTE]
    > Csak a **Részletezési szűrők** szakaszban lévő mező kerül át a részletező jelentésoldalra. Más környezeti információ nem jelenik meg rajta.
    > 
    > 

Ezek a legfontosabb tudnivalók a **részletezés** jelentésekben való használatáról. Ez nagyszerű mód a részletezési szűrőhöz kiválasztott entitásinformációk kibővített nézetének megjelenítésére.

