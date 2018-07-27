---
title: Power BI-irányítópultok, -jelentések és -csempék beágyazása
description: Megismerheti Power BI-tartalmak az alkalmazásba való beágyazásának lépéseit.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 05/25/2018
ms.author: maghan
ms.openlocfilehash: 6a19478e561edfb4398f9a128e284d3a7e43e9b6
ms.sourcegitcommit: efe6747614ff66b5a86af9677632c1fb535448b2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/19/2018
ms.locfileid: "39137944"
---
# <a name="embed-your-power-bi-dashboards-reports-and-tiles"></a>Power BI-irányítópultok, -jelentések és -csempék beágyazása

Megismerheti Power BI-tartalmak az alkalmazásba való beágyazásának lépéseit.

A Microsoft [bejelentette a Power BI Premiumot](https://powerbi.microsoft.com/blog/microsoft-accelerates-modern-bi-adoption-with-power-bi-premium/), egy új, kapacitásalapú licencelési modellt, amellyel a felhasználók rugalmasabban érhetik el, oszthatják meg és terjeszthetik a tartalmakat. Az ajánlat emellett növeli a Power BI szolgáltatás méretezhetőségét és teljesítményét. A Power BI Embedded is be lett jelentve, amely lehetővé teszi kapacitás létrehozását a Microsoft Azure-ban. A Power BI Embedded az alkalmazására és az ügyfeleire összpontosít. 

Ez a cikk a Power BI-tartalmaknak a szervezete és az ügyfelei számára történő beágyazásáról nyújt áttekintést. A lépések hasonlóak a két forgatókönyvben. Ábrafeliratok láthatóak, amikor egy lépés az ügyfelek számára végzett beágyazásra vonatkozik.

Ennek lehetővé tételéhez el kell végeznie néhány lépést az alkalmazással. Végigvesszük azokat a lépéseket, amelyek beágyazott tartalmak létrehozásához és az alkalmazásban való használatához szükségesek.

> [!NOTE]
> A Power BI API-k továbbra is csoportokként hivatkoznak az alkalmazás-munkaterületekre. Bármely csoportokra való utalás alkalmazás-munkaterületek használatát jelöli.

## <a name="step-1-setup-your-embedded-analytics-development-environment"></a>1. lépés: A beágyazott elemzési fejlesztési környezet beállítása

Mielőtt irányítópultokat és jelentéseket ágyazna be az alkalmazásba, győződjön meg arról, hogy a környezete be van állítva a beágyazás engedélyezéséhez. A beállítás részeként a következőket kell elvégeznie.

* [Győződjön meg arról, hogy rendelkezik Azure Active Directory-bérlővel](embedding-content.md#azureadtenant)
* [Hozza létre a Power BI Pro-fiókját](embedding-content.md#proaccount)
* [Alkalmazásregisztráció és engedélyek](embedding-content.md#appreg)
* [Alkalmazás-munkaterületek létrehozása](embedding-content.md#appws)
* [Jelentések létrehozása és feltöltése](embedding-content.md#createreports)

Használhatja az [Előkészítési eszközt](https://aka.ms/embedsetup), amellyel egyszerűen elvégezheti az első lépéseket, és letölthet egy mintaalkalmazást.

Válassza ki az Ön számára megfelelő megoldást:
* Amennyiben az [ügyfelei számára végez beágyazást](embedding.md#embedding-for-your-customers), irányítópultokat és jelentéseket ágyazhat be olyan felhasználók számára, akik nem rendelkeznek Power BI-fiókkal. Futtassa a [Beágyazás az ügyfelek számára](https://aka.ms/embedsetup/AppOwnsData) megoldást.
* A [Beágyazás a cég számra](embedding.md#embedding-for-your-organization) használatával kiterjesztheti a Power BI szolgáltatást. Futtassa a [Beágyazás a cég számára](https://aka.ms/embedsetup/UserOwnsData) megoldást.

Ha mégis a környezet manuális létrehozása mellett dönt, folytathatja az alábbiak szerint. 

> [!NOTE]
> Nincs szükség külön erre a célra elkülönített kapacitásra az alkalmazás fejlesztéséhez. Az alkalmazás fejlesztőinek Power BI Pro-licencre van szükségük.

### <a name="azureadtenant"></a>Azure Active Directory-bérlő

Egy Azure Active Directory- (Azure AD-) bérlőre van szüksége az elemeknek a Power BI-ból való beágyazásához. Ennek a bérlőnek legalább egy Power BI Pro-felhasználóval kell rendelkeznie. Egy Azure AD-alkalmazás meghatározására is szükség van a bérlőn belül. Használhat meglévő Azure AD-bérlőt, vagy létrehozhat egy újat kifejezetten beágyazáshoz.

El kell döntenie, milyen bérlőbeállítást használ az ügyfelek számára történő beágyazáshoz.

* A meglévő vállalati Power BI-bérlőt használja?
* Külön bérlőt használ az alkalmazáshoz?
* Külön bérlőt használ mindegyik ügyfélhez?

Ha nem szeretne meglévő bérlőt használni, létrehozhat egy új bérlőt az alkalmazáshoz, vagy egyet külön-külön mindegyik ügyfélhez. Ehhez tekintse meg az [Azure Active Directory-bérlő létrehozásával](create-an-azure-active-directory-tenant.md) vagy az [Azure Active Directory-bérlő beszerzésével](https://docs.microsoft.com/azure/active-directory/develop/active-directory-howto-tenant) kapcsolatos cikket.

### <a name="proaccount"></a>Power BI Pro felhasználói fiók létrehozása

Csak egy Power BI Pro-fiókra van szüksége a tartalmak beágyazásához. Azonban lehet, hogy több különféle felhasználót szeretne, akik megadott hozzáféréssel rendelkeznek bizonyos elemekhez. Az alábbiakban áttekintjük a bérlőn belüli lehetséges felhasználókat.

A következő fiókoknak kell létezniük a bérlőben Power BI Pro-licenccel. Power BI Pro-licencre van szükség a Power BI-n belüli alkalmazás-munkaterületek használatához.

#### <a name="an-organizationtenant-admin-user"></a>Szervezeti/bérlői rendszergazda felhasználó

A szervezeti/bérlői globális rendszergazdai felhasználót nem ajánlott az alkalmazás által az ügyfelek számára történő beágyazáshoz használt fiókként alkalmazni. Ennek az a célja, hogy minimálisra csökkentse az alkalmazásfiók bérlőn belüli hozzáférését. A rendszergazdai felhasználó a beágyazási célból létrehozott összes alkalmazás-munkaterület rendszergazdája kell, hogy legyen.

#### <a name="accounts-for-analysts-that-create-content"></a>Tartalomkészítő elemzők fiókjai

Több felhasználó is készíthet tartalmaz a Power BI-hoz. Külön Power BI Pro-fiókra van szükség minden olyan elemző számára, aki tartalmat készít és helyez üzembe a Power BI-ban.

#### <a name="an-application-master-user-account-for-embedding-for-your-customers"></a>Az alkalmazás *fő* felhasználói fiókja az ügyfelek számára történő beágyazáshoz

A fő fiók az alkalmazás által az ügyfelek számára történő beágyazáshoz használt fiók. Ez a forgatókönyv általában ISV-alkalmazásokra vonatkozik. A fő fiók az egyetlen kötelező fiók a szervezeten belül. Rendszergazdai és elemzői fiókként is használható, de ez nem ajánlott. Az alkalmazás háttérrendszere tárolja ezen fiók hitelesítő adatait, és ezekkel szerez be Azure AD-hitelesítési jogkivonatot a Power BI API-khoz. Ez a fiók létrehoz egy beágyazási jogkivonatot az alkalmazás számára az ügyfelekhez való használatra.

A fő fiók egyszerűen egy Power BI Pro-licenccel rendelkező normál felhasználó, amelyet az alkalmazással használhat. A fióknak a beágyazáshoz használt alkalmazás-munkaterület rendszergazdájának kell lennie.

### <a name="appreg"></a> Alkalmazásregisztráció és engedélyek

A REST API-hívások indításához az alkalmazásokat regisztrálni kell az Azure AD-ben. További információt az [Azure AD alkalmazás regisztrálása Power BI-tartalmak beágyazásához](register-app.md) eljárást ismertető cikkben talál.

### <a name="appws"></a>Alkalmazás-munkaterületek létrehozása

Ha irányítópultokat és jelentéseket ágyaz be az ügyfelek számára, akkor ezeket az irányítópultokat és jelentéseket egy alkalmazás-munkaterületre kell helyezni. A fentiekben említett *fő* fióknak az alkalmazás-munkaterület rendszergazdájának kell lennie.

[!INCLUDE [powerbi-service-create-app-workspace](../includes/powerbi-service-create-app-workspace.md)]

> [!NOTE]
> Egy nem rendszergazdai felhasználó legfeljebb 250 munkaterületet hozhat létre. Több alkalmazás-munkaterület létrehozásához egy bérlői rendszergazdai fiókot kell használnia.
>

### <a name="createreports"></a>Jelentések létrehozása és feltöltése

A Power BI Desktop segítségével létrehozhatja jelentéseit és adatkészleteit, majd közzéteheti ezeket a jelentéseket egy alkalmazás-munkaterületen. A jelentéseket közzétevő végfelhasználónak Power BI Pro-licencre van szüksége az alkalmazás-munkaterületen történő közzétételhez.

## <a name="step-2-embed-your-content"></a>2. lépés: A tartalmak beágyazása

Az alkalmazásban hitelesítést kell végeznie a Power BI-jal. Ha az ügyfelei számára ágyaz be tartalmat, a *fő* fiók hitelesítő adatait az alkalmazáson belül tárolja.

> [!NOTE]
> Az ügyfelek számára történő beágyazás közbeni felhasználóhitelesítéssel kapcsolatban további információkért tekintse meg [a felhasználók hitelesítésével és a Power BI-alkalmazáshoz Azure AD hozzáférési token beszerzésével](get-azuread-access-token.md) kapcsolatos cikket.
>

A hitelesítés után az alkalmazáson belül a Power BI REST API-kkal és a JavaScript API-kkal ágyazhat be irányítópultokat és jelentéseket az alkalmazásba. 

Ha a **cége számára végez beágyazást**, tekintse át a következő útmutatót:

* [Jelentés integrálása egy alkalmazásba](embed-sample-for-your-organization.md)

Ha az **ügyfelei számára végez beágyazást**, ami gyakran előfordul ISV-k esetén, tekintse át a következőket:

* [Jelentés beágyazása az alkalmazásba](embed-sample-for-customers.md)

Amikor ügyfelek számára végez beágyazást, beágyazási tokenre van szükség. További információ: [Embed Token](https://docs.microsoft.com/rest/api/power-bi/embedtoken) (Jogkivonat beágyazása).

## <a name="step-3-promote-your-solution-to-production"></a>3. lépés: A megoldás előléptetése éles környezetbe

Néhány további lépés szükséges, ha át szeretne állni éles környezetre.

### <a name="embedding-for-your-organization"></a>Beágyazás a szervezet számára

Ha a szervezete számára végez beágyazást, csak azt kell tudatnia másokkal, hogyan érhetik el az alkalmazását. 

A hozzájuk rendelt licenc típusától függetlenül minden felhasználó használhat alkalmazás-munkaterületről (csoportból) beágyazott tartalmakat, ha a munkaterület elkülönített kapacitással rendelkezik. Ehhez hozzá kell adnia minden olyan felhasználót az alkalmazás-munkaterülethez, aki nem rendelkezik Power BI Pro-licenccel, különben 401-es, jogosulatlan hozzáférést jelző hibát kap. A következő táblázat az Office 365-ben elérhető Power BI Premium-termékváltozatokat sorolja fel.

| Kapacitási csomópont | Magok száma összesen<br/>*(Háttérrendszer + előtérrendszer)* | Háttérrendszerbeli magok | Előtérrendszerbeli magok | DirectQuery-/élő kapcsolat korlátai | Maximális oldalmegjelenítések óránként csúcsidőszakban |
| --- | --- | --- | --- | --- | --- |
| EM3 |4 virtuális mag |2 mag, 10 GB RAM |2 mag | |601-1,200 |
| P1 |8 virtuális mag |4 mag, 25 GB RAM |4 mag |Másodpercenként 30 |1,201-2,400 |
| P2 |16 virtuális mag |8 mag, 50 GB RAM |8 mag |Másodpercenként 60 |2,401-4,800 |
| P3 |32 virtuális mag |16 mag, 100 GB RAM |16 mag |Másodpercenként 120 |4801-9600 |

> [!NOTE]
> Globális vagy számlázási rendszergazdának kell lennie a bérlőn belül a Power BI Premium megvásárlásához. A Power BI Premium megvásárlásával kapcsolatos további tudnivalókért lásd [a Power BI Premium megvásárlásának menetét](../service-admin-premium-purchase.md) ismertető cikket.

>[!Note]
>[Állítsa be a beágyazott analitikai környezetet a szervezet számára.](#step-1-setup-your-embedded-analytics-development-environment)
>

### <a name="embedding-for-your-customers"></a>Beágyazás ügyfelek számára

Ha az ügyfelek számára végez beágyazást, a következőket érdemes elvégeznie.

* Ha külön bérlőt használ a fejlesztéshez, győződjön meg arról, hogy az alkalmazás-munkaterületek az irányítópultokkal és a jelentésekkel együtt elérhetők az éles környezetben. Győződjön meg arról, hogy az Azure AD-ban az éles környezetbeli bérlőhöz létrehozta az alkalmazást és hozzárendelte az 1. lépésben jelzett megfelelő alkalmazásengedélyeket.
* Vásároljon az igényeinek megfelelő kapacitást. Az alábbi táblázatból megtudhatja, milyen kapacitású Power BI Embedded-termékváltozatra van szüksége. További részletekért tekintse meg az [Embedded elemzési kapacitásának tervezésével kapcsolatos tanulmányt](https://aka.ms/pbiewhitepaper). Amikor készen áll a vásárlásra, azt a [Microsoft Azure Portalon](https://portal.azure.com) teheti meg. A Power BI Embedded-kapacitások létrehozásával kapcsolatos részletekért lásd a [Power BI Embedded-kapacitás az Azure Portalon való létrehozásával](https://docs.microsoft.com/azure/power-bi-embedded/create-capacity) kapcsolatos cikket.

> [!IMPORTANT]
> Mivel a beágyazási tokenek elsődlegesen fejlesztési és tesztelési célokra használhatók, a Power BI fő fiókja csak korlátozott mennyiségű tokent tud előállítani. Éles üzemi beágyazási helyzetekhez [kapacitást szükséges vásárolni](https://docs.microsoft.com/power-bi/developer/embedded-faq#technical). Elkülönített kapacitás vásárlása esetén nincs korlátja a beágyazási tokenek előállításának. Az elhasznált ingyenes beágyazási tokenek számának megtekintéséhez lépjen az [s](https://docs.microsoft.com/rest/api/power-bi/availablefeatures) (Elérhető funkciók) weblapra.

| Kapacitáscsomópont | Magok száma összesen<br/>*(Háttérrendszer + előtérrendszer)* | Háttérrendszerbeli magok | Előtérrendszerbeli magok | DirectQuery-/élő kapcsolat korlátai | Maximális oldalmegjelenítések óránként csúcsidőszakban |
| --- | --- | --- | --- | --- | --- |
| A1 |1 virtuális mag |0,5 mag, 3 GB RAM |0,5 mag | Másodpercenként 5 |1-300 |
| A2 |2 virtuális mag |1 mag, 5 GB RAM |1 mag | Másodpercenként 10 |301-600 |
| A3 |4 virtuális mag |2 mag, 10 GB RAM |2 mag | Másodpercenként 15 |601-1200 |
| A4 |8 virtuális mag |4 mag, 25 GB RAM |4 mag |Másodpercenként 30 |1,201-2,400 |
| A5 |16 virtuális mag |8 mag, 50 GB RAM |8 mag |Másodpercenként 60 |2,401-4,800 |
| A6 |32 virtuális mag |16 mag, 100 GB RAM |16 mag |Másodpercenként 120 |4801-9600 |

* Az alkalmazás-munkaterületet a Speciális felületen módosíthatja és rendelheti hozzá erre a célra elkülönített kapacitáshoz.

    ![Alkalmazás-munkaterület hozzárendelése kapacitáshoz](media/embedding-content/powerbi-embedded-premium-capacity.png)

* Helyezze üzembe a frissített alkalmazást az éles környezetben, és kezdje meg a Power BI-irányítópultok és -jelentések beágyazását.

>[!Note]
>[Állítsa be a beágyazott analitikai környezetet az ügyfelek számára.](#step-1-setup-your-embedded-analytics-development-environment) 
>

## <a name="admin-settings"></a>Rendszergazdai beállítások

A globális rendszergazdák vagy a Power BI szolgáltatás-rendszergazdái be- és kikapcsolhatják a REST API-k használatának képességét a bérlők esetében. A Power BI-rendszergazdák a teljes szervezethez vagy egyes biztonsági csoportokhoz is megadhatják ezt a beállítást. A beállítás alapértelmezés szerint a teljes szervezethez engedélyezve van. Ez a [Power BI felügyeleti portálján](../service-admin-portal.md) végezhető el.

## <a name="next-steps"></a>További lépések

[Beágyazás a Power BI szolgáltatással](embedding.md)  
[Power BI Embedded-munkaterületcsoport tartalmainak migrálása a Power BI-ba](migrate-from-powerbi-embedded.md)  
[Power BI Premium – pontosan mi is ez?](../service-premium.md)  
[A Power BI Premium megvásárlása](../service-admin-premium-purchase.md)  
[JavaScript API Git-adattár](https://github.com/Microsoft/PowerBI-JavaScript)  
[Power BI C# Git-adattár](https://github.com/Microsoft/PowerBI-CSharp)  
[JavaScript beágyazási minta](https://microsoft.github.io/PowerBI-JavaScript/demo/)  
[Embedded elemzési kapacitásának tervezésével kapcsolatos tanulmány](https://aka.ms/pbiewhitepaper)  
[Power BI Premium-tanulmány](https://aka.ms/pbipremiumwhitepaper)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)