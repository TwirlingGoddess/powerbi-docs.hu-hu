---
title: A Power BI jelentéskészítő kiszolgáló újdonságai
description: A Power BI jelentéskészítő kiszolgáló újdonságainak bemutatása. A cikk a főbb funkciókat ismerteti és az új elemek kibocsátásakor frissül.
services: powerbi
documentationcenter: ''
author: maggiesMSFT
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
ms.date: 03/19/2018
ms.author: maggies
ms.openlocfilehash: 4f149baccf551762589c17bd6d6ba17c36f4da37
ms.sourcegitcommit: 0473a155495a7a9ba4b899d0815100426718b7ac
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/20/2018
---
# <a name="whats-new-in-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgáló újdonságai
A Power BI jelentéskészítő kiszolgáló újdonságainak bemutatása. A cikk a főbb funkciókat ismerteti és az új elemek kibocsátásakor frissül.

A Power BI jelentéskészítő kiszolgáló, illetve a Power BI jelentéskészítő kiszolgálóra optimalizált Power BI Desktop letöltéséhez nyissa meg az [On-premises reporting with Power BI Report Server](https://powerbi.microsoft.com/report-server/) (Helyi jelentéskészítés Power BI jelentéskészítő kiszolgálóval) webhelyet.

Az újdonságokra vonatkozó kapcsolódó információk:

* [A Power BI szolgáltatás újdonságai](../service-whats-new.md)
* [A Power BI Desktop újdonságai](../desktop-latest-update.md)
* [A Power BI-mobilalkalmazások újdonságai](../mobile-whats-new-in-the-mobile-apps.md)
* [A Power BI csapat blogja](https://powerbi.microsoft.com/blog/)

## <a name="march-2018-release"></a>2018. márciusi kiadás

A Power BI Desktop alkalmazás Power BI jelentéskészítő kiszolgálóhoz optimalizált verziója nagyszámú új szolgáltatással bővült a 2018. márciusi kiadásban. Az új szolgáltatások, területekre osztva: 
- [Vizualizációk](#visuals-updates)
- [Jelentéskészítés](#reporting)
- [Elemzés](#analytics)
- [Teljesítmény](#performance)
- [Jelentéskészítő kiszolgáló](#report-server)
- [Továbbiak](#other-improvements)

### <a name="highlights-of-this-release"></a>Legfontosabb változások

Az új szolgáltatások hosszú listájából az alábbiak különösen lényegesek.

#### <a name="rule-based-conditional-formatting-for-table-and-matrixhttpspowerbimicrosoftcomblogpower-bi-desktop-november-2017-feature-summaryconditionalformatting"></a>[Szabályalapú feltételes formázás táblához és mátrixhoz](https://powerbi.microsoft.com/blog/power-bi-desktop-november-2017-feature-summary/#conditionalFormatting)
 
Táblán vagy mátrixon alapuló egyéni üzleti logika segítségével szabályokat hozhat létre, melyekkel feltételesen formázhatja az oszlopok háttérszínét és betűszínét.

#### <a name="show-and-hide-pageshttpspowerbimicrosoftcomblogpower-bi-desktop-january-2018-feature-summaryhidepages"></a>[Oldalak megjelenítése és elrejtése](https://powerbi.microsoft.com/blog/power-bi-desktop-january-2018-feature-summary/#hidePages)

Előfordulhat, hogy a jelentését mások számára is elérhetővé szeretné tenni, de egyes oldalak még nem készültek el teljesen. Mostantól elrejtheti őket, amíg el nem készülnek. Vagy másik lehetőségként elrejtheti az oldalakat a normál navigációból, hogy az olvasók továbbra is elérhessék őket könyvjelzők vagy részletezés segítségével.

#### <a name="bookmarkinghttpspowerbimicrosoftcomblogpower-bi-desktop-march-2018-feature-summarybookmarking"></a>[Könyvjelzőkezelés](https://powerbi.microsoft.com/blog/power-bi-desktop-march-2018-feature-summary/#bookmarking)

Könyvjelzők létrehozásával mostantól egyéni információkat állíthat össze a jelentésében lévő adatokból.

- [Keresztkiemelés könyvjelzőkhöz:](https://powerbi.microsoft.com/blog/power-bi-desktop-december-feature-summary/#bookmarkCrossHighlighting) A könyvjelzők fenntartják és megjelenítik a jelentésoldalak keresztkiemelt állapotát a könyvjelző létrehozásakor aktuális állapot szerint.
- [További lehetőségek könyvjelzőkkel:](https://powerbi.microsoft.com/blog/power-bi-desktop-december-feature-summary/#bookmarkFlexibility) A könyvjelzők tükrözik a jelentésben beállított tulajdonságokat, és csak a választott vizualizációkra vannak hatással.

#### <a name="multi-select-data-points-across-multiple-chartshttpspowerbimicrosoftcomblogpower-bi-desktop-february-2018-feature-summarycrosshighlight"></a>[Többszörös kiválasztású adatpontok több diagramra](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#crosshighlight)

Több adatpontot is kiválaszthat több diagramon, és a teljes oldalra alkalmazhat keresztszűrést.

#### <a name="sync-slicers-across-multiple-pages-of-your-reporthttpspowerbimicrosoftcomblogpower-bi-desktop-february-2018-feature-summarysyncslicers"></a>[Szeletelők szinkronizálása több jelentésoldalon](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#syncSlicers)

A szeletelők alkalmazhatók egy, kettő vagy több oldalra is a jelentésben.

#### <a name="quick-measureshttpspowerbimicrosoftcomblogpower-bi-desktop-february-2018-feature-summaryquickmeasures"></a>[Gyorsmérők](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#quickMeasures) 

Létrehozhat mértékeket meglévő mértékek és táblabeli numerikus oszlopok alapján.

#### <a name="drilling-down-filters-other-visualshttpspowerbimicrosoftcomblogpower-bi-desktop-december-feature-summarydrillfiltersothervisuals"></a>[Más vizualizációk szűrése részletezéskor](https://powerbi.microsoft.com/blog/power-bi-desktop-december-feature-summary/#drillFiltersOtherVisuals)

Amikor részletezi egy vizualizáció egy kategóriáját, mostantól az adott oldal összes vizualizációját szűrheti ugyanazon kategória alapján.

### <a name="visuals-updates"></a>Vizualizációk frissítései

- [Cellaigazítás táblához és mátrixhoz](https://powerbi.microsoft.com/blog/power-bi-desktop-november-2017-feature-summary/#alignment)
- [Megjelenítési egységek és precíziós vezérlők a tábla- és mátrixoszlopokhoz](https://powerbi.microsoft.com/blog/power-bi-desktop-march-2018-feature-summary/#displayUnits)
- [Adatcímkék túlcsordulása sáv- és oszlopdiagramot tartalmazó vizualizációknál](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#overflow)
- [A Descartes-féle és térképes vizualizációk adatcímkéi háttérszínének vezérlése](https://powerbi.microsoft.com/blog/power-bi-desktop-january-2018-feature-summary/#dataLabelBackground)
- [Sáv- és oszlopdiagram kitöltésének vezérlése](https://powerbi.microsoft.com/blog/power-bi-desktop-january-2018-feature-summary/#padding)
- [Diagramokon belüli tengelycímkék területének növelése](https://powerbi.microsoft.com/blog/power-bi-desktop-january-2018-feature-summary/#axisSize)
- [Pontvizualizáció az X és az Y tengely szerinti csoportosítással](https://powerbi.microsoft.com/blog/power-bi-desktop-december-feature-summary/#scatterChart)
- [Nagy sűrűségű mintavétel szélességen és hosszúságon alapuló térképekhez](https://powerbi.microsoft.com/blog/power-bi-desktop-december-feature-summary/#highDensityMaps)
- [Rugalmas szeletelők](https://powerbi.microsoft.com/blog/power-bi-desktop-december-feature-summary/#responsive)
- [Relatív dátumszeletelő rögzített kezdőidejének hozzáadása](https://powerbi.microsoft.com/blog/power-bi-desktop-january-2018-feature-summary/#anchorDate)

### <a name="reporting"></a>Jelentéskészítés

- [Vizualizációs fejléc kikapcsolása jelentések olvasási nézetében](https://powerbi.microsoft.com/blog/power-bi-desktop-march-2018-feature-summary/#visualHeader)
- [Jelentési lehetőségek lassú adatforrásokhoz](https://powerbi.microsoft.com/blog/power-bi-desktop-november-2017-feature-summary/#slowDataSource)
- [Vizualizációk alapértelmezett elhelyezésének javítása](https://powerbi.microsoft.com/blog/power-bi-desktop-march-2018-feature-summary/#visualPlacement)
- [A vizualizációk rendezésének vezérlése a kijelöléspanelen keresztül](https://powerbi.microsoft.com/blog/power-bi-desktop-november-2017-feature-summary/#selectionPane)
- [Objektumok zárolása a jelentésben](https://powerbi.microsoft.com/blog/power-bi-desktop-november-2017-feature-summary/#lock)
- [Keresés a Formázás és Elemzés panelen](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#search)
- [Mezőtulajdonságok panelje és mezőleírások](https://powerbi.microsoft.com/blog/power-bi-desktop-december-feature-summary/#fieldPropertiesPane)

### <a name="analytics"></a>Elemzés

- [UTCNOW() és UTCTODAY()](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#utcDAX)
- [Egyéni dátumtábla megjelölése](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#customDateTable)
- [Más vizualizációk szűrése részletezéskor](https://powerbi.microsoft.com/blog/power-bi-desktop-december-feature-summary/#drillFiltersOtherVisuals)
- [Cellaszintű formázás többsoros kártyákhoz készült többdimenziós AS-modellekhez](https://powerbi.microsoft.com/blog/power-bi-desktop-november-2017-feature-summary/#cellLevelFormatting)
 
### <a name="performance"></a>Teljesítmény

- [Javított szűrési teljesítmény](https://powerbi.microsoft.com/blog/power-bi-desktop-november-2017-feature-summary/#filtering)
- [Javított DirectQuery-teljesítmény](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#dqPerf)
- [Javított megnyitási és mentési teljesítmény](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#savePerf)
- [Továbbfejlesztett „Adatot nem tartalmazó elemek megjelenítése” funkció](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#showItemsWithNoData)
 
### <a name="report-server"></a>Jelentéskészítő kiszolgáló 

#### <a name="export-to-accessible-pdf"></a>Exportálás akadálymentes PDF-fájlba

Mostantól a többoldalas (RDL) jelentéseket akadálymentes/címkézett PDF-fájlba is exportálhatja. Ezeknek a fájloknak a mérete nagyobb, de a képernyőolvasók és más kisegítő technológiák könnyebben tudják olvasni a tartalmukat, illetve könnyebben tudnak navigálni a fájlban. Az akadálymentes PDF-eket az **AccessiblePDF** eszközinformációs beállítás **Igaz** értékre állításával engedélyezheti. Lásd: [PDF-fájlok eszközinformációs beállításai](https://docs.microsoft.com/sql/reporting-services/pdf-device-information-settings) és [Eszközinformációs beállítások módosítása](https://docs.microsoft.com/sql/reporting-services/customize-rendering-extension-parameters-in-rsreportserver-config#changing-device-information-settings).


### <a name="other-improvements"></a>Egyéb fejlesztések

- [Továbbfejlesztett „Oszlop felvétele példákból” funkció](https://powerbi.microsoft.com/blog/power-bi-desktop-november-2017-feature-summary/#addColumnFromExamples)
- [Tanácsadási szolgáltatások gyorshivatkozása](https://powerbi.microsoft.com/blog/power-bi-desktop-february-2018-feature-summary/#consultingServices)
- [Továbbfejlesztett hibajelentés](https://powerbi.microsoft.com/blog/power-bi-desktop-march-2018-feature-summary/#errors)
- [Korábban észlelt hibák megtekintése](https://powerbi.microsoft.com/blog/power-bi-desktop-march-2018-feature-summary/#viewErrors)

 
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

## <a name="next-steps"></a>Következő lépések
[Felhasználói kézikönyv](user-handbook-overview.md)  
[Rendszergazdai kézikönyv](admin-handbook-overview.md)  
[Rövid útmutató: A Power BI jelentéskészítő kiszolgáló telepítése](quickstart-install-report-server.md)  
[A Jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

