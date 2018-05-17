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
ms.date: 05/02/2018
ms.author: davidi
LocalizationGroup: Model your data
ms.openlocfilehash: 5cb7370942cdd4b50c8315a075eb7a178b05a692
ms.sourcegitcommit: f679c05d029ad0765976d530effde744eac23af5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/04/2018
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
