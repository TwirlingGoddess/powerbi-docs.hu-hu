---
title: "Gyakori kérdések – Power BI Embedded"
description: "Az alábbiakban a Power BI Embeddeddel kapcsolatos gyakori kérdések és válaszok listáját tekintheti át."
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
ms.openlocfilehash: 5f884c9c45627ee3c129daca77e38d17f1223909
ms.sourcegitcommit: 8f72ce6b35aa25979090a05e3827d4937dce6a0d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/27/2017
---
# <a name="frequently-asked-questions-about-power-bi-embedded"></a>Gyakori kérdések – Power BI Embedded

* Ha bármilyen egyéb kérdése van, [kérdezze meg a Power BI közösségét](http://community.powerbi.com/).
* Továbbra is problémába ütközik? Látogasson el a [Power BI támogatási oldalára](https://powerbi.microsoft.com/support/).

## <a name="general"></a>Általános

### <a name="what-is-power-bi-embedded"></a>Mi az a Power BI Embedded?

A Microsoft Power BI Embedded használatával az alkalmazások fejlesztői lenyűgöző és teljes mértékben interaktív jelentéseket, irányítópultokat és csempéket ágyazhatnak alkalmazásaikba, így nem kell időt és pénzt fordítaniuk arra, hogy az alapokról építsék fel saját vizualizációikat és vezérlőelemeiket.

### <a name="who-is-the-target-audience-for-power-bi-embedded"></a>Ki a Power BI Embedded célközönsége?

A saját alkalmazásokat készítő fejlesztők és szoftvercégek, más néven a független szoftvergyártók (ISV-k).

### <a name="how-is-power-bi-embedded-different-from-power-bi-the-service"></a>Mi a különbség a Power BI Embedded és a Power BI szolgáltatás között?

A Power BI Embedded független szoftvergyártók vagy fejlesztők számára készült, akik alkalmazásokat készítenek és vizualizációkat ágyaznak be bennük, hogy ezzel segítsék ügyfeleik döntéseit, de ne kelljen az alapoktól kezdve elemzési megoldásokat létrehozniuk. A beágyazott elemzések használatával a vállalati felhasználók az alkalmazáson belül férhetnek hozzá a vállalati adataikhoz, amelyekben elemzéseket készíthetnek lekérdezések végrehajtásával.

A Power BI pedig egy olyan elemzési szolgáltatottszoftver-megoldás, amely vállalatok számára teszi lehetővé a legfontosabb üzleti adataik egyszerű megtekintését.

### <a name="what-is-the-difference-between-power-bi-premium-and-power-bi-embedded"></a>Mi a különbség a Power BI Premium és a Power BI Embedded között?

A Power BI Premium-kapacitás azokat a nagyvállalatokat célozza meg, akik egy teljes körű Power BI-megoldást szeretnének, amellyel egyetlen helyről áttekinthetik vállalatukat, partnereiket, ügyfeleiket és szállítóikat. A Power BI Premium segítséget nyújt vállalata döntéshozatalaiban. A Power BI Premium egy szolgáltatottszoftver-termék, amely a Power BI portálon, a mobilalkalmazáson és belsőleg fejlesztett alkalmazásokon keresztül a felhasználók számára is lehetővé teszi a tartalmak használatát.

A Power BI Embedded független szoftvergyártók vagy fejlesztők számára készült, akik alkalmazásokat készítenek, és vizualizációkat ágyaznak be bennük. A Power BI Embedded az Ön ügyfelei számára nyújt segítséget a döntéshozatalaik során, ugyanis a Power BI Embedded alkalmazások fejlesztőinek készült, és ezeknek az alkalmazásoknak a vállalaton belüli és kívüli ügyfelei egyaránt használhatják a Power BI Embedded-kapacitásokban tárolt tartalmakat. A Power BI Embedded-kapacitástartalmak nem oszthatók meg egy kattintásos közzététellel a weben vagy a SharePointban, és nem támogatják az SSRS-jelentéseket sem.

### <a name="what-is-the-microsoft-recommendation-for-when-a-customer-should-buy-power-bi-premium-vs-power-bi-embedded"></a>A Microsoft ajánlása alapján mikor érdemes megvásárolni a Power BI Premiumot, és mikor a Power BI Embeddedet?

A Microsoft ajánlása alapján a vállalatoknak a Power BI Premiumot érdemes megvásárolniuk, amely egy nagyvállalati szintű, felhőbeli önkiszolgáló BI-megoldás, a független szoftvergyártóknak pedig a Power BI Embeddedet érdemes megvásárolniuk, amely felhőalapú elemzési képességeket biztosít számukra. Azonban nincsenek korlátozások arra vonatkozóan, hogy ügyfeleink melyik terméket vásárolhatják meg.

Előfordulhatnak olyan esetek, amikor független szoftvergyártók (általában nagyobb méretűek) egy P termékváltozatot szeretnének használni, hogy kihasználhassák az előrecsomagolt Power BI szolgáltatás előnyeit a vállalatukon belül és az alkalmazásaikba ágyazva egyaránt. És persze nagyvállalatok is dönthetnek az Azure-beli A termékváltozatok használata mellet, ha csak az üzletági alkalmazások fejlesztése és az elemzési képességek beágyazása érdekli őket, és nem szeretnék az előrecsomagolt Power BI szolgáltatást használni.

### <a name="when-will-power-bi-embedded-be-available-in-azure"></a>Mikor lesz elérhető a Power BI Embedded az Azure-ban?

A Power BI Embedded már elérhető az Azure-ban.

## <a name="technical"></a>Műszaki

### <a name="what-is-the-difference-between-the-a-skus-in-azure-and-em-skus-in-office-365"></a>Mi a különbség az Azure-beli A termékváltozatok és az Office 365-beli EM termékváltozatok között?

A PowerBI.com egy vállalati megoldás, amely egy szolgáltatott szoftverként számos képességet kínál, többek között közösségi együttműködés lehetőségét és e-mailekre való feliratkozást.

A Power BI Embedded egy fejlesztők számára készült API-gyűjtemény, amellyel platformszolgáltatásokba ágyazhatnak be elemzési megoldásokat. A beágyazott elemzések forgatókönyve esetén a PowerBI.com használata segítséget nyújt a független szoftvergyártóknak és a fejlesztőknek a beágyazott elemzési megoldásaik tartalmainak és a bérlői beállításaik kezeléséhez.

Itt látható egy részlet a különbségek listájából, amely mindkét megoldás esetén hasznos lehet.

|Funkció  |Power BI Embedded<br>(A termékváltozatok) |Power BI Premium-kapacitás<br>(EM termékváltozatok)  |
|---------|---------|---------|
|Összetevők beágyazása Power BI alkalmazás munkaterületeiről     |Azure-kapacitás |Office 365-kapacitás |
|Power BI-licenc szükséges a jelentések használatához |Nem  |Igen |
|Power BI-jelentések használata Embedded-alkalmazásokban |Igen  |Igen |
|Power BI-jelentések használata SharePointban |Nem |Igen |
|Power BI-jelentések használata Teamsben |Nem |Igen |

### <a name="power-bi-now-offers-three-skus-for-embedding-a-skus-em-skus-and-p-skus-which-one-should-i-purchase-for-my-scenario"></a>A Power BI három típusú termékváltozatot kínál a beágyazásra: az A termékváltozatokat, az EM termékváltozatokat és a P termékváltozatokat. Melyiket vásároljam meg a saját forgatókönyvemhez?

|  |A termékváltozat (Power BI Embedded)  |EM termékváltozat (Power BI Premium)  |P termékváltozat (Power BI Premium)  |
|---------|---------|---------|---------|
|Vásárlás     |Azure Portal |Office |Office |
|Felhasználási módok |* Tartalmak beágyazása saját alkalmazásba |* Tartalmak beágyazása saját alkalmazásba<br>* Tartalmak megosztása Power BI FREE-felhasználókkal a PowerBI.com-on kívül, és tartalmak beágyazása más SaaS-alkalmazásokban (SharePoint, Teams) |* Tartalmak beágyazása saját alkalmazásba<br>* Tartalmak megosztása Power BI FREE-felhasználókkal a PowerBI.com-on kívül, és tartalmak beágyazása más SaaS-alkalmazásokban (SharePoint, Teams)<br>* Tartalmak megosztása Power BI FREE-felhasználókkal a PowerBI.com-on keresztül  |
|Számlázás |Óránként |Havonta |Havonta |
|Kötelezettségvállalás  |Nincs kötelezettségvállalás |Éves  |Havi/Éves |
|Megkülönböztetés |Az Azure Portalon vagy API-kon keresztül teljes mértékű rugalmasságot tesz lehetővé, vagyis felfelé és lefelé történő méretezhetőséget, illetve az erőforrások felfüggesztését és folytatását  |Tartalmak beágyazására használható a SharePointban vagy a Microsoft Teamsben |Egy kapacitáson belül egyesíti az alkalmazásokba történő beágyazásokat és a Power BI szolgáltatás használatát |

### <a name="how-can-i-monitor-capacity-consumption"></a>Hogyan tudom monitorozni a kapacitás felhasználását?

Az Azure-on keresztül történő monitorozás már szerepel a rövid távú terveink között. A Power BI Embedded Azure-erőforrás tartalmazni fog állapotot és használatot monitorozó KPI-ket is.

### <a name="will-my-capacity-scale-automatically-to-adjust-to-the-consumption-of-my-app"></a>Automatikusan méretezi magát a kapacitásom, hogy igazodjon az alkalmazásom felhasználásához?

Jelenleg nincs automatikus méretezés, ugyanakkor bármikor bármelyik API méretezhető.

### <a name="what-is-the-authentication-model-for-power-bi-embedded"></a>Milyen hitelesítési modellt használ a Power BI Embedded?

A Power BI Embedded továbbra is az Azure AD használatával hitelesíti a fő felhasználót (a Power BI Pro-licenccel rendelkező kijelölt felhasználót) és a Power BI-ban található alkalmazást.

Az alkalmazások felhasználóinak hitelesítését és engedélyezését a független szoftvergyártó implementálja, így a független szoftvergyártók használhatnak saját hitelesítést az alkalmazásaikban.

Ha már rendelkezik egy Azure AD-bérlővel, akkor használhatja meglévő címtárát, vagy létrehozhat egy új Azure AD-bérlőt a beágyazott alkalmazásai tartalmainak biztonságához.

### <a name="how-is-power-bi-embedded-different-from-other-azure-services"></a>Miben különbözik a Power BI Embedded más Azure-szolgáltatásoktól?

A független szoftvergyártónak vagy a fejlesztőnek rendelkeznie kell egy Power BI-fiókkal, mielőtt az Azure-ban megvásárolná a Power BI Embeddedet. A Power BI-fiókja határozza meg a Power BI Embeddedjének üzembe helyezési régióját. A Power BI Embedded-kapacitását az Azure-ban kezelheti:

* Méretezheti felfelé vagy lefelé
* Felvehet kapacitás-rendszergazdákat
* Szüneteltethet és folytathat szolgáltatásokat

A PowerBI.com használatával munkaterületeket rendelhet a Power BI Embedded-kapacitásához, vagy megszüntetheti a hozzárendeléseket.

### <a name="what-deploy-regions-are-supported"></a>Mely üzembe helyezési régiók támogatottak?

Délkelet-Ausztrália, Dél-Brazília, Közép-Kanada, USA 2. keleti régiója, Nyugat-India, Kelet-Japán, USA északi középső régiója, Észak-Európa, USA déli középső régiója, Délkelet-Ázsia, Egyesült Királyság déli régiója, Nyugat-Európa, az USA nyugati régiója és az USA 2. nyugati régiója.

## <a name="licensing"></a>Licencelés

### <a name="how-do-i-purchase-power-bi-embedded"></a>Hogyan tudom megvásárolni a Power BI Embeddedet?

A Power BI Embedded az Azure-on keresztül érhető el.

### <a name="how-power-bi-embedded-be-metered"></a>Hogyan történik a Power BI Embedded forgalmi díjának mérése?

A Power BI Embedded forgalmi díjának mérése óránként történik.

### <a name="how-does-the-usage-of-power-bi-embedded-show-up-on-my-bill"></a>Hogyan jelenik meg a Power BI Embedded használata a számlámon?

A Power BI Embedded költségeinek számlázása könnyen előrejelezhető módon, óránként történik az üzembe helyezett csomópont(ok) típusa alapján.

### <a name="what-happens-if-i-already-purchased-power-bi-premium-and-now-i-want-some-of-the-benefits-of-power-bi-embedded-in-azure"></a>Mi történik akkor, ha már megvásároltam a Power BI Premiumot és szeretném használni az Azure-beli Power BI Embedded néhány előnyös funkcióját?

Az ügyfelek továbbra is fizetnek a megvásárolt Power BI Premiumukért az aktuális megállapodásuk szerinti időszak végéig, ezt követően igényeik szerint válthatnak a megvásárolt Power BI Premiumukról.

### <a name="do-i-still-have-to-buy-power-bi-premium-to-get-access-to-power-bi-embedded"></a>Meg kell vásárolnom a Power BI Premiumot, hogy hozzáférhessek a Power BI Embeddedhez?

Nem, a Power BI Embedded magában foglalja a megoldásainak üzembe helyezéséhez és terjesztéséhez szükséges Azure-alapú kapacitást.

### <a name="who-needs-a-power-bi-pro-license-for-power-bi-embedded-and-why"></a>Kinek van szüksége a Power BI Embeddedhez Power BI Pro-licencre, és miért?

Szükségük van Power BI Pro-licencre az elemzőknek, akik jelentéseket vesznek fel Power BI-munkaterületeken, a REST API-kat használó fejlesztőknek, illetve a bérlőrendszergazdáknak, akik a Power BI-bérlőt és -kapacitást kezelik.

A Power BI Embedded a beágyazott tartalmak jóváhagyása és kezelése céljából engedélyezi a Power BI-portál használatát, ezért a PowerBI.com-on belül található alkalmazás hitelesítéséhez Power BI Pro-licenc szükséges, hogy az alkalmazás hozzáférhessen a megfelelő adattárakban található jelentésekhez.

### <a name="can-i-get-started-for-free"></a>Elkezdhetem ingyen a használatát?

Igen, használhatja az [Azure-kreditjeit](https://azure.microsoft.com/free/) a Power BI Embeddedhez.

### <a name="can-i-get-a-trial-experience-for-power-bi-embedded-in-azure"></a>Van lehetőség az Azure-beli Power BI Embedded kipróbálására?

Mivel a Power BI Embedded az Azure része, így használhatja ezt a szolgáltatást az [Azure-regisztráció során kapott 200 $ értékű kreditjéből](https://azure.microsoft.com/free/).

### <a name="whats-the-purchase-commitment-for-power-bi-embedded"></a>Milyen kötelezettségeket kell vállalni a Power BI Embedded megvásárlásakor? 

Ügyfeleink a használatukat óránként módosíthatják. A Power BI Embedded szolgáltatás esetén nincs havi vagy éves kötelezettségvállalás.

### <a name="where-is-power-bi-embedded-available-us-government-germany-china-what-is-the-timing"></a>Hol érhető el a Power BI Embedded? Az Egyesül Államok kormányzati szervei számára? Németországban? Kínában? Mi az ütemezés?

A Power BI Embedded az Azure kereskedelmi felhőiben lesz általánosan elérhető.  A független felhőkben való elérhetőség a későbbiekben várható.

### <a name="is-power-bi-embedded-available-for-non-profits-and-educational"></a>Létezik non-profit vagy oktatási intézményeknek szánt Power BI Embedded?

A non-profit és oktatási intézmények megvásárolhatják az Azure-t. Nincs az Azure-ban különleges díjszabásunk az ilyen típusú ügyfeleink számára.

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)