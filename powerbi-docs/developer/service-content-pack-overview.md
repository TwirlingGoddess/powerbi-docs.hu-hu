---
title: "A Power BI szolgáltatás tartalomcsomag-programjának áttekintése"
description: "Tartalomcsomag-tanúsítási program"
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
ms.date: 01/04/2018
ms.author: maghan
ms.openlocfilehash: 1eaa549bf42c17cd2bd857efd4d50b991e862ea0
ms.sourcegitcommit: 25489cf87c31fc107a5337fa1dd36506897c4bbb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2018
---
# <a name="overview-of-the-power-bi-service-content-pack-program"></a>A Power BI szolgáltatás tartalomcsomag-programjának áttekintése
A tartalomcsomagok olyan nem beépített tartalmakból álló csomagok, amelyekkel a felhasználók azonnali elemzésekhez juthatnak adatforrásaikból. A tartalomcsomagok általában egy adott üzleti forgatókönyvre fókuszálva elemzéseket készítenek egy szerepkörről, tartományról vagy munkafolyamatról.

A független szoftvergyártók (ISV-k) sablonalapú tartalomcsomagokat készítenek, amelyeket a felhasználók a fiókjukhoz kapcsolhatnak és példányosíthatnak. Tartományszakértőkként könnyen fogyaszthatóvá tehetik az adatokat az üzleti felhasználók számára. A tartalomcsomagok alkalmi megfigyelési és elemzési lehetőségeket biztosítanak az ügyfelek számára anélkül, hogy ehhez jelentős beruházásokra lenne szükség a jelentéskészítési infrastruktúrában. 

Az említett, ISV-k által létrehozott sablonalapú tartalomcsomagokat ez után elküldheti a Power BI csapatának, így nyilvánosan is elérhetők lesznek a Power BI tartalomcsomag-katalógusában (app.powerbi.com/getdata/services), illetve a Microsoft AppSource webhelyen (appsource.microsoft.com). A nyilvános tartalomcsomagok egyik példája [itt](template-content-pack-experience.md) tekinthető meg.

## <a name="overview"></a>Áttekintés
A sablonalapú tartalomcsomagok létrehozásának és beküldésének általános folyamata több lépésből áll.

 ![Folyamat](media/service-content-pack-overview/developer-content-pack-overview.png)

1. [Tekintse át a követelményeket](#requirements), és győződjön meg arról, hogy teljesülnek
2. [Hozzon létre a tartalmat](template-content-pack-authoring.md#queries) a Power BI Desktopban
3. [Hozzon létre egy irányítópultot](template-content-pack-authoring.md#dashboard) a PowerBI.com webhelyen
4. [Tesztelje a tartalomcsomagot](template-content-pack-testing.md) saját kezűleg a cégen belül
5. [Küldje be](template-content-pack-testing.md#submission) a tartalmat a Power BI csapatának közzétételre

<a name="requirements"></a>

## <a name="requirements"></a>Követelmények
Ahhoz, hogy létrehozzon egy tartalomcsomagot, majd beküldje a Power BI szolgáltatásban és az AppSource webhelyen való közzétételre, az alábbi követelményeknek kell megfelelnie:

* Rendelkeznie kell üzleti felhasználók által használt Saas-alkalmazással.
* Az SaaS-alkalmazásnak olyan felhasználói adatokat kell tartalmaznia, amelyek megjeleníthetők a Power BI-ban.
* Az SaaS-alkalmazásnak az interneten keresztül nyilvánosan elérhető API-val kell rendelkeznie. Ideális esetben az API egy REST-alapú API vagy OData-csatorna. A Power BI tartalomcsomagok több hitelesítéstípust is támogatnak, mint az alapszintű hitelesítés, az OAuth 2.0 és az API-kulcs. 
* SaaS-alkalmazása számára engedélyezve van tartalomcsomag közzététele. Kérelem beküldése: pbiservicesapps@microsoft.com. Minden kérelmet a relevancia és a várható használat alapján értékelünk. 
* Aláírt partnerszerződéssel kell rendelkeznie. Ezt a [beküldés lépésben](template-content-pack-testing.md#submission) fogja megtenni.

Kérjük, tekintse át a [tartalomkészítés](template-content-pack-authoring.md) szakaszt, amelyben részletesebben olvashat a technikai követelményekről.

## <a name="business-scenario"></a>Vállalati forgatókönyv
A tartalomcsomagok egy adott üzleti forgatókönyvre fókuszáló elemzéseket és metrikákat biztosítanak. A célközönség és a tartalomcsomagok által nyújtott előnyök megismerésével biztosítható, hogy a felhasználók eredményesen használhatják a nekik készült tartalmakat.

### <a name="tips"></a>Tippek
* Azonosítsa a közönséget, és a feladatot, amelyet el szeretnének végezni.  
* Fókuszáljon egy adott időszakra (az elmúlt 90 nap) vagy az utolsó N számú eredményre.  
* Csak a forgatókönyvéhez kapcsolódó táblákat/oszlopokat importálja.  
* Fontolja meg több tartalomcsomag felajánlását különféle egyéni forgatókönyvekhez.  

## <a name="frequently-asked-questions"></a>Gyakori kérdések
**Létrehozhatok Power BI szolgáltatás-tartalomcsomagot olyan harmadik féltől származó SaaS-alkalmazáshoz, amely nem az én tulajdonom?**

Nem, jelenleg partnerszerződést kell aláírnia a SaaS-alkalmazás tulajdonosával, mielőtt közzétehetné a tartalomcsomagot a szolgáltatásban.

**Nem rendelkezem nyilvános fejlesztői API-val a szolgáltatásomhoz. Így is létrehozhatok olyan Power BI szolgáltatás-tartalomcsomagot, amely közvetlenül az adattárolóból kéri le az adatokat?**

Nem, a Power BI szolgáltatáshoz készült tartalomcsomagokhoz az interneten keresztül nyilvánosan elérhető fejlesztői API-ra van szükség.

**Milyen API-kat támogatnak a szolgáltatás-tartalomcsomagok, és milyen hitelesítéstípusokkal működnek?**

A Power BI szolgáltatás-tartalomcsomagok minden REST API-t és OData-csatornát támogatnak. A Power BI több hitelesítéstípussal is működik, mint például az alapszintű hitelesítés, az Oauth 2.0 és a Webes API-kulcs. A technikai követelményekről részletesebben a [tartalomkészítésről](template-content-pack-authoring.md#dashboard) szóló cikkben olvashat.

**További kérdéseim vannak a szolgáltatás-tartalomcsomagokkal kapcsolatban. Hogyan léphetek kapcsolatba Önökkel?**

Kérdéseit elküldheti a következő e-mail-címre: pbiservicesapps@microsoft.com.

## <a name="support"></a>Támogatás
Ha a fejlesztési szakaszban van szüksége támogatásra, használja a következő webhelyet: [https://powerbi.microsoft.com/support](https://powerbi.microsoft.com/support). A támogatási webhelyet aktívan figyeljük és kezeljük. Az ügyfélincidensek gyorsan eljutnak a megfelelő csapathoz.

## <a name="next-step"></a>Következő lépés
[Tartalomkészítés](template-content-pack-authoring.md)

