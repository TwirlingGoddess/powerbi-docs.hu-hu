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
ms.date: 11/20/2017
ms.author: mihart
ms.openlocfilehash: 3d51475b300fadc55f33960b03c3adc0031a39b8
ms.sourcegitcommit: 12236d08c27c7ee3fabb7ef9d767e9dee693f8aa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/21/2017
---
# <a name="getting-a-custom-visual-certified"></a>Egyéni vizualizáció *minősítésének* megszerzése
## <a name="what-is-meant-by-certified"></a>Mit értünk az alatt, hogy *minősített*?
A *minősített egyéni vizualizáció* olyan vizualizáció, amely megfelel bizonyos kódelőírásoknak, valamint szigorú biztonsági ellenőrzéseken is átment.  Az egyéni vizualizáció a minősítést követően [exportálható PowerPointba](service-publish-to-powerpoint.md), és megjeleníthető [az egyes jelentésoldalakra feliratkozott](service-report-subscribe.md) felhasználók által kapott e-mailekben is.

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
| [Őszirózsa diagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380759?src=office&tab=Overview) | |
| [Csokornyakkendő diagram a MAQ Software-től](https://appsource.microsoft.com/product/power-bi-visuals/WA104380838?src=office&tab=Overview) |[Videó](https://youtu.be/So5xKMSpVJI) |
| [BciCalendar (Beyondsoft naptár)](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104381096?src=office&tab=Overview)  | |
| [Doboz diagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380831?src=office&tab=Overview) | |
| [Skáladiagram](https://store.office.com/app.aspx?assetid=WA104380755) |[1. videó](https://youtu.be/AOlsFYkfkcw)   [2. videó](https://youtu.be/AQvd2FhRyCI) |
| [Skáladiagram az OKViztől](https://store.office.com/bullet-chart-by-okviz-WA104380953.aspx) |[Videó](https://youtu.be/mtvUNl9bMjA) |
| [Naptár a Tallantól](https://appsource.microsoft.com/product/power-bi-visuals/WA104381146?src=office&tab=Overview) | |
| [Gombsorszeletelő](https://store.office.com/chiclet-slicer-WA104380756.aspx) |[Videó](https://youtu.be/iYOkJ1APueY) |
| [Körszeletdiagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380761?src=office&tab=Overview) |[Videó](https://youtu.be/AQvd2FhRyCI) |
| [Kör alakú mérőműszer a MAQ Software-től](https://appsource.microsoft.com/product/power-bi-visuals/WA104380837?tab=Overview) | |
| [Hengeres mérőműszer](https://appsource.microsoft.com/product/power-bi-visuals/WA104380874) | |
| [Tárcsa alakú mérőműszer](https://appsource.microsoft.com/product/power-bi-visuals/WA104381184) |[Videó](https://youtu.be/AOlsFYkfkcw) |
| [Fánkdiagram (gyűrűdiagram) a MAQ Software-től](https://appsource.microsoft.com/product/power-bi-visuals/WA104380824?tab=Overview) |[Videó](https://youtu.be/pDToHDFHnq8) |
| [Pöttydiagram az OKViztől](https://appsource.microsoft.com/product/power-bi-visuals/WA104381101?src=office&tab=Overview) |[Videó](https://youtu.be/4lskRgcpFJY) |
| [Lefúrásos fánkdiagram a ZoomChartstól](https://appsource.microsoft.com/product/power-bi-visuals/WA104380858) | |
| [Kettős KPI](https://store.office.com/dual-kpi-WA104380774.aspx) |[Videó](https://youtu.be/821o0-eVBXo?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x) |
| [Enlighten Aquarium](https://appsource.microsoft.com/product/power-bi-visuals/WA104381112?src=office&tab=Overview) | |
| Enlighten World Flags – hamarosan elérhető | |
| Enlighten Stack Shuffle – hamarosan elérhető | |
| [Gantt](https://store.office.com/gantt-WA104380765.aspx) |[Videó](https://youtu.be/qJ7s_KrGiUU) |
| [Hisztogram](https://store.office.com/histogram-chart-WA104380776.aspx) | |
| [Vízszintes tölcsér](https://appsource.microsoft.com/product/power-bi-visuals/WA104380846) |[Videó](https://youtu.be/SudZei68PPo) |
| [KPI-kijelző](https://store.office.com/kpi-indicator-WA104380832.aspx) | |
| [Lineáris mérőműszer a MAQ Software-től](https://appsource.microsoft.com/product/power-bi-visuals/WA104380821?src=office&tab=Overview) |[Videó](https://youtu.be/AOlsFYkfkcw) |
| [Mekko diagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104380785?src=office&tab=Overview)  | [Videó](https://youtu.be/90FLCKpgicA)|
| [Lejátszási tengely (dinamikus szeletelő)](https://store.office.com/play-axis-dynamic-slicer-WA104380981.aspx) | |
| [Nagy teljesítményű KPI](https://appsource.microsoft.com/product/power-bi-visuals/WA104381083) |[Videó](https://youtu.be/IvfIP3E6-1Q) |
| [Sugárdiagram](https://store.office.com/radar-chart-WA104380771.aspx) | |
| [Gyűrűdiagram (fánkdiagram) a MAQ Software-től](https://appsource.microsoft.com/en-us/product/power-bi-visuals/WA104380824?src=office&tab=Overview) | [Videó](https://youtu.be/pDToHDFHnq8)|
| [Sankey diagram](https://store.office.com/app.aspx?assetid=WA104380777.aspx) |[Videó](https://youtu.be/WWP9wVUHGaA) |
| [Görgető](https://store.office.com/scroller-WA104381018.aspx) |[Videó](https://youtu.be/uhRFQF2cGSY) |
| [Intelligens szűrő az SQLBI-től](https://store.office.com/smart-filter-by-okviz-WA104380859.aspx) |[Videó](https://youtu.be/gcJsDDRQq28) |
| [Értékgörbe az OKViztől](https://appsource.microsoft.com/product/power-bi-visuals/WA104380910?src=office&tab=Overview) |[Videó](https://youtu.be/0m3Vnvso9tY) |
| [Többszintű gyűrű](https://appsource.microsoft.com/product/power-bi-visuals/WA104380767?src=office&tab=Overview) | |
| [Fordulatszámmérő](https://store.office.com/tachometer-WA104380937.aspx?) |[Videó](https://www.youtube.com/watch?v=C3OXdETbS9o) |
| [Hőmérő](https://appsource.microsoft.com/product/power-bi-visuals/WA104380847?src=office&tab=Overview) | [Videó](https://youtu.be/SPX9mgrAdBc)|
| [Idősorfelbontás](https://appsource.microsoft.com/product/power-bi-visuals/WA104380897) | |
| [Hőtérképtábla](https://store.office.com/table-heatmap-WA104380818.aspx) | |
| [Szövegburkoló](https://appsource.microsoft.com/product/power-bi-visuals/WA104380826) | |
| [Idővonal-szeletelő](https://store.office.com/timeline-slicer-WA104380786.aspx) |[Videó](https://youtu.be/ozMtZ4_NZ10) |
| [Tornádó diagram](https://store.office.com/tornado-chart-WA104380768.aspx) |[Videó](https://youtu.be/AQvd2FhRyCI) |
| [Gofri diagram](https://appsource.microsoft.com/product/power-bi-visuals/WA104381049?src=office&tab=Overview) |[Videó](https://youtu.be/1vRqYUsm3Vk) |
| [Szófelhő](https://store.office.com/word-cloud-WA104380752.aspx?) |[Videó](https://www.youtube.com/watch?v=AblTenl9fqo) |

## <a name="next-steps"></a>További lépések
[Bevezetés az egyéni vizualizációk fejlesztői eszközeinek használatába (előzetes verzió)](service-custom-visuals-getting-started-with-developer-tools.md)      
[A Microsoft az egyéni vizualizációkat bemutató lejátszási listája a YouTube-on](https://www.youtube.com/playlist?list=PL1N57mwBHtN1vIjfvuBIzZllrmKo-Vz6x)  
[Vizualizáció a Power BI-ban](power-bi-report-visualizations.md)  
[Egyéni vizualizáció a Power BI-ban](power-bi-custom-visuals.md)  
[Egyéni vizualizációk közzététele a Microsoft AppSource-ban](developer/office-store.md)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

