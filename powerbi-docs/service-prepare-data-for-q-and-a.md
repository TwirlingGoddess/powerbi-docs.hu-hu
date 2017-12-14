---
title: "Megfelelő adatműködés biztosítása a Q&A és a Power BI használatánál"
description: "Megfelelő adatműködés biztosítása a Q&A és a Power BI használatánál"
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
ms.date: 09/26/2017
ms.author: mihart
ms.openlocfilehash: 499c3beca9046af9336de6dfec96994004050986
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="make-your-data-work-well-with-qa-in-power-bi"></a>Megfelelő adatműködés biztosítása a Q&A és a Power BI használatánál
Ha Ön a Power BI-jal használható adatmodelleket vagy Excel-munkafüzeteket készít, akkor olvasson tovább...

A Power BI-ban a Q&A olyan eszköz, amely strukturált adatok között keres, és kiválasztja az Ön kérdéséhez illő vizualizációt – ez teszi olyan vonzóvá a használatát.   

A Q&A bármely feltöltött Excel-fájllal működik, amely táblákat, tartományokat vagy PowerPivot-modelleket tartalmaz, de az optimalizálás és az adattisztítás még tovább fokozza a teljesítményét. 

## <a name="how-qa-works"></a>A Q&A működése
A Q&A része az alapvető természetes nyelvi értelmezési képességek halmaza, amelyek az Ön összes adatán működnek. Környezetfüggő kulcsszókeresést végez Excel-táblázatokban, -oszlopokban és számított mezőnevek között. Ezen kívül beépített képessége az adatok szűrése, rendezése, összesítése, csoportosítása és megjelenítése. 

Például egy “Eladások” nevű Excel-táblázatban, amelynek “Termék”, “Hónap”, “Eladott mennyiség”, “Bruttó bevétel” és “Nyereség” nevű oszlopai vannak, kérdéseket tehet fel ezek bármelyikével kapcsolatban.  Kérheti az eladások és az összes nyereség havonkénti kimutatását, a termékek eladott mennyiség szerinti rendezését és sok minden mást. Ismerje meg alaposabban [a feltehető kérdések fajtáit](http://blogs.msdn.com/b/powerbi/archive/2014/02/27/demystifying-power-bi-q-amp-a-part-1.aspx), [a kérdésfeltevést kérdéssablon alapján](service-q-and-a.md) és a [Q&A-lekérdezésben megadható vizualizációtípusokat](power-bi-visualization-types-for-reports-and-q-and-a.md).

## <a name="prepare-a-workbook-for-qa"></a>Munkafüzet előkészítése a Q&A használatához
A Q&A a táblázatok, oszlopok és számított mezők neve alapján válaszolja meg az adatokra vonatkozó kérdéseket, tehát lényeges a munkafüzet entitásainak elnevezése.

Néhány tanács a Q&A legjobb kihasználásához a munkafüzetben.

* Az adatai mindenképpen Excel-táblázatban legyenek. Sajátítsa el az [Excel-táblázatok létrehozását](https://support.office.com/article/Create-an-Excel-table-in-a-worksheet-e81aa349-b006-4f8a-9806-5af9df0ac664?ui=en-US&rs=en-US&ad=US).
* Ügyeljen rá, hogy a táblázatok, oszlopok és számított mezők neve érthető legyen az adott nyelven.
  
  Egy értékesítési adatokat tartalmazó táblázat neve például legyen “Értékesítés”. Az olyan oszlopnevek, mint “Év”, “Termék”, “Értékesítő” és “Mennyiség” jól használhatók a Q&A-ban.

> [!NOTE]
> Ha a munkafüzet PowerPivot-adatmodellt tartalmaz, akkor további optimalizálást is végezhet. Ismerkedjen meg a saját nyelvszakértőinkből álló csapat [A Power BI Q&A-val kapcsolatos mítoszok eloszlatása – 2. rész](http://blogs.msdn.com/b/powerbi/archive/2014/02/27/demystifying-power-bi-q-amp-a-part-2.aspx) című cikkét.
> 
> 

## <a name="next-steps"></a>További lépések
[Q&A a Power BI-ban](service-q-and-a.md)  
[Oktatóanyag: Bevezetés a Power BI Q&A használatába](power-bi-visualization-introduction-to-q-and-a.md)  
[Adatbeolvasás (a Power BI-ban)](service-get-data.md)  
[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

