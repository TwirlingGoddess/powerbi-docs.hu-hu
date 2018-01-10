---
title: "A Power BI jelentéskészítő kiszolgáló újdonságai"
description: "A Power BI jelentéskészítő kiszolgáló újdonságainak bemutatása. A cikk a főbb funkciókat ismerteti és az új elemek kibocsátásakor frissül."
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 10/31/2017
ms.author: maghan
ms.openlocfilehash: 433581f77cfeaa002cffeecd927ba8751fc46617
ms.sourcegitcommit: eec6b47970bf69ed30638d1a20051f961ba792f2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/06/2018
---
# <a name="whats-new-in-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgáló újdonságai
A Power BI jelentéskészítő kiszolgáló újdonságainak bemutatása. A cikk a főbb funkciókat ismerteti és az új elemek kibocsátásakor frissül.

A Power BI jelentéskészítő kiszolgáló és a hozzá optimalizált Power BI Desktop letöltéséhez keresse fel a [Helyszíni jelentéskészítés a Power BI jelentéskészítő kiszolgálóval](https://powerbi.microsoft.com/report-server/) című oldalt.

![Tipp](media/whats-new/fyi-tip.png "tipp") Az aktuális kibocsátási megjegyzések a [Power BI jelentéskészítő kiszolgáló – Kibocsátási megjegyzések](release-notes.md) oldalon olvashatók.

Kapcsolódó "Újdonságok" az alábbi helyeken találhatók:

* [A Power BI szolgáltatás újdonságai](../service-whats-new.md)
* [A Power BI Desktop újdonságai](../desktop-latest-update.md)
* [A Power BI-mobilalkalmazások újdonságai](../mobile-whats-new-in-the-mobile-apps.md)
* [A Power BI csapat blogja](https://powerbi.microsoft.com/blog/)

## <a name="october-2017-release"></a>2017. októberi kiadás
### <a name="power-bi-report-data-sources"></a>Adatforrások a Power BI-jelentésekhez
Power BI jelentéskészítő kiszolgáló Power BI-jelentései többféle adatforráshoz kapcsolódhatnak. Importálhatja az adatokat és ütemezheti a frissítésüket, vagy lekérdezheti őket közvetlenül a DirectQuery vagy az SQL Server Analysis Services élő kapcsolata használatával. Az ütemezett frissítést és a DirectQuery-t támogató adatforrások listáját a "Adatforrások Power BI-jelentésekhez a Power BI jelentéskészítő kiszolgálóban" című cikk tartalmazza.

### <a name="scheduled-data-refresh-for-imported-data"></a>Importált adatok ütemezett frissítése
A Power BI jelentéskészítő kiszolgálóval ütemezett adatfrissítést állíthat be, hogy élő kapcsolat vagy a DirectQuery helyett beágyazott modellel tartsa naprakészen a Power BI-jelentések adatait. A beágyazott modellben az adatokat importálja, így azok elkülönülnek az eredeti adatforrástól. Az adatok naprakészen tartásához frissíteni kell, erről pedig az ütemezett frissítés gondoskodik. További információ: "Power BI jelentéskészítő kiszolgáló Power BI-jelentéseinek ütemezett frissítése".

### <a name="editing-power-bi-reports-from-the-server"></a>Power BI-jelentések szerkesztése a kiszolgálóról
A Power BI-jelentésfájlokat (.pbix) a kiszolgálóról is megnyithatja és szerkesztheti, de az eredetileg feltöltött fájlt kapja vissza.  Emiatt **ha a kiszolgáló frissítette az adatokat, akkor azok nem frissülnek a fájl első megnyitásakor**. Helyileg, manuálisan kell frissítenie őket, hogy lássa a változást.

### <a name="large-file-uploaddownload"></a>Nagy méretű fájlok feltöltése/letöltése
Legfeljebb 2 GB méretű fájlok tölthetők fel, bár ez a korlát alapértelmezés szerint 1 GB-ra van beállítva a jelentéskészítő kiszolgáló SQL Server Management Studio-beli (SSMS) beállításaiban.  Ezek a fájlok az adatbázisban vannak tárolva, ahogyan a SharePoint esetében, és nem igényelnek különleges konfigurációt az SQL Server-katalógusban.  

### <a name="accessing-shared-datasets-as-odata-feeds"></a>Megosztott adatkészletek elérése OData-csatornákként
A megosztott adatkészletek a Power BI Desktopból OData-csatorna használatával érhetők el. További információ: [Megosztott adatkészletek elérése OData-csatornákként a Power BI jelentéskészítő kiszolgálóban](access-dataset-odata.md).

### <a name="scale-out"></a>Bővítés
Ez a kiadás támogatja a bővítést. A legjobb eredmény érdekében használjon terheléselosztót, és állítsa be a kiszolgálóaffinitást. Ne feledje, hogy a rendszer ekkor még nincs bővítésre optimalizálva, így esetleg több csomópont között replikált modelleket fog látni. Ez az összeállítás a hálózati terheléselosztó és rögzített munkamenetek nélkül is működik. Az N példányban betöltődő modell azonban nem csupán túlzott memóriahasználatot eredményez, de a kapcsolatok közötti átvitel is lassul a kérelmek között új csomópontot elérő modell átvitele miatt.  

### <a name="administrator-settings"></a>Rendszergazdai beállítások
A rendszergazdák a következő tulajdonságokat állíthatják be az SSMS-ben a kiszolgálófarm speciális tulajdonságai között:

* EnableCustomVisuals (Egyéni megjelenítések engedélyezése): True/False (Igaz/Hamis)
* EnablePowerBIReportEmbeddedModels (Power BI-jelentés beágyazott modellek engedélyezése): True/False (Igaz/Hamis)
* EnablePowerBIReportExportData (Power BI-jelentés adatexportálás engedélyezése): True/False (Igaz/Hamis)
* MaxFileSizeMb (Maximális fájlméret MB-ban): Alapértelmezett értéke jelenleg 1000
* ModelCleanupCycleMinutes (Modellek törlési ciklusa percekben): Milyen gyakran ellenőrzi a memóriából kizárandó modelleket
* ModelExpirationMinutes (Modellek lejárati ideje percekben): Mennyi idő után jár le és záródik ki a modell az utolsó használat időpontja után
* ScheduleRefreshTimeoutMinutes (Ütemezett frissítés időtúllépése percekben): Mennyi ideig tarthat egy modell adatfrissítése. Az alapértelmezett korlát két óra.  Nincs merev felső korlát.

**Az rsreportserver.config konfigurációs fájl**

```
<Configuration>
  <Service>
    <PollingInterval>10</PollingInterval>
    <IsDataModelRefreshService>false</IsDataModelRefreshService>
    <MaxQueueThreads>0</MaxQueueThreads>
  </Service>
</Configuration>
```

### <a name="developer-api"></a>Fejlesztői API
Az SSRS 2017-hez bevezetett fejlesztői API (REST API) kibővült az Excel- és .pbix-fájloknak a Power BI jelentéskészítő kiszolgálóval való használatával. Egy lehetséges felhasználási mód fájlok program alapján történő letöltése a kiszolgálóról, frissítése majd újbóli közzététele. PowerPivot modelleket tartalmazó Excel-munkafüzetek például csak ezen a módon frissíthetők.

Érdemes tudni, hogy létezik egy új, külön API a nagyméretű fájlokhoz, amelyek a Swaggernek a Power BI jelentéskészítő kiszolgálóhoz készült verziójával frissülnek. 

### <a name="sql-server-analysis-services-ssas-and-the-power-bi-report-server-memory-footprint"></a>Az SQL Server Analysis Services (SSAS) és a Power BI jelentéskészítő kiszolgáló memóriaigénye
A Power BI jelentéskészítő kiszolgáló már belsőleg üzemelteti az SQL Server Analysis Services szolgáltatást. Ez nem csak az ütemezett frissítésre vonatkozik. Az SSAS fenntartása nagy mértékben megnöveli a jelentéskészítő kiszolgáló memóriaigényét. Az AS.ini konfigurációs fájl megtalálható a kiszolgáló-csomópontokon, így ha jártas az SSAS használatában, módosíthatja a beállításokat, köztük a maximális memóriahasználatot és a lemezek gyorsítótárazását. További részletek: [Kiszolgálótulajdonságok az Analysis Services szolgáltatásban](https://docs.microsoft.com/sql/analysis-services/server-properties/server-properties-in-analysis-services).

### <a name="viewing-and-interacting-with-excel-workbooks"></a>Excel-munkafüzetek megtekintése és kezelése
Az Excel és a Power BI az iparágban egyedülálló eszköz-portfóliót tartalmaz. Együttesen egyszerűbbé teszik az üzleti elemzők számára az adatok gyűjtését, formálását, elemezését és vizuális felfedezését. A Power BI-jelentéseknek a webes portálon való megtekintésén kívül az üzleti felhasználók ugyanezt már Excel-munkafüzetekkel is megtehetik a Power BI jelentéskészítő kiszolgálón, így egy helyen tehetik közzé és tekinthetik meg önkiszolgáló Microsoft BI-tartalmaikat.

A Microsoft közzétett egy [útmutató Office Online Server (OOS) Power BI jelentéskészítő kiszolgáló előzetes környezetéhez való hozzáadásához](excel-oos.md) című cikket. A mennyiségi licenc fiókkal rendelkező ügyfelek költség nélkül tölthetik le az OOS-t a Volume License Servicing Centerből, és csak megtekintési funkciókhoz férnek hozzá. Konfigurálás után a felhasználók a következő követelményeknek megfelelő Excel-munkafüzeteket tekinthetnek meg és kezelhetnek:

* Nem függenek külső adatforrástól
* Élő kapcsolatuk van egy külső SQL Server Analysis Services-adatforrással
* PowerPivot-adatmodellel rendelkeznek

### <a name="support-for-new-table-and-matrix-visuals"></a>Támogatják az új táblázat és mátrix vizualizációkat
A Power BI jelentéskészítő kiszolgáló már támogatja a Power BI új táblázat és mátrix vizualizációit. Az ezeket a vizualizációkat tartalmazó jelentések készítéséhez a 2017. októberi kiadásra frissített Power BI Desktop szükséges. Az új verzió nem telepíthető a Power BI Desktop (2017. június) kiadása mellé. A Power BI Desktop legújabb verziója a [Power BI jelentéskészítő kiszolgáló letöltési oldal](https://powerbi.microsoft.com/report-server/) **Speciális letöltési beállítások** eleme alatt található.

## <a name="june-2017"></a>2017. június
* Általánosan elérhető (GA) a Power BI jelentéskészítő kiszolgáló.

## <a name="may-2017"></a>2017. május
* Elérhető a Power BI jelentéskészítő kiszolgáló előzetes verziója
* Power BI-jelentések helyszíni közzétételének lehetősége
  * Egyéni vizualizációk támogatása
  * Élő Analysis Services kapcsolat támogatása, de további adatforrások később várhatók
  * A Power BI mobilalkalmazás frissítése a Power BI jelentéskészítő kiszolgálón tárolt Power BI-jelentések megjelenítéséhez
* Továbbfejlesztett együttműködés megjegyzéseket tartalmazó jelentésekben

## <a name="next-steps"></a>További lépések
[Power BI jelentéskészítő kiszolgáló kibocsátási megjegyzések](release-notes.md)  
[Felhasználói kézikönyv](user-handbook-overview.md)  
[Rendszergazdai kézikönyv](admin-handbook-overview.md)  
[Rövid útmutató: A Power BI jelentéskészítő kiszolgáló telepítése](quickstart-install-report-server.md)  
[A Jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

