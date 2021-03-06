---
title: Power BI felügyeleti portál
description: A felügyeleti portál a Power BI bérlői felügyeletét teszi lehetővé a munkahelyen. Olyan lehetőségeket kínál, mint például a használati metrikák, hozzáférés az Office 365 felügyeleti központjához, valamint a beállítások.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 06/28/2017
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: 2f10ead5d08efa12cae05aeb6f2e3d3068636f77
ms.sourcegitcommit: a3ce866caba24217bcdd011e892b9ea72f3d2400
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/18/2018
ms.locfileid: "49396911"
---
# <a name="power-bi-admin-portal"></a>Power BI felügyeleti portál

A felügyeleti portál a Power BI bérlői felügyeletét teszi lehetővé a munkahelyen. Olyan lehetőségeket kínál, mint például a használati metrikák, hozzáférés az Office 365 felügyeleti központjához, valamint a beállítások.

A cégnél a Power BI bérlői felügyelete a Power BI felügyeleti portálján keresztül történik. A felügyeleti portálhoz az Office 365 minden globális rendszergazdája hozzáférhet, valamint olyan felhasználók is, akik Power BI-szolgáltatásadminisztrátori szerepkört kaptak. A Power BI szolgáltatás rendszergazdai szerepkörére vonatkozó további információkat [a Power BI rendszergazdai szerepkörét ismertető](service-admin-role.md) témakör tartalmaz.

Az összes felhasználó láthatja a **Felügyeleti portál** menüpontot a fogaskerék ikonja alatt. Ha nem rendszergazdáról van szó, a felhasználó csak a **Premium-beállítások** szakaszt látja, és csak azok a kapacitások jelennek meg, amelyek felügyeletéhez a felhasználó jogosultsággal rendelkezik.

## <a name="how-to-get-to-the-admin-portal"></a>A felügyeleti portál elérése

A Power BI felügyeleti portál eléréséhez az adott fiókot **globális rendszergazdaként** kell megjelölni az Office 365-ben vagy az Azure Active Directoryban, vagy Power BI-szolgáltatásadminisztrátori szerepkört kell hozzárendelni. További információ a Power BI-szolgáltatásadminisztrátori szerepkörről: [A Power BI rendszergazdai szerepkörének ismertetése](service-admin-role.md). A Power BI felügyeleti portál eléréséhez tegye az alábbiakat.

1. Válassza ki a Beállítások fogaskereket a Power BI szolgáltatás jobb felső sarkában.
2. Válassza a **Felügyeleti portál** lehetőséget.

![](media/service-admin-portal/powerbi-admin-settings.png)

A portálon hat lap található. Ezek leírását az alábbiakban láthatja.

* [Használati metrikák](#usage-metrics)
* [Felhasználók](#users)
* [Auditnaplók](#audit-logs)
* [Bérlői beállítások](#tenant-settings)
* [Premium-beállítások](#premium-settings)
* [Beágyazási kódok](#embed-codes)
* [Szervezeti vizualizációk](#Organization-visuals)

![](media/service-admin-portal/powerbi-admin-landing-page.png)

## <a name="usage-metrics"></a>Használati metrikák
A felügyeleti portál első lapja a **Használati metrikák**. A használati metrikákat tartalmazó jelentés a Power BI-beli használat monitorozását teszi lehetővé a munkahelyen. Ezenkívül azt is mutatja, hogy mely munkahelyi felhasználók és csoportok a legaktívabbak a Power BI-ban.

> [!NOTE]
> Az irányítópult első használatakor, vagy ha hosszú idő elteltével keresi fel újra az irányítópultot, egy betöltési képernyő jelenik meg az irányítópult betöltése során.

Miután az irányítópult betöltődött, két szakaszba sorolt csempék jelennek meg. Az első szakasz tartalmazza az egyes felhasználók használati adatait, míg a második szakaszban a munkahelyi csoportok hasonló információi láthatók.

Az alábbiakban az egyes csempéknél megjelenő részletes információkat ismertetjük:

* A felhasználói munkaterület összes irányítópultjának, jelentésének és adatkészletének eltérő darabszáma
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-number-tiles.png)

* A legtöbbet használt irányítópult az ahhoz hozzáférő felhasználók száma szerint. Például ha 3 felhasználóval oszt meg egy irányítópultot, és olyan tartalomcsomaghoz is hozzáadja azt, amelyhez két különböző felhasználó kapcsolódik, a számláló értéke 6 (1 + 3 + 2)
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-top-dashboards.png)

* A legnépszerűbb tartalom, amelyhez a felhasználók kapcsolódtak. Ez bármi lehet, amelyhez a felhasználók hozzáférhetnek az adatbeolvasási folyamaton keresztül, például szolgáltatott szoftveres tartalomcsomagok, munkahelyi tartalomcsomagok, fájlok vagy adatbázisok.
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-top-connections.png)

* A legaktívabb felhasználókat mutatja az irányítópultok száma alapján, beleértve a felhasználók által létrehozott és a velük megosztott irányítópultok számát.
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-top-users-dashboards.png)

* A legaktívabb felhasználókat mutatja a jelentések száma alapján
  
    ![](media/service-admin-portal/powerbi-admin-usage-metrics-top-users-reports.png)

A második szakasz ugyanezeket az információkat tartalmazza – a csoportok alapján. Lehetővé teszi annak megtekintését, hogy a munkahely mely csoportjai a legaktívabbak, és milyen típusú információkat használnak.

Ezek az információk valós betekintést nyújtanak abba, hogy a felhasználók miként használják a Power BI-t a munkahelyen, és mely munkahelyi felhasználók és csoportok számítanak különösen aktívnak.

## <a name="users"></a>Felhasználók

A felügyeleti portál második lapja a **Felhasználók kezelése**. A Power BI-beli felhasználók kezelése az Office 365 felügyeleti központjában történik. Ebből a szakaszból gyorsan elérhető a felhasználók, a rendszergazdák és a csoportok kezelésére szolgáló Office 365-beli terület.

![](media/service-admin-portal/powerbi-admin-manage-users.png)

Amikor rákattint az **Ugrás az O365 felügyeleti központjára** elemre, közvetlenül az Office 365 felügyeleti központjának kezdőlapjára kerül, ahol elvégezheti a bérlő felhasználóinak kezelését.

![](media/service-admin-portal/powerbi-admin-o365-admin-center.png)

## <a name="audit-logs"></a>Auditnaplók

A felügyeleti portál harmadik lapja az **Auditnaplók**. A naplók az Office 365 Biztonsági és megfelelőségi központjában találhatók. Ebben a szakaszban gyorsan hozzáférhet az Office 365-beli adott területhez.

Az auditnaplókkal kapcsolatos további információ: [A Power BI-naplózás használata a munkahelyen](service-admin-auditing.md)

## <a name="tenant-settings"></a>Bérlői beállítások

A felügyeleti portál negyedik lapja a **Bérlői beállítások**. A Bérlői beállítások használatával hatékonyabban lehet szabályozni, hogy mely funkciók legyenek elérhetők a munkahelyen. Ha aggályai vannak a bizalmas adatokkal kapcsolatban, a funkciók némelyike esetlegesen nem megfelelő a munkahely számára, vagy csak egy adott funkciót szeretne engedélyezni egy adott csoportnak. Ha ezekről van szó, kikapcsolhatja az adott funkciót a bérlőn.

![](media/service-admin-portal/powerbi-admin-tenant-settings.png)

> [!NOTE]
> A beállítás érvénybe léptetése a bérlő összes felhasználója számára akár 10 percet is igénybe vehet.

A beállítások állapota háromféle lehet:

* **Az egész munkahelyen sehol nem engedélyezett**: Letilthat egy funkciót, így a felhasználók nem fogják tudni használni azt.

    ![](media/service-admin-portal/powerbi-admin-tenant-settings-disabled.png)

* **Az egész munkahelyen mindenhol engedélyezett**: Engedélyezhet egy funkciót az egész munkahelyen, így ahhoz minden felhasználó hozzáférhet.

    ![](media/service-admin-portal/powerbi-admin-tenant-settings-enabled.png)

* **A munkahely egy alegységénél engedélyezett**: A funkciókat a munkahely egy adott alegységénél is engedélyezheti. Erre különböző módokon kerülhet sor. Engedélyezhet egy funkciót az egész munkahelyen a felhasználók egy adott csoportja kivételével.

    ![](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except.png)

    Engedélyezhet egy funkciót a felhasználók egy adott csoportjában, és letilthatja azt a felhasználók egy másik csoportjában. Így garantálható, hogy egyes felhasználók még akkor sem férhetnek hozzá az adott funkcióhoz, ha egyébként benne vannak az engedélyezett csoportban.

    ![](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except2.png)

A következő néhány bekezdés a bérlői beállítások különböző típusainak áttekintését nyújtja.

## <a name="workspace-settings"></a>Munkaterület beállításai

### <a name="create-workspaces-preview"></a>Munkaterületek létrehozása (előzetes verzió)
A vállalat felhasználói alkalmazás-munkaterületeket hozhatnak létre az irányítópultok, jelentések és egyéb tartalmak közös használatához.

További információk: [Új munkaterületek létrehozása](service-create-the-new-workspaces.md).

## <a name="export-and-sharing-settings"></a>Exportálási és megosztási beállítások

### <a name="share-content-to-external-users"></a>Tartalom megosztása külső felhasználókkal

A munkahelyi felhasználók külső felhasználókkal oszthatnak meg irányítópultokat.

![](media/service-admin-portal/powerbi-admin-sharing-external-02.png)

Ha külső felhasználóval oszt meg tartalmat, az alábbi üzenet jelenik meg.

![](media/service-admin-portal/powerbi-admin-sharing-external.png)

### <a name="publish-to-web"></a>Webes közzététel

A munkahelyi felhasználók a weben tehetnek közzé jelentéseket. [További információ](service-publish-to-web.md)

![](media/service-admin-portal/powerbi-admin-publish-to-web.png)

A webes közzététel beállításától függően a felhasználók különféle lehetőségeket láthatnak a felhasználói felületen.

|Funkció |A teljes cég számára engedélyezve |A teljes cég számára letiltva |Speciális biztonsági csoportok   |
|---------|---------|---------|---------|
|A **Webes közzététel** parancs egy jelentés **Fájl** menüjében.|Mindenki számára engedélyezve|Nem mindenki számára látható|Csak az arra jogosult felhasználók vagy csoportok láthatják.|
|A **Beágyazási kódok kezelése** funkció a **Beállítások** közt|Mindenki számára engedélyezve|Mindenki számára engedélyezve|Mindenki számára engedélyezve<br><br>* A **Törlés** parancsot csak az arra jogosult felhasználók vagy csoportok érik el.<br>* A **Kód lekérése** mindenki számára engedélyezve van.|
|**Beágyazási kódok** a felügyeleti portálon|Az állapot a következő értékek egyikét jeleníti meg:<br>* Aktív<br>* Nem támogatott<br>* Blokkolva|Állapotként a **Letiltva** jelenik meg|Az állapot a következő értékek egyikét jeleníti meg:<br>* Aktív<br>* Nem támogatott<br>* Blokkolva<br><br>Ha egy felhasználónak nincs megfelelő jogosultsága a bérlői beállítások alapján, akkor a **Megsértve** állapot jelenik meg.|
|Meglévő közzétett jelentések|Minden engedélyezve|Minden letiltva|A jelentések továbbra is megjelennek mindenki számára.|

### <a name="export-data"></a>Adatok exportálása

A munkahelyi felhasználók adatokat exportálhatnak egy csempéről vagy vizualizációból. [További információ](visuals/power-bi-visualization-export-data.md)

![](media/service-admin-portal/powerbi-admin-export-data.png)

> [!NOTE]
> Az **Adatok exportálása** lehetőség letiltásával azt is megakadályozhatja, hogy a felhasználók az **Elemzés az Excelben** funkciót vagy a Power BI szolgáltatás élő kapcsolatát használják.

### <a name="export-reports-as-powerpoint-presentations"></a>Jelentések exportálása PowerPoint-bemutatóként

A munkahelyi felhasználók PowerPoint-fájlként exportálhatják a Power BI-jelentéseket. [További információ](consumer/end-user-powerpoint.md)

![](media/service-admin-portal/powerbi-admin-powerpoint.png)

### <a name="print-dashboards-and-reports"></a>Irányítópultok és jelentések nyomtatása

A munkahelyi felhasználók irányítópultokat és jelentéseket nyomtathatnak. [További információ](consumer/end-user-print.md)

![](media/service-admin-portal/powerbi-admin-print-dashboard.png)

![](media/service-admin-portal/powerbi-admin-print-report.png)

## <a name="content-pack-settings"></a>Tartalomcsomag-beállítások

### <a name="publish-content-packs-to-the-entire-organization"></a>Tartalomcsomagok közzététele az egész munkahely számára

A munkahelyi felhasználók tartalomcsomagokat tehetnek közzé az egész munkahely számára.

![](media/service-admin-portal/powerbi-admin-publish-entire-org.png)

### <a name="create-template-organizational-content-packs"></a>Munkahelyi tartalomcsomagok sablonjainak létrehozása

A munkahelyi felhasználók tartalomcsomag-sablonokat készíthetnek, amelyek a Power BI Desktop adott adatforrására épülő adatkészleteket használják.

### <a name="push-apps-to-end-users"></a>Alkalmazások küldése a végfelhasználóknak

A bérlői rendszergazda a **Bérlői beállításokban** engedélyezheti az alkalmazások küldését.

   ![Alkalmazásleküldés engedélyezése](media/service-create-distribute-apps/power-bi-apps-pushapps01.png)

A beállítást **Engedélyezve** értékre állíthatja, és megadhatja, hogy ki használhatja ezt a funkciót (a teljes szervezet vagy adott biztonsági csoportok).

> [!NOTE]
> Ne feledje, hogy bérlői beállítások módosításának érvénybe lépése időbe telhet.

További információ az [alkalmazások leküldéséről](service-create-distribute-apps.md).

## <a name="integration-settings"></a>Integrálási beállítások

### <a name="ask-questions-about-data-using-cortana"></a>Adatokkal kapcsolatos kérdések feltevése Cortanával

A munkahelyi felhasználók Cortana használatával kérdéseket tehetnek fel az adataikról.

> [!NOTE]
> Ez a beállítás az egész munkahelyre vonatkozik, és nem lehet korlátozni meghatározott csoportokra.

### <a name="use-analyze-in-excel-with-on-premises-datasets"></a>Az Elemzés az Excelben helyszíni adatkészleteken való használata

A munkahelyi felhasználók az Excel használatával megtekinthetik és használhatják a helyszíni Power BI-adatkészleteket. [További információ](service-analyze-in-excel.md)

> [!NOTE]
> Az **Adatok exportálása** lehetőség letiltásával azt is megakadályozhatja, hogy a felhasználók az **Elemzés az Excelben** funkciót használják.

### <a name="use-arcgis-maps-for-power-bi"></a>Az ArcGIS Maps for Power BI használata

A vállalati felhasználók használhatják az Esri által biztosított ArcGIS Maps for Power BI vizualizációt. [További információ](power-bi-visualization-arcgis.md)

### <a name="use-global-search-for-power-bi-preview"></a>A globális keresés használata a Power BI-ban (előzetes verzió)

A vállalati felhasználók használhatják az Azure Searchre épülő külső keresési funkciókat. Például a felhasználók a Cortana használatával a lényeges információkat közvetlenül a Power BI-irányítópultokból és -jelentésekből nyerhetik ki. [További információ](service-cortana-intro.md)

## <a name="custom-visuals-settings"></a>Egyéni vizualizációk beállításai

### <a name="enable-custom-visuals-for-the-entire-organization"></a>Egyéni vizualizációk engedélyezése a teljes cég számára

A munkahelyi felhasználók egyéni vizualizációkat használhatnak és oszthatnak meg. [További információ](power-bi-custom-visuals.md)

> [!NOTE]
> Ez a beállítás az egész munkahelyre vonatkozik, és nem lehet korlátozni meghatározott csoportokra.

## <a name="r-visuals-settings"></a>R-vizualizációk beállításai

### <a name="interact-with-and-share-r-visuals"></a>R-vizualizációk kezelése és megosztása

A munkahelyi felhasználók R-szkriptekkel készült vizualizációkat használhatnak és oszthatnak meg. [További információ](visuals/service-r-visuals.md)

> [!NOTE]
> Ez a beállítás az egész munkahelyre vonatkozik, és nem lehet korlátozni meghatározott csoportokra.

## <a name="audit-and-usage-settings"></a>Naplózási és használati beállítások

### <a name="create-audit-logs-for-internal-activity-auditing-and-compliance"></a>Auditnaplók létrehozása a belső tevékenységek vizsgálatához és a megfelelőség biztosításához

A felhasználók a naplózással nyomon követhetik, hogy a munkahely más felhasználói milyen műveleteket hajtottak végre a Power BI-ban. [További információ](service-admin-auditing.md)

Az auditnapló bejegyzéseinek rögzítéséhez ezt a beállítást kell bekapcsolni. Akár 48 órás késés is lehet a naplózás engedélyezése és a naplózási adatok megtekinthetővé válása között. Ha nem látja azonnal adatokat, ellenőrizze később az auditnaplókat. Hasonló késés lehet az auditnaplók megtekintési engedélyének megkapása és a naplók elérésének lehetővé válása között.

> [!NOTE]
> Ez a beállítás az egész munkahelyre vonatkozik, és nem lehet korlátozni meghatározott csoportokra.

### <a name="usage-metrics-for-content-creators"></a>Használati metrikák tartalomkészítők számára
A szervezet felhasználói láthatják az általuk létrehozott jelentések és irányítópultok metrikáit. [További információ](service-usage-metrics.md).

A beállítást **Engedélyezve** értékre állíthatja, és megadhatja, hogy ki láthat használati metrikákat (a teljes szervezet vagy adott biztonsági csoportok).

> [!NOTE]
> Ne feledje, hogy bérlői beállítások módosításának érvénybe lépése időbe telhet.

### <a name="per-user-data-in-usage-metrics-for-content-creators"></a>Felhasználónkénti adatok a használati metrikákban a tartalmak szerzői számára
A tartalmak szerzőinek használati metrikáiban szerepel a tartalmakhoz hozzáférő felhasználók megjelenítendő neve és e-mail-címe. [További információ](service-usage-metrics.md).

A beállítást **Engedélyezve** értékre állíthatja, és megadhatja, hogy ki láthatja a megjelenített nevet és az e-mail-címet a használati metrikákban (a teljes szervezet vagy adott biztonsági csoportok).

A felhasználónkénti adatok alapértelmezés szerint engedélyezve vannak a használati metrikákhoz, a tartalomkészítői fiókadatok pedig szerepelnek a metrikák jelentéseiben. Ha ezt az információt nem szeretné belefoglalni egyes felhasználók esetében, tiltsa le a funkciót megadott biztonsági csoportok, vagy a teljes szervezet számára. A fiókadatok ekkor *névtelenként* jelennek meg a jelentésben.

> [!NOTE]
> Ne feledje, hogy bérlői beállítások módosításának érvénybe lépése időbe telhet.


## <a name="dashboard-settings"></a>Irányítópult beállításai

### <a name="data-classification-for-dashboards"></a>Irányítópultok adatainak besorolása

A munkahelyi felhasználók a biztonsági szint besorolását jelző címkékkel láthatják el az irányítópultokat. [További információ](service-data-classification.md)

> [!NOTE]
> Ez a beállítás az egész munkahelyre vonatkozik, és nem lehet korlátozni meghatározott csoportokra.

## <a name="developer-settings"></a>Fejlesztői beállítások

### <a name="embed-content-in-apps"></a>Tartalom beágyazása alkalmazásokba

A munkahelyi felhasználók beágyazhatnak Power BI-irányítópultokat és -jelentéseket szolgáltatott szoftveres (SaaS-) alkalmazásokba. A beállítás kikapcsolásával megakadályozhatja, hogy a felhasználók a REST API-k használatával Power BI-tartalmakat ágyazzanak be saját alkalmazásukba.

## <a name="capacity-settings"></a>Kapacitásbeállítások

### <a name="premium-settings"></a>Premium-beállítások

A Premium-beállítások lapon bármely Power BI Premium-kapacitás (Em vagy P termékváltozat) felügyelhető, amelyet a munkahely megvásárolt. A munkahely bármely felhasználója láthatja a Premium-beállítások lapot, de annak tartalma csak akkor jelenik meg, ha az adott felhasználó **kapacitás-rendszergazda**, vagy rendelkezik a szükséges engedélyekkel. Ha a felhasználó nem rendelkezik ilyen engedéllyel, az alábbi üzenet jelenik meg.

![A Power BI Premium adminisztrátori beállításai](media/service-admin-portal/premium-settings-no-access.png "Nincs hozzáférés a Premium-beállításokhoz")

További információ a Premium-beállítások kezeléséről: [A Power BI Premium kezelése](service-admin-premium-manage.md).

### <a name="power-bi-embedded-settings"></a>Power BI Embedded-beállítások

A Power BI Embedded beállítások lapján megtekintheti a Power BI Embedded (A termékváltozat) kapacitásait, amelyeket az ügyfelének vásárolt. Mivel az Azure-tól csak A termékváltozatot vásárolhat, a [beágyazott kapacitások Azure-ban való kezelésére](developer/azure-pbie-create-capacity.md) az **Azure Portalt** használhatja.

![A Power BI Embedded adminisztrátori beállításai](media/service-admin-portal/manage-pbie-capacities-01.png)

![A Power BI Embedded adminisztrátori beállításainak részletei](media/service-admin-portal/manage-pbie-capacities-02.png)

A Power BI Embedded (A termékváltozat) beállításainak kezeléséről további információért lásd a [Mi a Power BI Embedded](developer/azure-pbie-what-is-power-bi-embedded.md) szakaszt.

## <a name="embed-codes"></a>Beágyazási kódok

![Beágyazási kódok a Power BI felügyeleti portálon](media/service-admin-portal/embed-codes.png)

A rendszergazdák megnézhetik a bérlő számára generált beágyazási kódokat. Elérhetőek a jelentés megtekintésére, valamint a visszavonáshoz a beágyazási kód törlésére vonatkozó műveletek is.

## <a name="organization-visuals"></a>Szervezeti vizualizációk

A szervezeti vizualizációk lapon egyéni vizualizációkat helyezhet el és kezelhet a szervezetén belül, így könnyen alkalmazhat jogvédett egyéni vizualizációkat a szervezetében, amelyeket a jelentéskészítők könnyen megtalálhatnak és importálhatnak a jelentéseikbe közvetlenül a Power BI Desktopból.

A lapon minden olyan egyéni vizualizáció megjelenik, amely jelenleg megtalálható a szervezet adattárában.

![Szervezeti rendszergazdai visualizáció](media/service-admin-portal/power-bi-custom-visuals-organizational-admin-01.png)

### <a name="add-a-new-custom-visual"></a>Új egyéni vizualizáció hozzáadása

Új egyéni vizualizáció a listához adásához válassza az **Egyéni vizualizáció hozzáadása** lehetőséget

![](media/service-admin-portal/power-bi-custom-visuals-organizational-admin-02.png)

> [!WARNING]
> Az egyéni vizualizációk biztonsági vagy adatvédelmi kockázatot jelentő kódokat tartalmazhatnak, ezért az adattárban való üzembe helyezés előtt ellenőrizze, hogy megbízható-e a vizualizáció szerzője és forrása.

Töltse ki a mezőket:

* Válasszon egy .pbiviz-fájlt (kötelező): Válasszon ki egy feltöltendő egyéni vizualizációs fájlt. Csak a verziószámmal ellátott API-s vizualizációk támogatottak (itt elolvashatja, ez mit jelent).

Az egyéni vizualizációk feltöltése előtt át kell tekintenie a vizualizációt biztonsági és adatvédelmi szempontból, hogy biztosan megfeleljen a szervezet igényeinek. További információk az egyéni vizualizációk biztonságáról.

* Nevezze el az egyéni vizualizációkat (kötelező): Adjon egy rövid címet a vizualizációnak, a Power BI Desktop felhasználói így könnyen megérthetik, mi annak a célja

* Ikon (kötelező): A Power BI Desktop felhasználói felületén megjelenő ikonfájl.

* Leírás: A vizualizáció rövid leírása, amely több információt szolgáltat a felhasználónak

Az „Alkalmazás“ lehetőséggel kezdje meg a feltöltést. Ha ez sikeres, az új elem megjelenik a listában. Ha nem, egy ennek megfelelő hibaüzenet jelenhet meg

### <a name="delete-a-custom-visual-from-the-list"></a>Egyéni látványelem törlése a listából

A kuka ikonnal végleg törölheti a vizualizációt az adattárból.
Fontos: a törlés nem vonható vissza. A törölt vizualizációk azonnal abbahagyják a renderelést a meglévő jelentésekben. Még ha újra feltölti is a vizualizációt, az nem helyettesíti a törölt verziót, a felhasználók újra importálhatják az új vizualizációt, és kicserélhetik azt a saját jelentésükben található példánnyal.

### <a name="disable-a-custom-visual-in-the-list"></a>Egyéni látványelem letiltása a listában

A vizualizáció szervezeti áruházból való letiltásához válassza a fogaskerék ikont. A **Hozzáférés** szakaszban, tiltsa le az egyéni vizualizációt.

Miután letiltja a vizualizációt, az nem fog megjelenni a meglévő jelentésekben, és az alábbi hibaüzenet jelenik meg.

*Ez az egyéni vizualizáció már nem érhető el. További információért forduljon a rendszergazdához.*

Azonban a könyvjelzőzött vizualizációk továbbra is működnek.

Frissítés vagy rendszergazdai módosítás után a Power BI felhasználóinak újra kell indítaniuk az alkalmazást, vagy a Power BI szolgáltatás használata esetén frissíteniük kell a böngészőt a frissítések megjelenítéséhez.

### <a name="how-to-update-a-visual"></a>A vizualizációk frissítése

Ha szeretné frissíteni az adattárban a vizualizációt, mert annak újabb verziója érhető el (pl. hibajavítások, új funkciók stb.), akkor válassza a **Frissítés** ikont, és töltse fel az új fájlt. Győződjön meg róla, hogy a vizuális azonosító ugyanaz maradt. Az új fájl az előző fájlt helyére kerül a jelentésekben az egész vállalatnál. Ha azonban a vizualizáció új verziója megbontja az előző verziójának valamely használati vagy adatstruktúráját, akkor ne cserélje le az előző verziót. Ehelyett hozzon létre egy új listázást a vizualizáció új verziójához. Például adjon hozzá egy új verziószámot (X.X verzió) az új listázott vizualizáció címéhez. Ezáltal nyilvánvalóvá válik, hogy ez ugyanaz a vizualizáció, de frissített verziószámmal, így a meglévő jelentések működése nem hibásodik meg. Most is győződjön meg róla, hogy a vizuális azonosító ugyanaz maradt. Így amikor a felhasználók legközelebb belépnek a szervezeti adattárba a Power BI Desktopból, importálhatják az új verziót, amely kérni fogja őket, hogy cseréljék le a jelentésben található jelenlegi verziót.

## <a name="next-steps"></a>Következő lépések

[A Power BI rendszergazdai szerepkörének ismertetése](service-admin-role.md)  
[A Power BI-naplózás használata a munkahelyen](service-admin-auditing.md)  
[A Power BI Premium kezelése](service-admin-premium-manage.md)  
[A Power BI felügyelete a munkahelyen](service-admin-administering-power-bi-in-your-organization.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)
