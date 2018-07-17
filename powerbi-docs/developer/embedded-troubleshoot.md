---
title: Beágyazott alkalmazás hibaelhárítása
description: Ez a cikk azokat a gyakori problémákat ismerteti, amelyek Power BI-tartalmak beágyazása során merülhetnek fel.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 07/03/2018
ms.author: maghan
ms.openlocfilehash: b3c9599ea3ce01094bb75d9b036fb25b1ca7109a
ms.sourcegitcommit: 627918a704da793a45fed00cc57feced4a760395
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/10/2018
ms.locfileid: "37926559"
---
# <a name="troubleshooting-your-embedded-application"></a>Beágyazott alkalmazás hibaelhárítása

Ez a cikk azokat a gyakori problémákat ismerteti, amelyek Power BI-tartalmak beágyazása során merülhetnek fel.

## <a name="tools-for-troubleshooting"></a>Hibaelhárítási eszközök

### <a name="fiddler-trace"></a>Nyomon követés a Fiddlerrel

A [Fiddler](http://www.telerik.com/fiddler) a Telerik által kifejlesztett, HTTP-forgalmat figyelő ingyenes eszköz.  A Power BI API-k használatával megtekintheti a lekérdezések oda-vissza áramlását az ügyfélszámítógépen. Ebből kiderítheti az esetleges hibákat, illetve az egyéb kapcsolódó információkat.

![Nyomon követés a Fiddlerrel](../includes/media/gateway-onprem-tshoot-tools-include/fiddler.png)

### <a name="f12-in-browser-for-front-end-debugging"></a>F12 billentyű a böngészőben a kezelőfelületen történő hibakereséshez

Az F12 billentyű megnyitja a böngészőben a fejlesztői ablakot. Ezzel megtekintheti a hálózati forgalmat és az egyéb információkat.

![F12 billentyű a böngészőben történő hibakereséshez](media/embedded-troubleshoot/browser-f12.png)

### <a name="extracting-error-details-from-power-bi-response"></a>Hiba részleteinek kigyűjtése a Power BI-válaszból

Ez a kódrészlet azt mutatja be, hogyan lehet kigyűjteni a hiba részleteit egy HTTP-kivételből:

```
public static string GetExceptionText(this HttpOperationException exc)
{
    var errorText = string.Format("Request: {0}\r\nStatus: {1} ({2})\r\nResponse: {3}",
    exc.Request.Content, exc.Response.StatusCode, (int)exc.Response.StatusCode, exc.Response.Content);
    if (exc.Response.Headers.ContainsKey("RequestId"))
    {
        var requestId = exc.Response.Headers["RequestId"].FirstOrDefault();
        errorText += string.Format("\r\nRequestId: {0}", requestId);
    }

    return errorText;
}
```
Javasoljuk, hogy a kérelemazonosítókat (valamint hibakereséshez a hiba részleteit is) naplózza.
Ha a Microsoft támogatási szolgálatával lép kapcsolatba, kérjük, adja meg a kérelem azonosítóját is.

## <a name="app-registration"></a>Alkalmazásregisztráció

**Sikertelen alkalmazásregisztráció**

Ha hibaüzenetet tapasztal az Azure Portal vagy a Power BI alkalmazásregisztrációs oldalán, akkor az a megfelelő jogosultságok hiányára utal. Alkalmazások regisztrálásához rendszergazdának kell lennie az Azure AD-bérlőjében, vagy engedélyezni kell az alkalmazások regisztrációját a nem rendszergazdai felhasználók számára.

**Új alkalmazás regisztrációja során nem jelenik meg a Power BI szolgáltatás az Azure Portalon**

Legalább egy felhasználónak regisztrálni kell a Power BI-ra. Ha nem látja a **Power BI szolgáltatást** az API-listában, akkor egyetlen felhasználó sem regisztrált a Power BI-ra.

## <a name="rest-api"></a>REST API

**401-es értékkel visszatérő API-hívás**

A hiba további felderítéséhez szükség lehet a Fidlerre a forgalom rögzítéséhez. Előfordulhat, hogy a regisztrált alkalmazás nem rendelkezik a szükséges jogosultságok körével az Azure AD-n belül. Ellenőrizze az Azure Portalon, hogy megtalálhatók-e az alkalmazásregisztrációban az Azure AD-hez szükséges jogkörök.

**403-as értékkel visszatérő API-hívás**

A hiba további felderítéséhez szükség lehet a Fidlerre a forgalom rögzítéséhez. A 403-as hibát több tényező is okozhatja.

* A felhasználó túllépte a megosztási kapacitásban létrehozható beágyazási tokenek számát. Azure-kapacitást kell vásárolni a beágyazási tokenek létrehozásához, és a munkaterületet ehhez a kapacitáshoz kell rendelni. További információért lásd: [Power BI Embedded-kapacitás létrehozása az Azure Portalon](https://docs.microsoft.com/azure/power-bi-embedded/create-capacity).
* Lejárt az Azure AD-hitelesítési token.
* A hitelesített felhasználó nem tagja a csoportnak (alkalmazás-munkaterület).
* A hitelesített felhasználó nem a csoport rendszergazdája (alkalmazás-munkaterület).
* Az engedélyezési fejléc nem megfelelően szerepel. Ellenőrizze, hogy nincsenek-e benne elgépelések.

Lehet, hogy az alkalmazás háttérszolgáltatásának a GenerateToken-hívás előtt frissítenie kell a hitelesítési tokent.

```
    GET https://wabi-us-north-central-redirect.analysis.windows.net/metadata/cluster HTTP/1.1
    Host: wabi-us-north-central-redirect.analysis.windows.net
    ...
    Authorization: Bearer eyJ0eXAiOi...
    ...
 
    HTTP/1.1 403 Forbidden
    ...
     
    {"error":{"code":"TokenExpired","message":"Access token has expired, resubmit with a new access token"}}
```

## <a name="authentication"></a>Hitelesítés

### <a name="authentication-failed-with-aadsts70002-or-aadsts50053"></a>A hitelesítés nem sikerült: AADSTS70002 vagy AADSTS50053

**(AADSTS70002: Hiba történt a hitelesítő adatok ellenőrzésekor. AADSTS50053: Túl sokszor próbált bejelentkezni helytelen felhasználóazonosítóval vagy jelszóval)**

Ha Ön a Power BI Embedded szolgáltatást használja Azure AD közvetlen hitelesítéssel, és ehhez hasonló üzeneteket kap bejelentkezéskor: ***error:unauthorized_client,error_description:AADSTS70002, akkor hiba történt a hitelesítő adatok érvényesítésekor. AADSTS50053: Túl sokszor próbált bejelentkezni helytelen felhasználóazonosítóval vagy jelszóval***, ez azért van, mert a közvetlen hitelesítés 2018/06/14 dátummal ki lett kapcsolva.

Javasoljuk, használja az [Azure AD Conditional Access](https://cloudblogs.microsoft.com/enterprisemobility/2018/06/07/azure-ad-conditional-access-support-for-blocking-legacy-auth-is-in-public-preview/) (Azure AD feltételes hozzáférés) támogatását az elavult hitelesítések letiltására, vagy használja az [Azure AD Directory Pass-through Authentication](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect-pass-through-authentication) (Azure AD Directory átmenő hitelesítés) módszerét.

Azonban ennek visszakapcsolására is van lehetőség [Azure AD szabályzattal](https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/configure-authentication-for-federated-users-portal#enable-direct-authentication-for-legacy-applications), amelynek hatóköre lehet a cég vagy egy [szolgáltatásnév](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-application-objects#service-principal-object).

**_Javasoljuk, hogy ezt csak alkalmazásonként engedélyezze és csak a kerülő megoldásához szükséges mértékig._**

Ennek a szabályzatnak a létrehozásához **globális rendszergazdai** engedélyekre van szüksége ahhoz a könyvtárhoz, ahol létrehozza és hozzárendeli a szabályzatot. Itt látható egy mintaszkript a szabályzat létrehozásához és az SP-hez való hozzárendeléshez ennél az alkalmazásnál:

1. Telepítse az [Azure AD előzetes verziójának PowerShell-modulját](https://docs.microsoft.com/en-us/powershell/azure/active-directory/install-adv2?view=azureadps-2.0).

2. Futtassa a következő PowerShell-parancsokat soronként (győződjön meg róla, hogy a $sp változó nem kap egynél több alkalmazást eredményül).

```powershell
Connect-AzureAD
```

```powershell
$sp = Get-AzureADServicePrincipal -SearchString "Name_Of_Application"
```

```powershell
$policy = New-AzureADPolicy -Definition @("{`"HomeRealmDiscoveryPolicy`":{`"AllowCloudPasswordValidation`":true}}") -DisplayName EnableDirectAuth -Type HomeRealmDiscoveryPolicy -IsOrganizationDefault $false
```

```powershell
Add-AzureADServicePrincipalPolicy -Id $sp.ObjectId -RefObjectId $policy.Id 
```

A szabályzat hozzárendelése után várjon körülbelül 15–20 másodpercig a propagálásra a tesztelés előtt.

**A token generálása sikertelen a hatályos identitás megadásakor**

Megadott hatályos identitás esetén a GenerateToken-hívás sikertelenségét több tényező is okozhatja.

* Az adatkészlet nem támogatja a hatályos identitás használatát
* Nem adta meg a felhasználónevet
* Nem adta meg a szerepkört
* Nem adta meg a DatasetId-t
* A felhasználó nem rendelkezik megfelelő engedélyekkel

Ahhoz, hogy eldönthesse, melyik okozza a hibát, próbálja meg a következőket.

* Hajtsa végre az [adatkészlet lekérése](https://docs.microsoft.com/rest/api/power-bi/datasets) műveletet. Az IsEffectiveIdentityRequired tulajdonság true (igaz) értékű?
* A felhasználónév megadása minden EffectiveIdentity esetén kötelező.
* Ha az IsEffectiveIdentityRolesRequired true (igaz) értékű, akkor kötelező megadni a szerepkört.
* A DatasetId megadása minden EffectiveIdentity esetén kötelező.
* Az Analysis Serviceshez használt fő felhasználónak az átjáró rendszergazdájának kell lennie.

### <a name="aadsts90094-the-grant-requires-admin-permission"></a>AADSTS90094: A hozzájáruláshoz rendszergazdai engedély szükséges

**_Tünetek:_**</br>
Amikor egy rendszergazdai jogokkal nem rendelkező felhasználó először próbál bejelentkezni egy alkalmazásba és a hozzájárulását adja, a következő hibaüzenetet kapja:
* A ConsentTest folyamatnak olyan engedélyre van szüksége a cég erőforrásainak eléréséhez, amelyet csak egy rendszergazda adhat meg. Kérjen engedélyt a rendszergazdától az alkalmazáshoz, hogy használhassa azt.
* AADSTS90094: A hozzájáruláshoz rendszergazdai engedély szükséges.

    ![Hozzájárulás megadása – teszt](media/embedded-troubleshoot/consent-test-01.png)

Egy rendszergazdai jogú felhasználó be tud jelentkezni, és sikeresen meg tudja adni az engedélyt.

**_Alapvető ok:_**</br>
Felhasználói jóváhagyás le van tiltva a bérlő számára.

**_Többféle javítás lehetséges:_**

*Felhasználói beleegyezés engedélyezése a teljes bérlőnek (minden felhasználó, minden alkalmazás)*
1. Az Azure Portalon lépjen az „Azure Active Directory” => „Felhasználók és csoportok” => „Felhasználói beállítások” pontba
2. Engedélyezze „A felhasználók engedélyezhetik, hogy az alkalmazások a felhasználók nevében hozzáférjenek a vállalati adatokhoz” beállítást, és mentse a módosításokat

    ![Hozzájárulás megadásának javítása](media/embedded-troubleshoot/consent-test-02.png)

*Engedélyek adása rendszergazdaként* Adjon engedélyeket az alkalmazásnak rendszergazdaként – az egész bérlőhöz vagy egy meghatározott felhasználóhoz.

## <a name="data-sources"></a>Adatforrások

**A független szoftvergyártó eltérő hitelesítő adatokat szeretne használni ugyanahhoz az adatforráshoz**

Egy adatforrás egy fő felhasználóhoz csak egyetlen hitelesítő adattal rendelkezhet. Ha eltérő hitelesítő adatokra van szüksége, akkor hozzon létre további fő felhasználókat. Ezt követően rendelje hozzá a eltérő hitelesítési adatokat a fő felhasználó környezeteihez, majd ennek a felhasználónak az Azure AD-hitelesítési tokenje segítségével végezze el a beágyazást.

## <a name="content-rendering"></a>Tartalom megjelenítése

**A beágyazott tartalmak megjelenítése vagy használata sikertelen, vagy időtúllépés miatt megszakad**

Ellenőrizze, hogy a beágyazási token nem járt-e le. Ellenőrizze és frissítse a beágyazási token lejáratát. További információért tekintse meg a [Token frissítése JavaScript SDK használatával](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Refresh-token-using-JavaScript-SDK-example) című cikket.

**A jelentés vagy irányítópult nem tölt be**

Ha a felhasználó nem látja a jelentést vagy az irányítópultot, akkor ellenőrizze, hogy a jelentés vagy az irányítópult megfelelően betölt-e a powerbi.com-on. A jelentés vagy az irányítópult nem fog működni az alkalmazásban, ha nem tölt be a powerbi.com-on.

**A jelentés vagy irányítópult lassan működik**

Nyissa meg a fájlt a Power BI Desktopban vagy a powerbi.com-on, és ellenőrizze, hogy elfogadható-e a működése, hogy kizárhassa az alkalmazása vagy a beágyazási API-k hibáit.

## <a name="onboarding-experience-tool-for-embedding"></a>Előkészítési eszköz beágyazáshoz

Az [Előkészítési eszköz](https://aka.ms/embedsetup) használatával gyorsan letölthet egy mintaalkalmazást. Az alkalmazását ezután összehasonlíthatja a mintaalkalmazással.

### <a name="prerequisites"></a>Előfeltételek

Mielőtt használatba venné az előkészítési eszközt, ellenőrizze, hogy rendelkezik-e az összes szükséges előfeltétellel. Szükség van egy **Power BI Pro**-fiókra és egy **Microsoft Azure**-előfizetésre.

* Ha még nem regisztrált a **Power BI Pro** szolgáltatásra, a kezdés előtt [hozzon létre egy ingyenes próbaverziós fiókot](https://powerbi.microsoft.com/en-us/pricing/).
* Ha még nincs Azure-előfizetése, kezdés előtt hozzon létre egy [ingyenes fiókot](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* Állítson be egy saját [Azure Active Directory-bérlőt](create-an-azure-active-directory-tenant.md).
* Telepítse a [Visual Studio](https://www.visualstudio.com/) 2013-as vagy későbbi verzióját.

### <a name="common-issues"></a>Gyakori problémák

Az előkészítési eszköz tesztelésre való használatánál az alábbi gyakori problémák merülhetnek fel:

#### <a name="using-the-embed-for-your-customers-sample-application"></a>A Beágyazás az ügyfelek számára mintaalkalmazás használata

A **Beágyazás az ügyfelek számára** használatához mentse és csomagolja ki a *PowerBI-Developer-Samples.zip* fájlt. Nyissa meg a *PowerBI-Developer-Samples-master\App Owns Data* mappát, majd futtassa a *PowerBIEmbedded_AppOwnsData.sln* fájlt.

Az **Engedélyek megadása** kiválasztásánál (Engedélyek megadása lépés) az alábbi hiba jelentkezik:

    AADSTS70001: Application with identifier <client ID> was not found in the directory <directory ID>

A hiba elhárítható, ha bezárja az előugró ablakot, és néhány másodperc múlva újra próbálkozik. Ezt a műveletet esetenként többször is meg kell ismételni. Egy időintervallum miatt az alkalmazásregisztrációs folyamat nem tud befejeződni, amikor az elérhető külső API-k számára.

A mintaalkalmazás futtatásánál az alábbi hibaüzenet jelenik meg:

    Password is empty. Please fill password of Power BI username in web.config.

A hiba azért jelentkezik, mert a felhasználói jelszó az egyetlen érték, amely nem kerül be a mintaalkalmazásba. Nyissa meg a megoldásban a Web.config fájlt, és adja meg a jelszavát a pbiPassword mezőben.

#### <a name="using-the-embed-for-your-organization-sample-application"></a>A Beágyazás a cég számára mintaalkalmazás használata

A **Beágyazás a cég számára** használatához mentse és csomagolja ki a *PowerBI-Developer-Samples.zip* fájlt. Nyissa meg a *PowerBI-Developer-Samples-master\User Owns Data\integrate-report-web-app* mappát, és futtassa a *pbi-saas-embed-report.sln* fájlt.

A **Beágyazás a cég számára** mintaalkalmazás futtatásánál az alábbi hiba jelentkezik:

    AADSTS50011: The reply URL specified in the request does not match the reply URLs configured for the application: <client ID>

Ennek az az oka, hogy a webkiszolgáló alkalmazáshoz megadott átirányítási URL-cím más, mint a minta URL-cím. A mintaalkalmazás regisztrálásához használja a `http://localhost:13526/` címet átirányítási URL-ként.

Ha szerkeszteni szeretné a regisztrált alkalmazást, ismerje meg, hogyan lehet szerkeszteni az [AAD-ben regisztrált alkalmazást](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#updating-an-application), hogy az alkalmazás hozzáférhessen a webes API-khoz.

Ha a Power BI felhasználói profiljait vagy adatait szeretné szerkeszteni, olvassa el, hogyan szerkeszthetők a [Power BI-adatok](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts).

További információ: [Power BI Embedded – gyakori kérdések](embedded-faq.md).

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)