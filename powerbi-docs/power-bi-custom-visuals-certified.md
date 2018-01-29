---
title: "Minősített egyéni Power BI képi megjelenítések"
description: "Az egyéni vizualizációk minősítésre való beküldésének követelményei és folyamata. Továbbá a már minősített egyéni vizualizációk listája."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/20/2018
ms.author: mihart
ms.openlocfilehash: 90449f79da8aed3d992b9ac8bf83ac2ac4c0f83c
ms.sourcegitcommit: 2ae323fbed440c75847dc55fb3e21e9c744cfba0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/23/2018
---
# <a name="getting-a-custom-visual-certified"></a>Egyéni vizualizáció *minősítésének* megszerzése
## <a name="what-is-meant-by-certified"></a>Mit értünk az alatt, hogy *minősített*?
A *minősített egyéni vizualizáció* olyan vizualizáció, amely megfelel bizonyos kódelőírásoknak, valamint szigorú biztonsági ellenőrzéseken is átment.  Az egyéni vizualizáció a minősítést követően [exportálható PowerPointba](service-publish-to-powerpoint.md), és megjeleníthető [az egyes jelentésoldalakra feliratkozott](service-report-subscribe.md) felhasználók által kapott e-mailekben is. Természetesen [hagyományos egyéni vizualizációként](power-bi-custom-visuals.md) is használható, hozzáadható a Power BI szolgáltatáshoz és a Power BI Desktophoz, és megtekinthető a Power BI-mobilalkalmazásban és az Embeddedben.

Ön olyan webfejlesztő, aki szeretne saját képi megjelenítéseket létrehozni, és hozzáadni azokat a [Microsoft AppSource](https://appsource.microsoft.com) listájához? Ehhez tekintse át az [Ismerkedés a fejlesztői eszközökkel](service-custom-visuals-getting-started-with-developer-tools.md) című részt.


## <a name="certification-requirements"></a>Minősítési követelmények
* Microsoft AppSource-jóváhagyás    
* Az egyéni vizualizációt a verzióval ellátott API-k 1.2-es vagy újabb verzióival kell megírni    
* A kódtárat elérhetővé kell tenni felülvizsgálati célokra (például a vizualizáció kódját meg kell osztani velünk a GitHubon keresztül)    
* Csak nyilvánosan véleményezhető OSS-összetevők használata    
* Nem kapcsolódhat külső szolgáltatásokhoz és erőforrásokhoz    

> **TIPP**: Javasoljuk az EsLint az alapértelmezett biztonsági szabálykészlettel való használatát a kód előzetes ellenőrzésére a beküldés előtt.
> 
> 

## <a name="process-for-submitting-a-custom-visual-for-certification"></a>Az egyéni vizualizációk minősítésre való beküldésének folyamata
Egyéni vizualizáció beküldése minősítésre:

1. Küldjön egy e-mailt a Power BI egyéni vizualizációk támogatásáért felelő csapatának (pbicvsupport@microsoft.com). Az e-mailben adja meg az alábbi információkat:    
   
   * Cím: Vizualizáció minősítésére vonatkozó kérelem    
   * A vizualizáció forráskódját tartalmazó GitHub-adattárra mutató hivatkozás    
   * Feleljen meg a követelményeknek (lásd fent)    
   * Sikeres kód- és biztonsági felülvizsgálat    
2. A Microsoft egyéni vizualizációkért felelős csapata értesíti, amint az egyéni vizualizáció megkapja a minősítést, és elérhetővé válik a Minősített listában (alább), illetve a vizualizáció elutasítása esetén megküldi az orvosolandó problémák listáját. A fejlesztő felelőssége, hogy biztosítsa a megfelelő kommunikációt a Microsoft csapatával, és szükség esetén frissítse Minősített vizualizációit.

## <a name="removal-of-power-bi-certified-custom-visuals"></a>Minősített egyéni Power BI vizualizációk eltávolítása
A Microsoft saját belátása szerint eltávolíthatja a vizualizációkat a Minősített listáról.  

## <a name="list-of-custom-visuals-that-have-been-certified"></a>A már minősített egyéni vizualizációk listája
| Az AppSource-ra mutató hivatkozás | A videóra mutató hivatkozás |
| --- | --- |
| [Társítási szabályok](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380815) | |
| [Őszirózsa diagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380759?src=office&tab=Overview) | |
| [BciCalendar (Beyondsoft naptár)](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381096?src=office&tab=Overview)  | |
| [Csokornyakkendő diagram a MAQ Software-től](https://appsource.microsoft.com/product/power-bi-visuals/WA104380838?src=office&tab=Overview) |[Videó](https://youtu.be/So5xKMSpVJI) |
| [Doboz diagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380831?src=office&tab=Overview) | |
| [Tégladiagram a MAQ Software-től](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380836) | |
| [Buborékdiagram az Akvelontól](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381340?src=office) | |
| [Skáladiagram](https://store.office.com/app.aspx?assetid=WA104380755) |[1. videó](https://youtu.be/AOlsFYkfkcw)   [2. videó](https://youtu.be/AQvd2FhRyCI) |
| [Skáladiagram az OKViztől](https://store.office.com/bullet-chart-by-okviz-WA104380953.aspx) |[Videó](https://youtu.be/mtvUNl9bMjA) |
| [Naptár a Tallantól](https://appsource.microsoft.com/product/power-bi-visuals/WA104381146?src=office&tab=Overview) | |
| [Gyertya a OKViztől](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380952) | |
| [Gombsorszeletelő](https://store.office.com/chiclet-slicer-WA104380756.aspx) |[Videó](https://youtu.be/iYOkJ1APueY) |
| [Körszeletdiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380761?src=office&tab=Overview) |[Videó](https://youtu.be/AQvd2FhRyCI) |
| [Kör alakú mérőműszer a MAQ Software-től](https://appsource.microsoft.com/product/power-bi-visuals/WA104380837?tab=Overview) | |
| [Hengeres mérőműszer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380874) | |
| [Tárcsa alakú mérőműszer](https://appsource.microsoft.com/product/power-bi-visuals/WA104381184) |[Videó](https://youtu.be/AOlsFYkfkcw) |
| [Fánkdiagram (gyűrűdiagram) a MAQ Software-től](https://appsource.microsoft.com/product/power-bi-visuals/WA104380824?tab=Overview) |[Videó](https://youtu.be/pDToHDFHnq8) |
| [Pöttydiagram az MAQ Software-től](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381101) | |
| [Pöttydiagram az OKViztől](https://appsource.microsoft.com/product/power-bi-visuals/WA104381101?src=office&tab=Overview) |[Videó](https://youtu.be/4lskRgcpFJY) |
| [Pöttydiagram a Microsofttól](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380760?src=office) | |
| [Lefúrásos fánkdiagram a ZoomChartstól](https://appsource.microsoft.com/product/power-bi-visuals/WA104380858) | |
| [Drilldown Cartogram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381045?src=office) | |
| [Drilldown Choropleth](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381044?src=office) | |
| [Lefúrásos oszlopdiagram a ZoomChartstól](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380881?src=office) | |
| [Lefúrásos oszlopdiagram időalapú adatokhoz a ZoomChartstól](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380881) | |
| [Lefúrásos fánkdiagram a ZoomChartstól](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380858) | |
| [Kettős KPI](https://store.office.com/dual-kpi-WA104380774.aspx) |[Videó](https://youtu.be/821o0-eVBXo?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x) |
| [Bővített pont](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380762) | |
| [Enlighten Aquarium](https://appsource.microsoft.com/product/power-bi-visuals/WA104381112?src=office&tab=Overview) | |
| [Enlighten Bubble stack](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380868) | |
| [Enlighten Slicer](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380960?tab=Overview) | |
| [Enlighten Stack Shuffle](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380849) | |
| [Gofridiagram az Enlightentől](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380850) | |
| [Országzászlók az Enlightentől](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380923) | |
| [Előrejelzési TBATS](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381326?src=office) | |
| [Tölcsér forrással]() | || [Gantt](https://store.office.com/gantt-WA104380765.aspx) |[Videó](https://youtu.be/qJ7s_KrGiUU) |
| [Hierarchiadiagram az Akvelontól](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381333?src=office) | |
| [Hisztogram](https://store.office.com/histogram-chart-WA104380776.aspx) | |
| [Vízszintes tölcsér](https://appsource.microsoft.com/product/power-bi-visuals/WA104380846) |[Videó](https://youtu.be/SudZei68PPo) |
| [Képes idővonal](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381254) | |
| [Infografika-tervező](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380898?src=office) | |
| [KPI-kijelző](https://store.office.com/kpi-indicator-WA104380832.aspx) | |
| [KPI-szalagcím a MAQ Software-től](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380946) | |
| [Vonalpontos diagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380766?src=office) | |
| [Lineáris mérőműszer a MAQ Software-től](https://appsource.microsoft.com/product/power-bi-visuals/WA104380821?src=office&tab=Overview) |[Videó](https://youtu.be/AOlsFYkfkcw) |
| [Mekko diagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380785?src=office&tab=Overview)  | [Videó](https://youtu.be/90FLCKpgicA)|
| [Lejátszási tengely (dinamikus szeletelő)](https://store.office.com/play-axis-dynamic-slicer-WA104380981.aspx) | |
| [Nagy teljesítményű KPI](https://appsource.microsoft.com/product/power-bi-visuals/WA104381083) |[Videó](https://youtu.be/IvfIP3E6-1Q) |
| [Pulzusdiagram](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381006) | |
| [Sugárdiagram](https://store.office.com/radar-chart-WA104380771.aspx) | |
| [Gyűrűdiagram (fánkdiagram) a MAQ Software-től](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380824?src=office&tab=Overview) | [Videó](https://youtu.be/pDToHDFHnq8)|
| [Forgó diagram a MAQ Software-től](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381007?src=office) |  |
| [Sankey diagram](https://store.office.com/app.aspx?assetid=WA104380777.aspx) |[Videó](https://youtu.be/WWP9wVUHGaA) |
| [Görgető](https://store.office.com/scroller-WA104381018.aspx) |[Videó](https://youtu.be/uhRFQF2cGSY) |
| [Intelligens szűrő az SQLBI-től](https://store.office.com/smart-filter-by-okviz-WA104380859.aspx) |[Videó](https://youtu.be/gcJsDDRQq28) |
| [Értékgörbe az OKViztől](https://appsource.microsoft.com/product/power-bi-visuals/WA104380910?src=office&tab=Overview) |[Videó](https://youtu.be/0m3Vnvso9tY) |
| [Többszintű gyűrű](https://appsource.microsoft.com/product/power-bi-visuals/WA104380767?src=office&tab=Overview) | |
| [Hőtérképtábla](https://store.office.com/table-heatmap-WA104380818.aspx) | |
| [Fordulatszámmérő](https://store.office.com/tachometer-WA104380937.aspx?) |[Videó](https://www.youtube.com/watch?v=C3OXdETbS9o) |
| [Szövegburkoló](https://appsource.microsoft.com/product/power-bi-visuals/WA104380826) | |
| [Hőmérő](https://appsource.microsoft.com/product/power-bi-visuals/WA104380847?src=office&tab=Overview) | [Videó](https://youtu.be/SPX9mgrAdBc)|
| [Idősorfelbontás](https://appsource.microsoft.com/product/power-bi-visuals/WA104380897) | |
| [Idővonal-szeletelő](https://store.office.com/timeline-slicer-WA104380786.aspx) |[Videó](https://youtu.be/ozMtZ4_NZ10) |
| [Tornádó diagram](https://store.office.com/tornado-chart-WA104380768.aspx) |[Videó](https://youtu.be/AQvd2FhRyCI) |
| [Ultimate Varianciadiagram a Klaus Birringertől](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381140?src=office) | |
| [Ultimate Waterfall ingyenes](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380956) | |
| [VitaraCharts - MicroChart](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381165) | |
| [Gofri diagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104381049?src=office&tab=Overview) |[Videó](https://youtu.be/1vRqYUsm3Vk) |
| [Szófelhő](https://store.office.com/word-cloud-WA104380752.aspx?) |[Videó](https://www.youtube.com/watch?v=AblTenl9fqo) |

## <a name="next-steps"></a>További lépések
[Bevezetés az egyéni vizualizációk fejlesztői eszközeinek használatába (előzetes verzió)](service-custom-visuals-getting-started-with-developer-tools.md)      
[A Microsoft az egyéni vizualizációkat bemutató lejátszási listája a YouTube-on](https://www.youtube.com/playlist?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x)  
[Vizualizációk a Power BI-ban](power-bi-report-visualizations.md)  
[Egyéni vizualizáció a Power BI-ban](power-bi-custom-visuals.md)  
[Egyéni vizualizációk közzététele a Microsoft AppSource-ban](developer/office-store.md)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

