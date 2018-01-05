---
title: "Power BI felügyeleti portál"
description: "A felügyeleti portál a Power BI bérlői felügyeletét teszi lehetővé a munkahelyen. Olyan lehetőségeket kínál, mint például a használati metrikák, hozzáférés az Office 365 felügyeleti központjához, valamint a beállítások."
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
ms.date: 11/27/2017
ms.author: asaxton
ms.openlocfilehash: d831363d6afa88aa94d78776f59f81ba8ba96299
ms.sourcegitcommit: 85302d577895e779466df55aa02e5785ab2e3138
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/18/2017
---
# <a name="power-bi-admin-portal"></a>Power BI felügyeleti portál

A felügyeleti portál a Power BI bérlői felügyeletét teszi lehetővé a munkahelyen. Olyan lehetőségeket kínál, mint például a használati metrikák, hozzáférés az Office 365 felügyeleti központjához, valamint a beállítások.

A cégnél a Power BI bérlői felügyelete a Power BI felügyeleti portálján keresztül történik. A felügyeleti portálhoz az Office 365 minden globális rendszergazdája hozzáférhet, valamint olyan felhasználók is, akik Power BI-szolgáltatásadminisztrátori szerepkört kaptak. További információ a Power BI-szolgáltatásadminisztrátori szerepkörről: [A Power BI rendszergazdai szerepkörének ismertetése](service-admin-role.md).

Az összes felhasználó láthatja a **Felügyeleti portál** menüpontot a fogaskerék ikonja alatt. Ha nem rendszergazdáról van szó, a felhasználó csak a **Premium-beállítások** szakaszt látja, és csak azok a kapacitások jelennek meg, amelyek felügyeletéhez a felhasználó jogosultsággal rendelkezik.

## <a name="how-to-get-to-the-admin-portal"></a>A felügyeleti portál elérése

A Power BI felügyeleti portál eléréséhez az adott fiókot **globális rendszergazdaként** kell megjelölni az Office 365-ben vagy az Azure Active Directoryban, vagy Power BI-szolgáltatásadminisztrátori szerepkört kell hozzárendelni. További információ a Power BI-szolgáltatásadminisztrátori szerepkörről: [A Power BI rendszergazdai szerepkörének ismertetése](service-admin-role.md). A Power BI felügyeleti portál eléréséhez tegye az alábbiakat.

1. Válassza ki a Beállítások fogaskereket a Power BI szolgáltatás jobb felső sarkában.
2. Válassza a **Felügyeleti portál** lehetőséget.

![](media/service-admin-portal/powerbi-admin-settings.png)

A portálon öt lap található. Ezek leírását az alábbiakban láthatja.

* [Használati metrikák](#usage-metrics)
* [Felhasználók](#users)
* [Auditnaplók](#audit-logs)
* [Bérlői beállítások](#tenant-settings)
* [Premium-beállítások](#premium-settings)
* [Beágyazási kódok](#embed-codes)

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

A megadott beállítások alapján a beállításoknak három állapota lehet.

### <a name="disabled-for-the-entire-organization"></a>Az egész munkahelyen sehol nem engedélyezett

Letilthat egy funkciót, így a felhasználók nem fogják tudni használni azt.

![](media/service-admin-portal/powerbi-admin-tenant-settings-disabled.png)

### <a name="enabled-for-the-entire-organization"></a>Az egész munkahelyen mindenhol engedélyezett

Engedélyezhet egy funkciót az egész munkahelyen, így minden felhasználó hozzáférhet ahhoz.

![](media/service-admin-portal/powerbi-admin-tenant-settings-enabled.png)

### <a name="enabled-for-a-subset-of-the-organization"></a>A munkahely egy alegységénél engedélyezett

A funkciókat a munkahely egy adott alegységénél is engedélyezheti. Erre különböző módokon kerülhet sor. Engedélyezhet egy funkciót az egész munkahelyen a felhasználók egy adott csoportja kivételével.

![](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except.png)

Engedélyezhet egy funkciót a felhasználók egy adott csoportjában, és letilthatja azt a felhasználók egy másik csoportjában. Így garantálható, hogy egyes felhasználók még akkor sem férhetnek hozzá az adott funkcióhoz, ha egyébként benne vannak az engedélyezett csoportban.

![](media/service-admin-portal/powerbi-admin-tenant-settings-enabled-except2.png)

## <a name="export-and-sharing-settings"></a>Exportálási és megosztási beállítások

### <a name="share-content-to-external-users"></a>Tartalom megosztása külső felhasználókkal

A munkahelyi felhasználók külső felhasználókkal oszthatnak meg irányítópultokat.

![](media/service-admin-portal/powerbi-admin-sharing-external.png)

### <a name="publish-to-web"></a>Webes közzététel

A munkahelyi felhasználók a weben tehetnek közzé jelentéseket. [További információ](service-publish-to-web.md)

![](media/service-admin-portal/powerbi-admin-publish-to-web.png)

A webes közzététel beállításától függően a felhasználók különféle lehetőségeket láthatnak majd a felhasználói felületen.

|Funkció |A teljes cég számára engedélyezve |A teljes cég számára letiltva |Speciális biztonsági csoportok   |
|---------|---------|---------|---------|
|A **Webes közzététel** parancs egy jelentés **Fájl** menüjében.|Mindenki számára engedélyezve|Mindenki számára nem látható|Csak az arra jogosult felhasználók vagy csoportok láthatják.|
|A **Beágyazási kódok kezelése** funkció a **Beállítások** közt|Mindenki számára engedélyezve|Mindenki számára engedélyezve|Mindenki számára engedélyezve<br><br>* A **Törlés** parancsot csak az arra jogosult felhasználók vagy csoportok érik el.<br>* A **Kód lekérése** mindenki számára engedélyezve van.|
|**Beágyazási kódok** a felügyeleti portálon|Az állapot a következő értékeket jelenítheti meg:<br>* Aktív<br>* Nem támogatott<br>* Blokkolva|Az állapot **Letiltva** lesz|Az állapot a következő értékeket jelenítheti meg:<br>* Aktív<br>* Nem támogatott<br>* Blokkolva<br><br>Ha egy felhasználónak nincs megfelelő jogosultsága a bérlői beállítások alapján, akkor az állapot **Megsértve** lesz.|
|Meglévő közzétett jelentések|Minden engedélyezve|Minden letiltva|A jelentések továbbra is megjelennek mindenki számára.|

### <a name="export-data"></a>Adatok exportálása

A munkahelyi felhasználók adatokat exportálhatnak egy csempéről vagy vizualizációból. [További információ](power-bi-visualization-export-data.md)

![](media/service-admin-portal/powerbi-admin-export-data.png)

> [!NOTE]
> Az **Adatok exportálása** lehetőség letiltásával azt is megakadályozhatja, hogy a felhasználók az **Elemzés az Excelben** funkciót vagy a Power BI szolgáltatás élő kapcsolatát használják.

### <a name="export-reports-as-powerpoint-presentations"></a>Jelentések exportálása PowerPoint-bemutatóként

A munkahelyi felhasználók PowerPoint-fájlként exportálhatják a Power BI-jelentéseket. [További információ](service-publish-to-powerpoint.md)

![](media/service-admin-portal/powerbi-admin-powerpoint.png)

### <a name="print-dashboards-and-reports"></a>Irányítópultok és jelentések nyomtatása

A munkahelyi felhasználók irányítópultokat és jelentéseket nyomtathatnak. [További információ](service-print.md)

![](media/service-admin-portal/powerbi-admin-print-dashboard.png)

![](media/service-admin-portal/powerbi-admin-print-report.png)

## <a name="content-pack-settings"></a>Tartalomcsomag-beállítások

### <a name="publish-content-packs-to-the-entire-organization"></a>Tartalomcsomagok közzététele az egész munkahely számára

A munkahelyi felhasználók tartalomcsomagokat tehetnek közzé az egész munkahely számára.

![](media/service-admin-portal/powerbi-admin-publish-entire-org.png)

### <a name="create-template-organizational-content-packs"></a>Munkahelyi tartalomcsomagok sablonjainak létrehozása

A munkahelyi felhasználók tartalomcsomag-sablonokat készíthetnek, amelyek a Power BI Desktop adott adatforrására épülő adatkészleteket használják.

## <a name="integration-settings"></a>Integrálási beállítások

### <a name="ask-questions-about-data-using-cortana"></a>Adatokkal kapcsolatos kérdések feltevése Cortanával
A munkahelyi felhasználók Cortana használatával kérdéseket tehetnek fel az adataikról.

> [!NOTE]
> Ez a beállítás az egész munkahelyre vonatkozik, és nem lehet korlátozni meghatározott csoportokra.

### <a name="use-analyze-in-excel-with-on-premises-datasets"></a>Az Elemzés az Excelben helyszíni adatkészleteken való használata
A munkahelyi felhasználók az Excel használatával megtekinthetik és használhatják a helyszíni Power BI-adatkészleteket. [További információ](service-analyze-in-excel.md)

> [!NOTE]
> Az **Adatok exportálása** lehetőség letiltásával azt is megakadályozhatja, hogy a felhasználók az **Elemzés az Excelben** funkciót használják.

### <a name="user-arcgis-maps-for-power-bi-preview"></a>Az ArcGIS Maps for Power BI (előzetes verzió) használata

A munkahelyi felhasználók használhatják az Esri által biztosított ArcGIS Maps for Power BI (előzetes verzió) vizualizációját. [További információ](power-bi-visualization-arcgis.md)

## <a name="r-visuals-settings"></a>R-vizualizációk beállításai

### <a name="interact-with-an-dshare-r-visuals"></a>Az R-vizualizációk interaktív használata és megosztása

A munkahelyi felhasználók R-szkriptekkel készült vizualizációkat használhatnak és oszthatnak meg. [További információ](service-r-visuals.md)

> [!NOTE]
> Ez a beállítás az egész munkahelyre vonatkozik, és nem lehet korlátozni meghatározott csoportokra.

## <a name="audit-settings"></a>Naplózási beállítások

### <a name="create-audit-logs-for-internal-activity-auditing-and-compliance"></a>Auditnaplók létrehozása a belső tevékenységek vizsgálatához és a megfelelőség biztosításához

A felhasználók a naplózással nyomon követhetik, hogy a munkahely más felhasználói milyen műveleteket hajtottak végre a Power BI-ban. [További információ](service-admin-auditing.md)

Az auditnapló bejegyzéseinek rögzítéséhez ezt a beállítást kell bekapcsolni.

> [!NOTE]
> Ez a beállítás az egész munkahelyre vonatkozik, és nem lehet korlátozni meghatározott csoportokra.

## <a name="dashboard-settings"></a>Irányítópult beállításai

### <a name="data-classification-for-dashboards"></a>Irányítópultok adatainak besorolása

A munkahelyi felhasználók a biztonsági szint besorolását jelző címkékkel láthatják el az irányítópultokat. [További információ](service-data-classification.md)

> [!NOTE]
> Ez a beállítás az egész munkahelyre vonatkozik, és nem lehet korlátozni meghatározott csoportokra.

## <a name="developer-settings"></a>Fejlesztői beállítások

### <a name="embed-content-in-apps"></a>Tartalom beágyazása alkalmazásokba

A munkahelyi felhasználók beágyazhatnak Power BI-irányítópultokat és -jelentéseket szolgáltatott szoftveres (SaaS-) alkalmazásokba. A beállítás kikapcsolásával megakadályozhatja, hogy a felhasználók a REST API-k használatával Power BI-tartalmakat ágyazzanak be saját alkalmazásukba.

## <a name="premium-settings"></a>Premium-beállítások

A Premium-beállítások lapon bármely Power BI Premium-kapacitás felügyelhető, amelyet a munkahely megvásárolt. A munkahely bármely felhasználója láthatja a Premium-beállítások lapot, de annak tartalma csak akkor jelenik meg, ha az adott felhasználó **kapacitás-rendszergazda**, vagy rendelkezik a szükséges engedélyekkel. Ha a felhasználó nem rendelkezik ilyen engedéllyel, az alábbi üzenet jelenik meg.

![](media/service-admin-portal/premium-settings-no-access.png "Nincs hozzáférés a Premium-beállításokhoz")

További információ a Premium-beállítások kezeléséről: [A Power BI Premium kezelése](service-admin-premium-manage.md).

## <a name="embed-codes"></a>Beágyazási kódok

![Beágyazási kódok a Power BI felügyeleti portálon](media/service-admin-portal/embed-codes.png)

A rendszergazdák megnézhetik a bérlő számára generált beágyazási kódokat. Elérhetőek a jelentés megtekintésére, valamint a visszavonáshoz a beágyazási kód törlésére vonatkozó műveletek is.

## <a name="next-steps"></a>Következő lépések

[A Power BI rendszergazdai szerepkörének ismertetése](service-admin-role.md)  
[A Power BI-naplózás használata a munkahelyen](service-admin-auditing.md)  
[A Power BI Premium kezelése](service-admin-premium-manage.md)  
[A Power BI felügyelete a munkahelyen](service-admin-administering-power-bi-in-your-organization.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)