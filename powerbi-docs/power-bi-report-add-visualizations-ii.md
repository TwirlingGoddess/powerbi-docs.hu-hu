---
title: "2. rész – Képi megjelenítések hozzáadása Power BI-jelentésekhez (oktatóanyag)"
description: "Oktatóanyag: 2. rész – Képi megjelenítések hozzáadása Power BI-jelentésekhez"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: 2b3f25c772a049d10bc03941db677c67c844da8b
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="part-2-add-visualizations-to-a-power-bi-report-tutorial"></a>2. rész – Képi megjelenítések hozzáadása Power BI-jelentésekhez (oktatóanyag)
Az [1. részben](power-bi-report-add-visualizations-ii.md) alapszintű képi megjelenítéseket hozott létre a mezők neve melletti jelölőnégyzetek bejelölésével.  A 2. részben megtudhatja, hogyan hozhat létre és módosíthat képi megjelenítéseket az egér húzásával, valamint a **Mezők** és a **Képi megjelenítések** panelek nyújtotta lehetőségek teljes körű kiaknázásával.

## <a name="create-a-new-visualization"></a>Új képi megjelenítés létrehozása
Ebben az oktatóanyagban a Kiskereskedelmi elemzés adatkészlet felhasználásával létrehozunk néhány fontosabb képi megjelenítést.

### <a name="open-a-report-and-add-a-new-blank-page"></a>Nyisson meg egy jelentést, és adjon hozzá egy üres oldalt.
1. Nyissa meg a munkaterületet, ahová a Kereskedelmi elemzési mintát mentette. A **Kiskereskedelmi elemzés minta** lehetőségre kattintva a jelentés az Olvasás nézetben nyílik meg.
   
   ![](media/power-bi-report-add-visualizations-ii/power-bi-open-report.png)
2. Válassza a **Jelentés szerkesztése** a jelentés Szerkesztési nézetben való megnyitásához.
   
   ![](media/power-bi-report-add-visualizations-ii/editreport1.png)
3. A vászon aljánál lévő sárga plusz ikonra kattintva [adhat hozzá egy új oldalt](power-bi-report-add-page.md).
   
   ![](media/power-bi-report-add-visualizations-ii/pbi_addreportpage.png)

### <a name="add-a-visualization-that-looks-at-this-years-sales-compared-to-last-year"></a>Adjon hozzá egy olyan képi megjelenítést, amely az idei értékesítési adatokat a tavalyiakkal veti össze.
1. Az **Értékesítés** táblában válassza az **Idei értékesítés** > **Érték** és a **Tavalyi értékesítések** mezőket. A Power BI létrehoz egy oszlopdiagramot.  Ez valamelyest azért érdekes, és nem árt a mélyére ásni. Hogy néz ki az értékesítés havi bontásban?  
   
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_4bnew.png)
2. Az Idő tábláról húzza a **Hónap** elemet a **Tengely** területre.  
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_5newnew.png)
3. [Módosítása a képi megjelenítést](power-bi-report-change-visualization-type.md) területdiagramra.  Számos különféle képi megjelenítési típusból választhat – ha segítségre van szüksége a választáshoz, olvassa át [az egyes típusok leírását, a bevált gyakorlatokra vonatkozó tanácsokat és az oktatóanyagokat](power-bi-visualization-types-for-reports-and-q-and-a.md). A Képi megjelenítések panelen válassza a Területdiagram ikont.
4. A képi megjelenítés rendezéséhez válassza a három pontot (...), majd a **Rendezés hónapok szerint** lehetőséget.
5. [A képi megjelenítés átméretezéséhez](power-bi-visualization-move-and-resize.md) jelölje ki a képi megjelenítést, majd fogja meg és húzza a külső körvonalak valamelyikét. Legyen elég széles ahhoz, hogy a görgetősáv már eltűnjön, de egy másik képi megjelenítés még elférjen mellette.
   
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_7b.png)
6. [Mentse a jelentést](service-report-save.md).

### <a name="add-a-map-visualization-that-looks-at-sales-by-location"></a>Térképi megjelenítés hozzáadása az értékesítések helyek szerinti megjelenítéséhez
1. Az **Üzletek** táblában válassza a **Terület** elemet. A Power BI felismeri, hogy a Terület helyet jelöl, ezért egy térképi megjelenítést hoz létre.  
   ![](media/power-bi-report-add-visualizations-ii/pbi_part2_8newnew.png)
2. Húzza az **Összes üzlet** elemet a Méret területre.  
   ![](media/power-bi-report-add-visualizations-ii/power-bi-add-visual-to-a-reportnew.png)
3. Adjon hozzá egy jelmagyarázatot.  Ha szeretné az adatokat az üzletek neve alapján megjeleníteni, húzza a **Lánc** mezőt a Jelmagyarázat területre.  
   ![](media/power-bi-report-add-visualizations-ii/power-bi-add-visual-to-a-report-3new.png)

## <a name="next-steps"></a>További lépések
* A Mezők panellel kapcsolatos további információkért lásd: [Jelentésszerkesztő – Bevezetés](service-the-report-editor-take-a-tour.md).   
* A vizualizációk adatainak szűrésével és kiemelésével kapcsolatos információkért lásd: [Szűrők és kiemelések a Power BI-jelentésekben](power-bi-reports-filters-and-highlighting.md).  
* Az összesítések használatával és módosításával kapcsolatos információkért lásd: [Összesítések a jelentésekben](service-aggregates.md).  
* További információk [a Power BI-jelentések vizualizációjáról](power-bi-report-visualizations.md).  
* További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/).
