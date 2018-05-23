---
title: Power BI-tartalom beágyazása alkalmazásokba szuverén felhőket használó ügyfelek számára
description: Ismerje meg, hogyan integrálhat vagy ágyazhat be egy irányítópultot, csempét vagy jelentést egy webalkalmazásba a Power BI API-kkal az ügyfelei számára.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 03/28/2018
ms.author: maghan
ms.openlocfilehash: 59f045d142fdf5ba22f9d240913687a9306e6b43
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
---
# <a name="embed-a-power-bi-dashboard-tile-or-report-into-your-application-for-sovereign-clouds"></a>Power BI-irányítópult, -csempe vagy -jelentés beágyazása az alkalmazásba szuverén felhők használata esetén
Ismerje meg, hogyan integrálhat vagy ágyazhat be egy irányítópultot, csempét vagy jelentést egy webalkalmazásba a Power BI .NET SDK-val és a Power BI JavaScript API-val, amikor az ügyfelei számára ágyaz be. Ez általában a független szoftverszállítóknál jellemző.

A Power BI a szuverén (privát) felhőket is támogatja. Minden egyes szuverén felhő saját szolgáltatással rendelkezik. A különböző szuverén felhők az alábbiak:

* Egyesült Államok Kormányzati közösségi felhő (GCC)

* Egyesült Államok Katonai alvállalkozók (DoDCON)

* Egyesült Államok Katonaság (DoD)

* A németországi felhőhöz készült Power BI

![Beágyazott irányítópult](media/embed-sample-for-customers/powerbi-embed-dashboard.png)

A bemutató megkezdéséhez **Power BI**-fiókra van szükség. Ha nincs beállított fiókja, a kormányzati típustól függően egy [egyesült államokbeli kormányzati Power BI-fiókot](../service-govus-signup.md) vagy egy [németországi felhőhöz készült Power BI-fiókot regisztrálhat](https://powerbi.microsoft.com/power-bi-germany/?ru=https%3A%2F%2Fapp.powerbi.de%2F%3FnoSignUpCheck%3D1).

> [!NOTE]
> A saját cégének szeretne irányítópultot beágyazni? Tekintse meg az [irányítópult céges alkalmazásba való integrálását](integrate-dashboard.md) ismertető cikket.
>

Egy irányítópult webalkalmazásba ágyaszásához használja a **Power BI** API-t, és egy Azure Active Directory (AD) engedélyezési **hozzáférési tokent** az irányítópult lekéréséhez. Ezután töltse be az irányítópultot egy beágyazási token használatával. A **Power BI** API szoftveres hozzáférést biztosít egyes **Power BI**-erőforrásokhoz. További információkat [A Power BI REST API áttekintése](https://msdn.microsoft.com/library/dn877544.aspx), a [Power BI .NET SDK](https://github.com/Microsoft/PowerBI-CSharp) és a [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript) cikkekben talál.

## <a name="download-the-sample"></a>A minta letöltése
Ez a cikk a GitHubon az [ügyfelek számára végzett beágyazási mintában](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data/PowerBIEmbedded_AppOwnsData) használt kódot mutatja be. A bemutató követéséhez letöltheti a mintát.

* Kormányzati közösségi felhő (GCC):
    1. Írja felül a Cloud.config fájlt a GCCCloud.config tartalmával.
    2. Frissítse a clientid (a natív alkalmazás ügyfél-azonosítója), a groupid, a user (a fő felhasználó) és a password (jelszó) paramétereit a Web.config fájlban.
    3. Az alábbiaknak megfelelően adja hozzá a GCC-paramétereket a web.config fájlhoz.

```xml
<add key="authorityUrl" value="https://login.windows.net/common/oauth2/authorize/" />

<add key="resourceUrl" value="https://analysis.usgovcloudapi.net/powerbi/api" />

<add key="apiUrl" value="https://api.powerbigov.us/" />

<add key="embedUrlBase" value="https://app.powerbigov.us" />
```

* Katonai alvállalkozók (DoDCON):
    1. Írja felül a Cloud.config fájlt a TBCloud.config tartalmával.
    2. Frissítse a clientid (a natív alkalmazás ügyfél-azonosítója), a groupid, a user (a fő felhasználó) és a password (jelszó) paramétereit a Web.config fájlban.
    3. Az alábbiaknak megfelelően adja hozzá a DoDCON-paramétereket a web.config fájlhoz.

```xml
<add key="authorityUrl" value="https://login.windows.net/common/oauth2/authorize/" />

<add key="resourceUrl" value="https://high.analysis.usgovcloudapi.net/powerbi/api" />

<add key="apiUrl" value="https://api.high.powerbigov.us/" />

<add key="embedUrlBase" value="https://app.high.powerbigov.us" />
```

* Katonaság (DoD):
    1. Írja felül a Cloud.config fájlt a PFCloud.config tartalmával.
    2. Frissítse a clientid (a natív alkalmazás ügyfél-azonosítója), a groupid, a user (a fő felhasználó) és a password (jelszó) paramétereit a Web.config fájlban.
    3. Az alábbiaknak megfelelően adja hozzá a DoDCON-paramétereket a web.config fájlhoz.

```xml
<add key="authorityUrl" value="https://login.windows.net/common/oauth2/authorize/" />

<add key="resourceUrl" value="https://mil.analysis.usgovcloudapi.net/powerbi/api" />

<add key="apiUrl" value="https://api.mil.powerbigov.us/" />

<add key="embedUrlBase" value="https://app.mil.powerbigov.us" />
```

* A németországi felhőhöz készült Power BI paraméterei
    1. Írja felül a Cloud.config fájlt a németországi felhőhöz készült Power BI tartalmával.
    2. Frissítse a clientid (a natív alkalmazás ügyfél-azonosítója), a groupid, a user (a fő felhasználó) és a password (jelszó) paramétereit a Web.config fájlban.
    3. Az alábbiaknak megfelelően adja hozzá a németországi felhőhöz készült Power BI paramétereit a web.config fájlhoz.

```xml
<add key="authorityUrl" value=https://login.microsoftonline.de/common/oauth2/authorize/" />

<add key="resourceUrl" value="https://analysis.cloudapi.de/powerbi/api" />

<add key="apiUrl" value="https://api.powerbi.de/" />

<add key="embedUrlBase" value="https://app.powerbi.de" />
```

## <a name="step-1---register-an-app-in-azure-ad"></a>1. lépés – alkalmazás regisztrálása az Azure AD-ben
A REST API-hívások indításához az alkalmazásokat regisztrálni kell az Azure AD-ben. További információt az [Azure AD alkalmazás regisztrálása Power BI-tartalmak beágyazásához](register-app.md) eljárást ismertető cikkben talál. Mivel különböző szuverén felhőszolgáltatások léteznek, különböző URL-címek használatával regisztrálhatja alkalmazását.

* Kormányzati közösségi felhő (GCC) – https://app.powerbigov.us/apps 

* Katonai alvállalkozók (DoDCON) – https://app.high.powerbigov.us/apps 

* Katonaság (DoD) – https://app.mil.powerbigov.us/apps

* A németországi felhőhöz készült Power BI – https://app.powerbi.de/apps

Ha letöltötte az [ügyfelek számára végzett beágyazási mintát](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data), használja a regisztráció után kapott **Ügyfél-azonosítót**, így a minta hitelesíthet az Azure AD-ben. A minta konfigurálásához módosítsa a **clientId** azonosítót a *web.config* fájlban.


## <a name="step-2---get-an-access-token-from-azure-ad"></a>2. lépés – hozzáférési token lekérése az Azure AD-ből
Az alkalmazásban először egy **hozzáférési tokent** kell beszereznie az Azure AD-ből, mielőtt hívásokat indíthatna a Power BI REST API-hoz. További információkért lásd [a felhasználók hitelesítésével és a Power BI-alkalmazáshoz Azure AD hozzáférési token beszerzésével](get-azuread-access-token.md) kapcsolatos cikket. Mivel különböző szuverén felhőszolgáltatások léteznek, különböző URL-címek használatával szerezheti be az alkalmazása hozzáférési jogkivonatát.

* Kormányzati közösségi felhő (GCC) – https://login.microsoftonline.com

* Katonai alvállalkozók (DoDCON) – http://login.microsoftonline.us

* Katonaság (DoD) – https://login.microsoftonline.us

* A németországi felhőhöz készült Power BI – https://login.microsoftonline.de

A **Controllers\HomeController.cs** fájlban lévő tartalomelem feladatokban láthat példát ilyen megoldásra.

## <a name="step-3---get-a-content-item"></a>3. lépés – tartalomelem lekérése
A Power BI-tartalom beágyazásához el kell végeznie néhány dolgot a megfelelő beágyazás biztosítása érdekében. Bár ezen lépések mindegyike elvégezhető közvetlenül a REST API-val, a mintaalkalmazás és az itt szereplő példák a .NET SDK-t használják.

### <a name="create-the-power-bi-client-with-your-access-token"></a>A Power BI-ügyfél létrehozása a hozzáférési tokennel
A hozzáférési tokennel érdemes létrehozni a Power BI-ügyfélobjektumot, amely lehetővé teszi a Power BI API-k használatát. Ehhez a hozzáférési tokent a *Microsoft.Rest.TokenCredentials* objektummal kell tördelni.

```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.Rest;
using Microsoft.PowerBI.Api.V2;

var tokenCredentials = new TokenCredentials(authenticationResult.AccessToken, "Bearer");

// Create a Power BI Client object. It will be used to call Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Your code to embed items.
}
```

### <a name="get-the-content-item-you-want-to-embed"></a>A beágyazni kívánt tartalomelem lekérése
A Power BI-ügyfélobjektummal kérje le a beágyazni kívánt elem hivatkozását. Irányítópultokat, csempéket vagy jelentéseket ágyazhat be. Itt láthat arra példát, hogyan kérhető le az első irányítópult, csempe vagy jelentés adott munkaterületről.

Ennek példája az [alkalmazás tulajdonában lévő adatok használatát ismertető mintában](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data) lévő **Controllers\HomeController.cs** fájlban érhető el.

**Irányítópultok**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// You will need to provide the GroupID where the dashboard resides.
ODataResponseListDashboard dashboards = client.Dashboards.GetDashboardsInGroup(GroupId);

// Get the first report in the group.
Dashboard dashboard = dashboards.Value.FirstOrDefault();
```

**Csempe**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// To retrieve the tile, you first need to retrieve the dashboard.

// You will need to provide the GroupID where the dashboard resides.
ODataResponseListDashboard dashboards = client.Dashboards.GetDashboardsInGroup(GroupId);

// Get the first report in the group.
Dashboard dashboard = dashboards.Value.FirstOrDefault();

// Get a list of tiles from a specific dashboard
ODataResponseListTile tiles = client.Dashboards.GetTilesInGroup(GroupId, dashboard.Id);

// Get the first tile in the group.
Tile tile = tiles.Value.FirstOrDefault();
```

**Jelentés**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// You will need to provide the GroupID where the dashboard resides.
ODataResponseListReport reports = client.Reports.GetReportsInGroupAsync(GroupId);

// Get the first report in the group.
Report report = reports.Value.FirstOrDefault();
```

### <a name="create-the-embed-token"></a>A beágyazási token létrehozása
Létre kell hozni egy beágyazási tokent, amely a JavaScript API-ból használható. A beágyazási token a beágyazott elemre jellemző. Ez azt jelenti, hogy amikor Power BI-tartalmat ágyaz be, mindig létre kell hoznia egy új beágyazási tokent. További információt (beleértve a használandó **hozzáférési szintet**) a [GenerateToken API-ban](https://msdn.microsoft.com/library/mt784614.aspx) talál.

> [!IMPORTANT]
> Mivel a beágyazási tokenek elsődlegesen fejlesztési és tesztelési célokra használhatók, a Power BI fő fiókja csak korlátozott mennyiségű tokent tud előállítani. Éles üzemi beágyazási helyzetekhez [kapacitást szükséges vásárolni](https://docs.microsoft.com/power-bi/developer/embedded-faq#technical). Kapacitásvásárlás esetén nincs korlátja a beágyazási tokenek előállításának.

Ennek példája a [céges beágyazási mintában](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data) lévő **Controllers\HomeController.cs** fájlban érhető el.

Ez feltételezi, hogy létrejött egy osztály az **EmbedConfig** és a **TileEmbedConfig** elemekhez. Ezek mintái a **Models\EmbedConfig.cs** és a **Models\TileEmbedConfig.cs** fájlban érhetők el.

**Irányítópult**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// Generate Embed Token.
var generateTokenRequestParameters = new GenerateTokenRequest(accessLevel: "view");
EmbedToken tokenResponse = client.Dashboards.GenerateTokenInGroup(GroupId, dashboard.Id, generateTokenRequestParameters);

// Generate Embed Configuration.
var embedConfig = new EmbedConfig()
{
    EmbedToken = tokenResponse,
    EmbedUrl = dashboard.EmbedUrl,
    Id = dashboard.Id
};
```

**Csempe**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// Generate Embed Token for a tile.
var generateTokenRequestParameters = new GenerateTokenRequest(accessLevel: "view");
EmbedToken tokenResponse = client.Tiles.GenerateTokenInGroup(GroupId, dashboard.Id, tile.Id, generateTokenRequestParameters);

// Generate Embed Configuration.
var embedConfig = new TileEmbedConfig()
{
    EmbedToken = tokenResponse,
    EmbedUrl = tile.EmbedUrl,
    Id = tile.Id,
    dashboardId = dashboard.Id
};
```

**Jelentés**

```csharp
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

// Generate Embed Token.
var generateTokenRequestParameters = new GenerateTokenRequest(accessLevel: "view");
EmbedToken tokenResponse = client.Reports.GenerateTokenInGroup(GroupId, report.Id, generateTokenRequestParameters);

// Generate Embed Configuration.
var embedConfig = new EmbedConfig()
{
    EmbedToken = tokenResponse,
    EmbedUrl = report.EmbedUrl,
    Id = report.Id
};
```
## <a name="step-4---load-an-item-using-javascript"></a>4. lépés – elem betöltése a JavaScript használatával
A JavaScript használatával egy irányítópultot tölthet be egy div elembe a weboldalon. A minta EmbedConfig/TileEmbedConfig modellt használ egy irányítópult, csempe vagy jelentés nézeteivel együtt. A JavaScript API használatának teljes mintájáért használhatja a [Microsoft Power BI Embedded mintát](https://microsoft.github.io/PowerBI-JavaScript/demo).

Ennek alkalmazásmintája a [céges beágyazási mintában](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data) érhető el.

**Views\Home\EmbedDashboard.cshtml**

```csharp
<script src="~/scripts/powerbi.js"></script>
<div id="dashboardContainer"></div>
<script>
    // Read embed application token from Model
    var accessToken = "@Model.EmbedToken.Token";

    // Read embed URL from Model
    var embedUrl = "@Html.Raw(Model.EmbedUrl)";

    // Read dashboard Id from Model
    var embedDashboardId = "@Model.Id";

    // Get models. models contains enums that can be used.
    var models = window['powerbi-client'].models;

    // Embed configuration used to describe the what and how to embed.
    // This object is used when calling powerbi.embed.
    // This also includes settings and options such as filters.
    // You can find more information at https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details.
    var config = {
        type: 'dashboard',
        tokenType: models.TokenType.Embed,
        accessToken: accessToken,
        embedUrl: embedUrl,
        id: embedDashboardId
    };

    // Get a reference to the embedded dashboard HTML element
    var dashboardContainer = $('#dashboardContainer')[0];

    // Embed the dashboard and display it within the div container.
    var dashboard = powerbi.embed(dashboardContainer, config);
</script>
```

**Views\Home\EmbedTile.cshtml**

```csharp
<script src="~/scripts/powerbi.js"></script>
<div id="tileContainer"></div>
<script>
    // Read embed application token from Model
    var accessToken = "@Model.EmbedToken.Token";

    // Read embed URL from Model
    var embedUrl = "@Html.Raw(Model.EmbedUrl)";

    // Read tile Id from Model
    var embedTileId = "@Model.Id";

    // Read dashboard Id from Model
    var embedDashboardeId = "@Model.dashboardId";

    // Get models. models contains enums that can be used.
    var models = window['powerbi-client'].models;

    // Embed configuration used to describe the what and how to embed.
    // This object is used when calling powerbi.embed.
    // This also includes settings and options such as filters.
    // You can find more information at https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details.
    var config = {
        type: 'tile',
        tokenType: models.TokenType.Embed,
        accessToken: accessToken,
        embedUrl: embedUrl,
        id: embedTileId,
        dashboardId: embedDashboardeId
    };

    // Get a reference to the embedded tile HTML element
    var tileContainer = $('#tileContainer')[0];

    // Embed the tile and display it within the div container.
    var tile = powerbi.embed(tileContainer, config);
</script>
```

**Views\Home\EmbedReport.cshtml**

```csharp
<script src="~/scripts/powerbi.js"></script>
<div id="reportContainer"></div>
<script>
    // Read embed application token from Model
    var accessToken = "@Model.EmbedToken.Token";

    // Read embed URL from Model
    var embedUrl = "@Html.Raw(Model.EmbedUrl)";

    // Read report Id from Model
    var embedReportId = "@Model.Id";

    // Get models. models contains enums that can be used.
    var models = window['powerbi-client'].models;

    // Embed configuration used to describe the what and how to embed.
    // This object is used when calling powerbi.embed.
    // This also includes settings and options such as filters.
    // You can find more information at https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details.
    var config = {
        type: 'report',
        tokenType: models.TokenType.Embed,
        accessToken: accessToken,
        embedUrl: embedUrl,
        id: embedReportId,
        permissions: models.Permissions.All,
        settings: {
            filterPaneEnabled: true,
            navContentPaneEnabled: true
        }
    };

    // Get a reference to the embedded report HTML element
    var reportContainer = $('#reportContainer')[0];

    // Embed the report and display it within the div container.
    var report = powerbi.embed(reportContainer, config);
</script>
```

## <a name="next-steps"></a>Következő lépések

* Egy mintaalkalmazás elérhető a GitHubon, hogy áttekinthesse. A fenti példák azon a mintán alapulnak. További információért tekintse meg a [céges beágyazási mintát](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data).
* További információ a JavaScript API-ról: [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript).
* További információ a németországi felhőhöz készült Power BI-ról: [A németországi felhőhöz készült Power BI – gyakori kérdések](https://docs.microsoft.com/power-bi/service-govde-faq)
* [Power BI-munkaterületcsoport tartalmainak migrálása a Power BI-ba](migrate-from-powerbi-embedded.md)

Korlátozások és megfontolandó szempontok
* A GCC-fiókok jelenleg csak a P és EM kapacitásokat támogatják

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)
