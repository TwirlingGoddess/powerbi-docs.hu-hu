---
title: Gyakori kérdések – Power BI Embedded
description: Az alábbiakban a Power BI Embeddeddel kapcsolatos gyakori kérdések és válaszok listáját tekintheti át.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 04/23/2018
ms.author: maghan
ms.openlocfilehash: 255efac5d5bf73bca3126f869d4c7434d5c6ef0f
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
ms.locfileid: "34289740"
---
# <a name="frequently-asked-questions-about-power-bi-embedded"></a>Gyakori kérdések – Power BI Embedded

* Ha bármilyen egyéb kérdése van, [kérdezze meg a Power BI közösségét](http://community.powerbi.com/).
* Továbbra sem találja a megoldást? Látogasson el a [Power BI támogatási oldalára](https://powerbi.microsoft.com/support/).

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

### <a name="how-many-embed-tokens-can-i-create"></a>Hány beágyazási tokent hozhatok létre?

A PRO licenccel a beágyazási tokenek elsődlegesen fejlesztési tesztelésre használhatók, a Power BI fő fiókja csak korlátozott mennyiségű tokent tud előállítani. Éles környezetben használt beágyazásokhoz [kapacitást szükséges vásárolni](#technical). Kapacitásvásárlás esetén nincs korlátja a beágyazási tokenek előállításának. Az [Elérhető szolgáltatások beszerzése](https://msdn.microsoft.com/library/mt846473.aspx) oldalon ellenőrizheti az aktuális beágyazott használatot százalékosan jelző használati értéket.

## <a name="technical"></a>Műszaki

### <a name="what-is-the-difference-between-the-a-skus-in-azure-and-the-em-skus-in-office-365"></a>Mi a különbség az Azure-beli „A” termékváltozatok és az Office 365-beli „EM” termékváltozatok között?

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

### <a name="what-are-the-prerequisites-to-create-a-pbie-capacity-in-azure"></a>Milyen feltételekkel hozható létre PBIE-kapacitás az Azure-ban?

- Be kell jelentkeznie a vállalati címtárba (MSA-fiókok nincsenek támogatva).
- Power BI-bérlővel kell rendelkeznie, azaz a címtár legalább egy felhasználójának regisztrálva kell lennie a Power BI-ban. 
- A vállalati címtárban szerepelnie kell egy Azure-előfizetésnek.

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

### <a name="what-type-of-content-pack-data-can-be-embedded"></a>Milyen típusú tartalomcsomagot lehet beágyazni?

A tartalomcsomagok adathalmazaiból készült **irányítópultokat** és **csempéket** *nem lehet beágyazni*, a tartalomcsomagok adathalmazaiból készült **jelentések** viszont *beágyazhatók*.

## <a name="licensing"></a>Licencelés

### <a name="how-do-i-purchase-power-bi-embedded"></a>Hogyan tudom megvásárolni a Power BI Embeddedet?

A Power BI Embedded az Azure-on keresztül érhető el.

### <a name="what-happens-if-i-already-purchased-power-bi-premium-and-now-i-want-some-of-the-benefits-of-power-bi-embedded-in-azure"></a>Mi történik akkor, ha már megvásároltam a Power BI Premiumot és szeretném használni az Azure-beli Power BI Embedded néhány előnyös funkcióját?

Az ügyfelek továbbra is fizetnek a megvásárolt Power BI Premiumukért az aktuális megállapodásuk szerinti időszak végéig, ezt követően igényeik szerint válthatnak a megvásárolt Power BI Premiumukról.

### <a name="do-i-still-have-to-buy-power-bi-premium-to-get-access-to-power-bi-embedded"></a>Meg kell vásárolnom a Power BI Premiumot, hogy hozzáférhessek a Power BI Embeddedhez?

Nem, a Power BI Embedded magában foglalja a megoldásainak üzembe helyezéséhez és terjesztéséhez szükséges Azure-alapú kapacitást.

### <a name="whats-the-purchase-commitment-for-power-bi-embedded"></a>Milyen kötelezettségeket kell vállalni a Power BI Embedded megvásárlásakor? 

Ügyfeleink a használatukat óránként módosíthatják. A Power BI Embedded szolgáltatás esetén nincs havi vagy éves kötelezettségvállalás.

### <a name="how-does-the-usage-of-power-bi-embedded-show-up-on-my-bill"></a>Hogyan jelenik meg a Power BI Embedded használata a számlámon?

A Power BI Embedded költségeinek számlázása könnyen előrejelezhető módon, óránként történik az üzembe helyezett csomópont(ok) típusa alapján. Vegye figyelembe, hogy ha az erőforrása aktív, abban az esetben akkor is díjat számolunk fel, ha nem történik tényleges használat. Ha nem szeretne díjat fizetni, az erőforrást kifejezetten szüneteltetnie kell.

### <a name="who-needs-a-power-bi-pro-license-for-power-bi-embedded-and-why"></a>Kinek van szüksége a Power BI Embeddedhez Power BI Pro-licencre, és miért?

Szükségük van Power BI Pro-licencre az elemzőknek, akik jelentéseket vesznek fel Power BI-munkaterületeken, a REST API-kat használó fejlesztőknek, illetve a bérlőrendszergazdáknak, akik a Power BI-bérlőt és -kapacitást kezelik.

A Power BI Embedded a beágyazott tartalmak jóváhagyása és kezelése céljából engedélyezi a Power BI-portál használatát, ezért a PowerBI.com-on belül található alkalmazás hitelesítéséhez Power BI Pro-licenc szükséges, hogy az alkalmazás hozzáférhessen a megfelelő adattárakban található jelentésekhez.

### <a name="can-i-get-started-for-free"></a>Elkezdhetem ingyen a használatát?

Igen, használhatja az [Azure-kreditjeit](https://azure.microsoft.com/free/) a Power BI Embeddedhez.

### <a name="can-i-get-a-trial-experience-for-power-bi-embedded-in-azure"></a>Van lehetőség az Azure-beli Power BI Embedded kipróbálására?

Mivel a Power BI Embedded az Azure része, így használhatja ezt a szolgáltatást az [Azure-regisztráció során kapott 200 $ értékű kreditjéből](https://azure.microsoft.com/free/).

### <a name="is-power-bi-embedded-available-for-sovereign-clouds-us-government-germany-china"></a>Elérhető a Power BI Embedded a szuverén felhőkben (US Government, Németország, Kína)?

A Power BI Embedded csak bizonyos [szuverén felhőkben](embed-sample-for-customers-sovereign-clouds.md) érhető el. A kínai felhőben **nem**.

### <a name="is-power-bi-embedded-available-for-non-profits-and-educational"></a>Létezik non-profit vagy oktatási intézményeknek szánt Power BI Embedded?

A non-profit és oktatási intézmények megvásárolhatják az Azure-t. Nincs az Azure-ban különleges díjszabásunk az ilyen típusú ügyfeleink számára.

## <a name="power-bi-workspace-collection"></a>Power BI-munkaterületcsoport

### <a name="what-is-power-bi-workspace-collection"></a>Mi a Power BI-munkaterületcsoport?

A **Power BI-munkaterület-csoport** (a **Power BI Embedded** 1 verziója) egy olyan megoldás, amely a **Power BI-munkaterületcsoport** nevű Azure-erőforráson alapul. Ez a megoldás **Power BI Embedded**-alkalmazások létrehozását teszi lehetővé az ügyfelek részére a **Power BI-munkaterületcsoporton** belüli Power BI tartalmak, megoldások és dedikált API-k segítségével, valamint munkaterületcsoport-kulcsokkal az alkalmazás Power BI-ban történő hitelesítéséhez.

### <a name="can-i-migrate-from-power-bi-workspace-collection-to-power-bi-embedded"></a>Áttelepíthetem-e a Power BI-munkaterületcsoport tartalmait a Power BI Embeddedbe?

1. Az áttelepítési eszközzel klónozhatja a **Power BI-munkaterületcsoport** tartalmát a Power BI-ba – https://docs.microsoft.com/power-bi/developer/migrate-from-powerbi-embedded#content-migration.

2. Kezdje a Power BI-tartalmakat használó **Power BI Embedded** kísérleti (POC) alkalmazással.

3. Ha készen áll a munkára, szerezzen be dedikált kapacitást a **Power BI Embedded** használatához, és rendelje hozzá a saját Power BI-tartalmat (munkaállomást).

>[!Note]
Miközben párhuzamosan létrehozza a **Power BI Embedded** megoldást, tovább használhatja a **Power BI-munkaterületcsoportot** is. Miután elkészült, áttelepítheti az ügyfelet az új **Power BI Embedded** megoldásba, majd kivezetheti a **Power BI-munkaterületcsoportot**.

További információkért lásd: [Power BI-munkaterületcsoport tartalmainak áttelepítése a Power BI Embeddedbe](https://docs.microsoft.com/power-bi/developer/migrate-from-powerbi-embedded)

### <a name="is-power-bi-workspace-collection-on-a-path-to-be-deprecated"></a>Nemsokára elavul a Power BI-munkaterületcsoport?

Igen, de a  **Power BI-munkaterületcsoport** meglévő felhasználói tovább használhatják azt az elavulás időpontjáig. Az ügyfelek egyaránt létrehozhatnak új munkaterületcsoportokat és **Power BI-munkaterületcsoportot** még használó **Power BI Embedded**-megoldásokat is.

Ez azonban azzal jár, hogy a **Power BI-munkaterületcsoportokban** már nem jelennek meg új funkciók, és az ügyfeleknek érdemes lesz megtervezni a tartalmak áttelepítését a **Power BI Embedded** megoldásba.
### <a name="when-will-power-bi-workspace-collection-support-be-discontinued"></a>Mikor szűnik meg a Power BI-munkaterületcsoport támogatása?

A **Power BI-munkaterületcsoportot** használó ügyfelek 2018 június végéig, vagy a támogatási szerződésük lejártáig folytathatják a használatot.

### <a name="in-what-regions-can-pbi-workspace-collection-be-created"></a>Mely régiókban hozható létre a PBI-munkaterületcsoport?

Az elérhető régiók Délkelet-Ausztrália, Dél-Brazília, Közép-Kanada, az USA 2. keleti régiója, Kelet-Japán, az USA északi középső régiója, Észak-Európa, az USA déli középső régiója, Délkelet-Ázsia, az Egyesült Királyság déli régiója, Nyugat-Európa, Nyugat-India és az USA nyugati régiója.

### <a name="why-should-i-migrate-from-pbi-workspace-collection-to-power-bi-embedded"></a>Miért kell áttelepítenem a PBI-munkaterületcsoportot a Power BI Embeddedbe?

A **Power BI Embedded** megoldás olyan új funkciókkal és képességekkel rendelkezik, amelyek a **Power BI-munkaterületcsoportban** nem valósíthatók meg.

Néhány ilyen funkció:
* A PBI esetében minden adatforrás támogatott, szemben a **Power BI-munkaterületcsoport** 2 adatforrásával. 
* Számos új funkció, köztük a Q&A, a Frissítés, a könyvjelzők, az irányítópultok és csempék beágyazása és az egyéni menü csak a **Power BI Embedded** megoldásban támogatott.
* Kapacitás-számlázási modell.

További információ: [A beágyazott alkalmazás hibaelhárítása](embedded-troubleshoot.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)