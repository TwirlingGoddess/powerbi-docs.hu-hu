---
title: KPI-k importálása és megjelenítése a Power BI-ban
description: KPI-k importálása és megjelenítése
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
ms.date: 01/24/2018
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: deb6da926cafd78bfc12931ee731a6e2b2d6d44d
ms.sourcegitcommit: 3f2f254f6e8d18137bae879ddea0784e56b66895
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/26/2018
---
# <a name="import-and-display-kpis-in-power-bi"></a>KPI-k importálása és megjelenítése a Power BI-ban
A **Power BI Desktop** használatával KPI-ket importálhat és jeleníthet meg a táblákban, mátrixokban és kártyákon.

A KPI-k importálásához és megjelenítéséhez kövesse az alábbi lépéseket

1. Kezdje egy olyan Excel-fájllal, amely Power Pivot-modellel és KPI-kkel rendelkezik. Ebben a gyakorlatban egy *KPI-k* elnevezésű munkafüzetet használunk.

1. Importálja az Excel-munkafüzetet a Power BI-ba a **File -> Importálás -> Excel-munkafüzet tartalma** lehetőséggel. Így [a munkafüzetek importálásának módját is elsajátíthatja](desktop-import-excel-workbooks.md). 

1. A Power BI-ba történt importálás után a KPI megjelenik a ![jelzőlámpa](media/desktop-import-and-display-kpis/traffic.png) ikonnal jelölt **Mezők** panelen. Ahhoz, hogy a KPI-t felhasználhassa a jelentésben, ki kell bontania annak tartalmát, hogy megjelenjen az **Érték**, **Cél** és **Állapot** mező.

    ![](media/desktop-import-and-display-kpis/desktoppreviewfeatureon2.png)

1. Az importált KPI-ket érdemes szabványos vizualizáció-típusokban, például **Tábla** típusban felhasználni. A Power BI **KPI** vizualizáció-típust is tartalmaz, amely csak új KPI-k létrehozásához használandó.
   
    ![](media/desktop-import-and-display-kpis/desktoppreviewfeatureon3.png)

Ennyi az egész. Ezekkel a KPI-kkel trendeket, előrehaladást vagy egyéb jelentős mutatókat emelhet ki.
