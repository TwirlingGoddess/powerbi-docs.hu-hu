---
title: "Ismerkedés a Power BI jelentéskészítő kiszolgálóval"
description: "Ismerje meg, hogyan telepítheti a Power BI jelentéskészítő kiszolgálót. "
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 3/5/2018
ms.author: maghan
ms.openlocfilehash: 88aa347a5e6feae969cf9b32e0e2177114efc757
ms.sourcegitcommit: ee5d044db99e253c27816e0ea6bdeb9e39a2cf41
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/08/2018
---
# <a name="get-started-with-power-bi-report-server"></a>Ismerkedés a Power BI jelentéskészítő kiszolgálóval
A Power BI mobil és többoldalas jelentések létrehozása, telepítése és felügyelete a helyszínen a Power BI jelentéskészítő kiszolgáló által biztosított, használatra kész eszközökkel.

## <a name="create-deploy-and-manage-reports"></a>Jelentések létrehozása, üzembe helyezése és kezelése
A Power BI jelentéskészítő kiszolgáló olyan megoldás, amelyet az ügyfelek telepíthetnek a saját helyszíni környezetükben jelentések létrehozására, közzétételére és kezelésére, majd kézbesítésére az arra jogosult felhasználóknak más-más módon, attól függően, hogy webböngészőben, a mobil eszközén, vagy pedig egy e-mailben tekinti meg őket.

A Power BI jelentéskészítő kiszolgáló egy termékcsomagot kínál:

* Egy modern webportált, amely bármelyik korszerű böngészőben megtekinthető. A webportálon rendezheti és megjeleníti a jelentéseket és a KPI-ket. A portálon Excel-munkafüzeteket is tárolhat.
* A Power BI Desktoppal létrehozott Power BI-jelentéseket a saját környezetben, a webes portálon belül tudja megtekinteni.
* Többoldalas, modern megjelenésű jelentéseket hozhat létre a rendelkezésére bocsátott eszközökkel.
* A rugalmas elrendezésű mobil jelentések alkalmazkodnak a különböző eszközökhöz és a különböző módokhoz, ahogyan tartja őket.

Ezekről külön-külön olvashat bővebben.

### <a name="whats-new-in-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgáló újdonságai
Ezek a források folyamatosan naprakészen tartják a Power BI jelentéskészítő kiszolgáló új funkcióit.

* [A Power BI jelentéskészítő kiszolgáló újdonságai](whats-new.md)
* [Microsoft Power BI-blog](https://powerbi.microsoft.com/blog/)
* [Az SQL Server Reporting Services csapat blogja](https://blogs.msdn.microsoft.com/sqlrsteamblog/)
* A [Guy in a Cube YouTube-csatorna](https://aka.ms/guyinacube)

## <a name="web-portal"></a>Webportál
![](media/get-started/web-portal.png)

A Power BI jelentéskészítő kiszolgáló végfelhasználói számára a bejárati ajtó a modern böngészőkben megtekinthető modern webes portál. A jelentések és a KPI-k az új portálon keresztül elérhetők.

Alkalmazhatja saját egyéni [védjegyzését](https://docs.microsoft.com/sql/reporting-services/branding-the-web-portal) a webes portálra. A webes portálon közvetlenül is létrehozhatja a KPI-ket. A KPI-kkel a böngészőben egy pillantással áttekintheti a fő üzleti mérőszámokat jelentés megnyitása nélkül.

A webportál tartalmát típus szerint szervezzük: Power BI-jelentések, mobiljelentések, többoldalas jelentések és KPI-k, valamint Excel-munkafüzetek, megosztott adathalmazok és megosztott adatforrások, amelyek a jelentések építőelemeként használhatók. Itt biztonságosan tárolhatja és kezelheti őket a hagyományos mappahierarchiában. Megjelölheti kedvenceit, és kezelheti a tartalmat, ha rendelkezik ezzel a szerepkörrel.

Továbbá ütemezheti a jelentésfeldolgozást, igény szerint érheti el a jelentéseket, és előfizethet a közzétett jelentésekre az új webes portálon.

További részletek a [webportálról](https://docs.microsoft.com/sql/reporting-services/web-portal-ssrs-native-mode).

## <a name="power-bi-reports"></a>Power BI-jelentések
![](media/get-started/powerbi-reports.png)

A Power BI-jelentések az adatkészletek többszempontú nézetei, amelyek az adatkészletből származó különféle eredményeket és elemzéseket bemutató vizualizációkat tartalmaznak.  Egy jelentés lehet egyetlen képi vizualizáció vagy vizualizációkkal megtöltött oldalak. Feladatkörétől függően Ön lehet jelentéskészítő és/vagy egy azokat feldolgozó vagy felhasználó személy.

A jelentések egyetlen adathalmazon alapulnak. A jelentésben lévő vizualizációk egy-egy információmorzsát képviselnek. A vizualizációk nem statikusak: hozzáadhat és eltávolíthat adatokat, módosíthatja a vizualizációtípusokat, és az elemzésekhez és a válaszok kereséséhez az adatok mélyebb szintjére lehatolva szűrőket és szeletelőket alkalmazhat. A jelentések rendkívül interaktívak és nagymértékben testre szabhatók – akárcsak az irányítópultok, de még jobban – és a vizualizációk az alapjukul szolgáló adatok változásával frissülnek.

## <a name="paginated-reports"></a>Többoldalas jelentések
![](media/get-started/paginated-reports.png)

A többoldalas jelentések többlapos dokumentum stílusú jelentések, amelyekben minél több adat van, annál több sor lesz a táblákban és annál több oldala lesz a jelentésnek. Tökéletesek a nyomtatásra optimalizált, rögzített elrendezésű, képpontról képpontra egyező, például PDF- és Word-dokumentumok létrehozásához.

Az [SQL Server Data Tools (SSDT)](https://docs.microsoft.com/sql/reporting-services/tools/reporting-services-in-sql-server-data-tools-ssdt) eszközkészlet által tartalmazott Jelentéstervező vagy a [Jelentéskészítő](https://docs.microsoft.com/sql/reporting-services/report-builder/report-builder-in-sql-server-2016) használatával modern megjelenésű jelentéseket hozhat létre.

## <a name="report-server-programming-features"></a>A Jelentéskészítő kiszolgáló programozási szolgáltatásai
Bővítheti és testre szabhatja a jelentéskészítési funkciókat a Power BI Jelentéskészítő kiszolgáló programozási szolgáltatásaival, API-kkal integrálhatja vagy terjesztheti ki az adatokat és a jelentésfeldolgozást egyéni alkalmazásokban.

További [fejlesztői dokumentáció a Jelentéskészítő kiszolgálóhoz](https://docs.microsoft.com/sql/reporting-services/reporting-services-developer-documentation).

## <a name="next-steps"></a>Következő lépések
[Felhasználói kézikönyv](user-handbook-overview.md)  
[Rendszergazdai kézikönyv](admin-handbook-overview.md)  
[Rövid útmutató: A Power BI jelentéskészítő kiszolgáló telepítése](quickstart-install-report-server.md)  
[A Jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)


