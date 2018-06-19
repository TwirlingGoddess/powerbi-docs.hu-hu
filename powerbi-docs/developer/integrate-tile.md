---
title: Power BI-csempe integrálása a szervezet egy alkalmazásába
description: 'Bemutató: csempe integrálása egy alkalmazásba, mintakód'
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 02/13/2018
ms.author: maghan
ms.openlocfilehash: afed2bc87e7e358d9ba02a465c43d223f6e7cba3
ms.sourcegitcommit: 8ee0ebd4d47a41108387d13a3bc3e7e2770cbeb8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34813779"
---
# <a name="integrate-a-tile-into-an-app-user-owns-data"></a>Csempe integrálása egy alkalmazásba (a felhasználó az adatok tulajdonosa)
Ismerje meg, hogyan integrálhat vagy ágyazhat be egy csempét egy webalkalmazásba REST API-hívásokkal és a Power BI JavaScript API-val, ha a szervezete számára ágyaz be.

![Beágyazott csempe a webalkalmazásban](media/integrate-tile/powerbi-embedded-tile.png)

Az útmutató megkezdéséhez egy **Power BI**-fiókra van szükség. Ha nincs fiókja, [regisztrálhat egy ingyenes Power BI-fiókot](../service-self-service-signup-for-power-bi.md), vagy létrehozhat saját [Azure Active Directory-bérlőt](create-an-azure-active-directory-tenant.md) tesztelési célra.

> [!NOTE]
> Inkább beágyazási tokennel szeretne csempét beágyazni az ügyfeleinek? Tekintse meg az [Irányítópult, csempe vagy jelentés beágyazása az alkalmazásba ügyfelek számára](embed-sample-for-customers.md) című cikket.
> 
> 

Egy csempe beágyazásához a webalkalmazásba használja a **Power BI** REST API-t vagy a Power BI C# SDK-t, valamint egy Azure Active Directory (AD) engedélyezési **hozzáférési tokent** a csempe lekéréséhez. Ezután töltse be a csempét ugyanezen hozzáférési token használatával. A **Power BI** API szoftveres hozzáférést biztosít egyes **Power BI**-erőforrásokhoz. További információt a [Power BI REST API](https://docs.microsoft.com/rest/api/power-bi/) és a [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript) című cikkekben talál.

## <a name="download-the-sample"></a>A minta letöltése
Ez a cikk a GitHubon, az [integrate-tile-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-tile-web-app) mintában használt kódot mutatja be. A bemutató követéséhez letöltheti a mintát.

## <a name="step-1---register-an-app-in-azure-ad"></a>1. lépés – alkalmazás regisztrálása az Azure AD-ben
A REST API-hívások indításához az alkalmazásokat regisztrálni kell az Azure AD-ben. További információkért lásd: [Azure AD alkalmazás regisztrálása Power BI-tartalmak beágyazásához](register-app.md).

Ha letöltötte az [integrate-tile-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-tile-web-app) mintát, használja a regisztráció után kapott **Ügyfél-azonosítót** és a **Titkos ügyfélkulcsot**, így a minta hitelesítheti magát az Azure AD-ben. A minta konfigurálásához módosítsa az **Ügyfél-azonosítót** és a **Titkos ügyfélkulcsot** a *cloud.config* fájlban.

![](media/integrate-tile/powerbi-embed-dashboard-register-app4.png)

## <a name="step-2---get-an-access-token-from-azure-ad"></a>2. lépés – hozzáférési token lekérése az Azure AD-ből
Az alkalmazásban először egy **hozzáférési tokent** kell beszereznie az Azure AD-ből, mielőtt hívásokat indíthatna a Power BI REST API-hoz. További információkért lásd [a felhasználók hitelesítésével és a Power BI-alkalmazáshoz Azure AD hozzáférési token beszerzésével](get-azuread-access-token.md) kapcsolatos cikket.

## <a name="step-3---get-a-tile"></a>3. lépés – csempe lekérése
A **Power BI**-csempe lekéréséhez használja a [Csempék lekérése](https://docs.microsoft.com/rest/api/power-bi/dashboards/gettiles) műveletet, amely a **Power BI**-csempék listáját kéri le egy adott irányítópultból. A csempék listájából lekérhet egy csempeazonosítót és egy beágyazási URL-t.

Először az irányítópult azonosítóját kell lekérni, mielőtt lekérné a csempét. Az irányítópult lehívásáról szóló további információért lásd: [Irányítópult integrálása alkalmazásba (a felhasználó az adatok tulajdonosa)](integrate-dashboard.md).

### <a name="get-tiles-using-an-access-token"></a>Csempék lekérése hozzáférési token használatával
A [2. lépésben](#step-2-get-an-access-token-from-azure-ad) lekért **hozzáférési token** segítségével meghívhatja a [Csempék lekérése](https://docs.microsoft.com/rest/api/power-bi/dashboards/gettiles) műveletet. A [Csempék lekérése](https://docs.microsoft.com/rest/api/power-bi/dashboards/gettiles) művelet csempék listáját adja vissza. A csempék listájából lekérhet egyetlen csempét. Alább látható egy teljes C# metódus a csempe lekéréséhez. 

A REST API-hívásához egy *Engedélyezési* fejlécet is meg kell adnia a *Tulajdonos {hozzáférési token}* formátumában.

#### <a name="get-tiles-with-the-rest-api"></a>Csempék lekérése a REST API-val
**Default.aspx.cs**

```
using Newtonsoft.Json;

//Get a tile from a dashboard. In this sample, you get the first tile.
protected void GetTile(string dashboardId, int index)
{
    //Configure tiles request
    System.Net.WebRequest request = System.Net.WebRequest.Create(
        String.Format("{0}Dashboards/{1}/Tiles",
        baseUri,
        dashboardId)) as System.Net.HttpWebRequest;

    request.Method = "GET";
    request.ContentLength = 0;
    request.Headers.Add("Authorization", String.Format("Bearer {0}", accessToken.Value));

    //Get tiles response from request.GetResponse()
    using (var response = request.GetResponse() as System.Net.HttpWebResponse)
    {
        //Get reader from response stream
        using (var reader = new System.IO.StreamReader(response.GetResponseStream()))
        {
            //Deserialize JSON string
            PBITiles tiles = JsonConvert.DeserializeObject<PBITiles>(reader.ReadToEnd());

            //Sample assumes at least one Dashboard with one Tile.
            //You could write an app that lists all tiles in a dashboard
            if (tiles.value.Length > 0)
                tileEmbedUrl.Text = tiles.value[index].embedUrl;
        }
    }
}

//Power BI Tiles used to deserialize the Get Tiles response.
public class PBITiles
{
    public PBITile[] value { get; set; }
}
public class PBITile
{
    public string id { get; set; }
    public string title { get; set; }
    public string embedUrl { get; set; }
}
```

#### <a name="get-tiles-using-the-net-sdk"></a>Csempék lekérése a .NET SDK használatával
A .NET SDK használatával lekérheti az irányítópultok listáját ahelyett, hogy közvetlenül a REST API-t hívná.

```
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

var tokenCredentials = new TokenCredentials(<ACCESS TOKEN>, "Bearer");

// Create a Power BI Client object. It will be used to call Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Get a list of dashboards your "My Workspace"
    ODataResponseListDashboard tiles = client.Dashboards.GetDashboards();

    // Get a list of dashboards from a group (app workspace)
    ODataResponseListDashboard dashboards = client.Dashboards.GetDashboardsInGroup(groupId);

    Dashboard dashboard = dashboards.Value.FirstOrDefault();

    // Get the first tile from the above dashbaord
    ODataResponseListTile tiles = client.Dashboards.GetTiles(dashboard.Id);

    Tile tile = tiles.Value.FirstOrDefault();
}
```

## <a name="step-4---load-a-tile-using-javascript"></a>4. lépés – csempe betöltése JavaScript használatával
A JavaScript használatával egy csempét tölthet be a div elembe a weblapon.

**Default.aspx**

```
<!-- Embed Tile-->
<div> 
    <asp:Panel ID="PanelEmbed" runat="server" Visible="true">
        <div>
            <div><b class="step">Step 3</b>: Embed a tile</div>

            <div>Enter an embed url for a tile from Step 2 (starts with https://):</div>
            <input type="text" id="tb_EmbedURL" style="width: 1024px;" />
            <br />
            <input type="button" id="bEmbedTileAction" value="Embed Tile" />
        </div>

        <div id="tileContainer"></div>
    </asp:Panel>
</div>
```

**Site.master**

```
window.onload = function () {
    // client side click to embed a selected tile.
    var el = document.getElementById("bEmbedTileAction");
    if (el.addEventListener) {
        el.addEventListener("click", updateEmbedTile, false);
    } else {
        el.attachEvent('onclick', updateEmbedTile);
    }

    // handle server side post backs, optimize for reload scenarios
    // show embedded tile if all fields were filled in.
    var accessTokenElement = document.getElementById('MainContent_accessTokenTextbox');
    if (accessTokenElement !== null) {
        var accessToken = accessTokenElement.value;
        if (accessToken !== "")
            updateEmbedTile();
    }
};

// update embed tile
function updateEmbedTile() {

    // check if the embed url was selected
    var embedUrl = document.getElementById('tb_EmbedURL').value;
    if (embedUrl === "")
        return;

    // get the access token.
    accessToken = document.getElementById('MainContent_accessTokenTextbox').value;

    // Embed configuration used to describe the what and how to embed.
    // This object is used when calling powerbi.embed.
    // You can find more information at https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details.
    var config = {
        type: 'tile',
        accessToken: accessToken,
        embedUrl: embedUrl
    };

    // Grab the reference to the div HTML element that will host the tile.
    var tileContainer = document.getElementById('tileContainer');

    // Embed the tile and display it within the div container.
    var tile = powerbi.embed(tileContainer, config);

    // tile.on will add an event handler which prints to Log window.
    tile.on("error", function (event) {
        var logView = document.getElementById('logView');
        logView.innerHTML = logView.innerHTML + "Error<br/>";
        logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
        logView.innerHTML = logView.innerHTML + "---------<br/>";
    });
}
```

Ha letöltötte és futtatta az [integrate-tile-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-tile-web-app) mintát, a minta az alább láthatóhoz fog hasonlítani.

![Beágyazott csempe a webalkalmazásban](media/integrate-tile/powerbi-embedded-tile.png)

## <a name="working-with-groups-app-workspaces"></a>A csoportok kezelése (alkalmazás-munkaterületek)
Egy csempe beágyazásához egy csoportból (alkalmazás-munkaterületről) le kell kérnie az egy csoport irányítópultján belül elérhető csempék listáját az alábbi REST API-hívás használatával. További információ erről a REST API-hívásról: [Csempék lekérése](https://docs.microsoft.com/rest/api/power-bi/dashboards/gettiles). A csoportban engedéllyel kell rendelkeznie, hogy a kérés eredményeket adjon vissza.

```
https://api.powerbi.com/v1.0/myorg/groups/{groupId}/dashboards/{dashboard_id}/tiles
```

A fenti API az elérhető csempék listáját adja vissza. Mindegyik csempe rendelkezik egy EmbedUrl-tulajdonsággal, amely a csoportbeágyazás támogatására lett létrehozva.

```
https://app.powerbi.com/embed?dashboardId={dashboard_id}&tileId={tile_id}&groupId={group_id}
```

## <a name="next-steps"></a>Következő lépések
[Csempe beágyazása](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Tile-Embed) a PowerBI-JavaScript wikijén

[Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript).

A [integrate-tile-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-tile-web-app) minta a GitHubon.

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

