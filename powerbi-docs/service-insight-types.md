---
title: "A Power BI által támogatott gyors elemzések típusai"
description: "Gyors elemzések a Power BI-jal."
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
ms.date: 09/03/2017
ms.author: mihart
ms.openlocfilehash: 13f5614cf121b17d8ae4dff9653f5789372f7f49
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="types-of-quick-insights-supported-by-power-bi"></a>A Power BI által támogatott gyors elemzések típusai
## <a name="how-does-quick-insights-work"></a>A Gyors elemzések működése
A Power BI kifinomult algoritmusok alkalmazásával részhalmazokat keres az adatkészletben potenciálisan érdekes összefüggések feltárásához. A Power BI adott idő alatt annyi adatot vizsgál meg az adatkészletből, amennyit csak tud.

Gyors elemzést adatkészletre vagy csempére vonatkozóan is futtathat. A csempére vonatkozó elemzések az úgynevezett Kapcsolódó elemzések.   

## <a name="what-types-of-quick-insights-can-we-find"></a>Milyen összefüggések tárhatók fel a Gyors elemzésekkel?
A rendszer többek között az alábbi algoritmusokat használja:

## <a name="category-outliers-topbottom"></a>Kiugró (alsó vagy felső) értékek a kategóriában
Az adatmodell valamely kategóriája vonatkozásában kiemeli azokat az eseteket, amelyeknél adott dimenzióban az egyik vagy másik elem értéke sokkal nagyobb vagy alacsonyabb, mint a többié.  

![](media/service-insight-types/pbi_auto_insight_types_category_outliers.png)

## <a name="change-points-in-a-time-series"></a>Időbeli adatsorok változási pontjai
Időbeli adatsoroknál kiemeli, hogy mikor következett be szignifikáns változás a trendekben.

![](media/service-insight-types/pbi_auto_insight_types_changepoint.png)

## <a name="correlation"></a>Korreláció
Észleli, hogy az adatkészletet egy adott dimenzió mentén ábrázolva milyen eseteken korrelálnak egymással a különböző kategóriák értékei.

![](media/service-insight-types/pbi_auto_insight_types_correlation.png)

## <a name="low-variance"></a>Alacsony variancia
Észleli azokat az eseteket, melyeknél az adatpontok közel vannak az átlaghoz.

![](media/service-insight-types/power-bi-low-variance.png)

## <a name="majority-major-factors"></a>Többség (fő tényezők)
Megkeresi azokat az eseteket, amelyekben az összérték többségi aránya egy másik dimenzió mentén vizsgálva egyetlen tényezőnek tudható be.  

![](media/service-insight-types/pbi_auto_insight_types_majority.png)

## <a name="overall-trends-in-time-series"></a>Időbeli adatsorok általános trendjei
Észleli az időrendben elérhető adatok növekvő és csökkenő trendjeit.

![](media/service-insight-types/pbi_auto_insight_types_trend.png)

## <a name="seasonality-in-time-series"></a>Időbeli adatsorok szezonális változásai
Azt vizsgálja, hogy felfedezhetőek-e heti, havi vagy éves gyakorisággal ismétlődő minták az időbeli adatsorokban.

![](media/service-insight-types/pbi_auto_insight_types_seasonality_new.png)

## <a name="steady-share"></a>Állandó részesedés
Kiemeli azokat az eseteket, amelyekben szülő-gyermek típusú korreláció fedezhető fel egy gyermek érték részesedése és egy folyamatos változó mentén vizsgált teljes szülő érték között.

![](media/service-insight-types/pbi_auto_insight_types_steadyshare.png)

## <a name="time-series-outliers"></a>Kiugró értékek egy időbeli adatsorban
Időrendben elérhető adatok esetén észleli, hogy vannak-e olyan dátumok vagy időpontok, melyeknél az érték szignifikánsan eltér a többi dátumhoz/időponthoz tartozó értéktől.

![](media/service-insight-types/pbi_auto_insight_types_time_series_outliers.png)

## <a name="next-steps"></a>További lépések
[Power BI – gyors elemzések](service-insights.md)

Ha Ön az adatkészlet tulajdonosa, [optimalizálhatja azt gyors elemzések készítéséhez](service-insights-optimize.md)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

