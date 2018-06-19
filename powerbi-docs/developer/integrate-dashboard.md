---
title: Irányítópult integrálása a cég egy alkalmazásába
description: Ismerje meg, hogyan integrálhat vagy ágyazhat be egy irányítópultot egy webalkalmazásba a Power BI API-kkal.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 02/13/2018
ms.author: maghan
ms.openlocfilehash: dd7276eb436dfd9d842930f6a2c550a2a6b521f3
ms.sourcegitcommit: 8ee0ebd4d47a41108387d13a3bc3e7e2770cbeb8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34812951"
---
# <a name="integrate-a-dashboard-into-an-app-for-your-organization"></a>Irányítópult integrálása a cég egy alkalmazásába
Ismerje meg, hogyan integrálhat vagy ágyazhat be egy irányítópultot egy webalkalmazásba a REST API-hívásokkal és a Power BI JavaScript API-val együtt, ha a cége számára ágyaz be.

![Beágyazott irányítópult](media/integrate-dashboard/powerbi-embed-dashboard.png)

A bemutató megkezdéséhez egy **Power BI**-fiókra van szükség. Ha nincs fiókja, [regisztrálhat egy ingyenes Power BI-fiókot](../service-self-service-signup-for-power-bi.md), vagy létrehozhat saját [Azure Active Directory-bérlőt](create-an-azure-active-directory-tenant.md) tesztelési célra.

> [!NOTE]
> Inkább beágyazási tokennel szeretne irányítópultot beágyazni az ügyfeleinek? Tekintse meg az [Irányítópult, csempe vagy jelentés beágyazása az alkalmazásba ügyfelek számára](embed-sample-for-customers.md) című cikket.
> 
> 

Egy irányítópult beágyazásához a webalkalmazásba, használja a **Power BI** REST API-t, vagy a Power BI C# SDK-t, és egy Azure Active Directory (AD) engedélyezési **hozzáférési tokent** az irányítópult lekéréséhez. Ezután töltse be az irányítópultot ugyanezen hozzáférési token használatával. A **Power BI** API szoftveres hozzáférést biztosít egyes **Power BI**-erőforrásokhoz. További információt a [Power BI REST API](https://docs.microsoft.com/rest/api/power-bi/) és a [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript) című cikkekben talál.

## <a name="download-the-sample"></a>A minta letöltése
Ez a cikk a GitHubon, az [integrate-dashboard-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-dashboard-web-app) mintában használt kódot mutatja be. A bemutató követéséhez letöltheti a mintát.

## <a name="step-1---register-an-app-in-azure-ad"></a>1. lépés – alkalmazás regisztrálása az Azure AD-ben
A REST API-hívások indításához az alkalmazásokat regisztrálni kell az Azure AD-ben. További információt az [Azure AD alkalmazás regisztrálása Power BI-tartalmak beágyazásához](register-app.md) eljárást ismertető cikkben talál.

Ha letöltötte az [irányítópult integrálását bemutató mintát](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-dashboard-web-app), használja a regisztráció után kapott **ügyfél-azonosítót** és a **titkos ügyfélkódot**, így a minta hitelesítheti magát Azure AD-ben. A minta konfigurálásához módosítsa az **ügyfél-azonosítót** és a **titkos ügyfélkódot** a *cloud.config* fájlban.

![](media/integrate-dashboard/powerbi-embed-dashboard-register-app4.png)

## <a name="step-2---get-an-access-token-from-azure-ad"></a>2. lépés – hozzáférési token lekérése az Azure AD-ből
Az alkalmazásban először egy **hozzáférési tokent** kell beszereznie az Azure AD-ből, mielőtt hívásokat indíthatna a Power BI REST API-hoz. További információkért lásd [a felhasználók hitelesítésével és a Power BI-alkalmazáshoz Azure AD hozzáférési token beszerzésével](get-azuread-access-token.md) kapcsolatos cikket.

## <a name="step-3---get-a-dashboard"></a>3. lépés – irányítópult beszerzése
A **Power BI** irányítópult beszerzéséhez használja a [Get Dashboards](https://docs.microsoft.com/rest/api/power-bi/dashboards/getdashboards) műveletet, amely a **Power BI** irányítópultok listáját kéri le. Az irányítópultok listájából lekérheti az irányítópultok azonosítóit.

![](media/integrate-dashboard/powerbi-embed-dashboard-get-dashboards.png)

### <a name="get-dashboards-using-an-access-token"></a>Irányítópultok beszerzése hozzáférési token használatával
A [2. lépésben](#step-2-get-an-access-token-from-azure-ad) lekért **hozzáférési token** segítségével meghívhatja a [Get Dashboards](https://docs.microsoft.com/rest/api/power-bi/dashboards/getdashboards) műveletet. A [Get Dashboards](https://docs.microsoft.com/rest/api/power-bi/dashboards/getdashboards) művelet az irányítópultok listáját adja vissza. Az irányítópultok listájából lekérhet egyetlen irányítópultot is. Alul látható egy teljes C# metódus az irányítópult beszerzéséhez. 

A REST API-hívásához egy *Engedélyezési* fejlécet is meg kell adnia a *Tulajdonos {hozzáférési token}* formátumában.

#### <a name="get-dashboards-with-the-rest-api"></a>Irányítópultok beszerzése a REST API-val
**Default.aspx.cs**

```
protected void getDashboardsButton_Click(object sender, EventArgs e)
{
    string responseContent = string.Empty;

    //Configure dashboards request
    System.Net.WebRequest request = System.Net.WebRequest.Create(String.Format("{0}dashboards", baseUri)) as System.Net.HttpWebRequest;
    request.Method = "GET";
    request.ContentLength = 0;
    request.Headers.Add("Authorization", String.Format("Bearer {0}", authResult.AccessToken));

    //Get dashboards response from request.GetResponse()
    using (var response = request.GetResponse() as System.Net.HttpWebResponse)
    {
        //Get reader from response stream
        using (var reader = new System.IO.StreamReader(response.GetResponseStream()))
        {
            responseContent = reader.ReadToEnd();

            //Deserialize JSON string
            PBIDashboards PBIDashboards = JsonConvert.DeserializeObject<PBIDashboards>(responseContent);

            if (PBIDashboards != null)
            {
                var gridViewDashboards = PBIDashboards.value.Select(dashboard => new {
                    Id = dashboard.id,
                    DisplayName = dashboard.displayName,
                    EmbedUrl = dashboard.embedUrl
                });

                this.GridView1.DataSource = gridViewDashboards;
                this.GridView1.DataBind();
            }
        }
    }
}

//Power BI Dashboards used to deserialize the Get Dashboards response.
public class PBIDashboards
{
    public PBIDashboard[] value { get; set; }
}
public class PBIDashboard
{
    public string id { get; set; }
    public string displayName { get; set; }
    public string embedUrl { get; set; }
    public bool isReadOnly { get; set; }
}
```

#### <a name="get-dashboards-using-the-net-sdk"></a>Irányítópultok beszerzése a .NET SDK használatával
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
    ODataResponseListDashboard dashboards = client.Dashboards.GetDashboards();

    // Get a list of dashboards from a group (app workspace)
    ODataResponseListDashboard dashboards = client.Dashboards.GetDashboardsInGroup(groupId);

    Dashboard dashboard = dashboards.Value.FirstOrDefault();

    var embedUrl = dashboard.EmbedUrl
}
```

## <a name="step-4---load-a-dashboard-using-javascript"></a>4. lépés – irányítópult betöltése a JavaScript használatával
A JavaScript használatával egy irányítópultot tölthet be egy div elembe a weboldalon.

**Default.aspx**

```
<!-- Embed Dashboard-->
<div> 
    <asp:Panel ID="PanelEmbed" runat="server" Visible="true">
        <div>
            <div><b class="step">Step 3</b>: Embed a dashboard</div>

            <div>Enter an embed url for a dashboard from Step 2 (starts with https://):</div>
            <input type="text" id="tb_EmbedURL" style="width: 1024px;" />
            <br />
            <input type="button" id="bEmbedDashboardAction" value="Embed Dashboard" />
        </div>

        <div id="dashboardContainer"></div>
    </asp:Panel>
</div>
```

**Site.master**

```
window.onload = function () {
    // client side click to embed a selected dashboard.
    var el = document.getElementById("bEmbedDashboardAction");
    if (el.addEventListener) {
        el.addEventListener("click", updateEmbedDashboard, false);
    } else {
        el.attachEvent('onclick', updateEmbedDashboard);
    }

    // handle server side post backs, optimize for reload scenarios
    // show embedded dashboard if all fields were filled in.
    var accessTokenElement = document.getElementById('MainContent_accessTokenTextbox');
    if (accessTokenElement !== null) {
        var accessToken = accessTokenElement.value;
        if (accessToken !== "")
            updateEmbedDashboard();
    }
};

// update embed dashboard
function updateEmbedDashboard() {

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
        type: 'dashboard',
        accessToken: accessToken,
        embedUrl: embedUrl
    };

    // Grab the reference to the div HTML element that will host the dashboard.
    var dashboardContainer = document.getElementById('dashboardContainer');

    // Embed the dashboard and display it within the div container.
    var dashboard = powerbi.embed(dashboardContainer, config);

    // dashboard.on will add an event handler which prints to Log window.
    dashboard.on("tileClicked", function (event) {
        var logView = document.getElementById('logView');
        logView.innerHTML = logView.innerHTML + "Tile Clicked<br/>";
        logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
        logView.innerHTML = logView.innerHTML + "---------<br/>";
    });

    // dashboard.on will add an event handler which prints to Log window.
    dashboard.on("error", function (event) {
        var logView = document.getElementById('logView');
        logView.innerHTML = logView.innerHTML + "Error<br/>";
        logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
        logView.innerHTML = logView.innerHTML + "---------<br/>";
    });
}
```

Ha letöltötte és futtatta az [irányítópult integrálását ismertető mintát](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-dashboard-web-app), a minta a lent láthatóhoz fog hasonlítani.

![](media/integrate-dashboard/powerbi-embed-dashboard.png)

## <a name="tile-clicked-events"></a>Csempére kattintás események
A fenti mintában talán már észrevette, hogy kezelheti azokat az eseményeket, amikor egy felhasználó rákattint a csempére az irányítópulton. További információk az eseményekről: [Események kezelése a JavaScript API-ban](https://github.com/Microsoft/PowerBI-JavaScript/wiki/Handling-Events).

```
// dashboard.on will add an event handler which prints to Log window.
dashboard.on("tileClicked", function (event) {
    var logView = document.getElementById('logView');
    logView.innerHTML = logView.innerHTML + "Tile Clicked<br/>";
    logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
    logView.innerHTML = logView.innerHTML + "---------<br/>";
});

// dashboard.on will add an event handler which prints to Log window.
dashboard.on("error", function (event) {
    var logView = document.getElementById('logView');
    logView.innerHTML = logView.innerHTML + "Error<br/>";
    logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
    logView.innerHTML = logView.innerHTML + "---------<br/>";
});
```

Ha letöltötte és futtatta az [irányítópult integrálását ismertető mintát](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/PowerBI.com%20Integrate/integrate-dashboard-web-app), és valaki rákattint egy csempére, egy szöveg jelenik meg az irányítópult alatt. A szöveg a következőhöz fog hasonlítani. Ez lehetővé teszi, hogy naplózza, amikor valaki rákattint egy csempére, és a megfelelő helyre irányítsa a felhasználót.

```
Tile Clicked
{ "event": "TileClick", "reportEmbedUrl": "", "navigationUrl": "https://app.powerbi.com/dashboards/fcff76f9-15ff-4a8e-8242-275ac9c25b90/qna?q=count%20of%20new%20hires%20from%20July%202014%20to%20December%202014", "tileId": "0e99b45c-9b53-4920-b239-cee7d37d2369" }
---------
Tile Clicked
{ "event": "TileClick", "reportEmbedUrl": "https://app.powerbi.com/reportEmbed?reportId=ab199308-80b1-4626-9823-43a84623bd9c", "navigationUrl": "https://app.powerbi.com/reports/ab199308-80b1-4626-9823-43a84623bd9c/ReportSection1", "tileId": "ffc30447-674a-4511-944f-79e182d719de", "pageName": "ReportSection1" }
---------
```

## <a name="working-with-groups-app-workspaces"></a>A csoportok kezelése (alkalmazás-munkaterületek)
Az irányítópultok csoportokból (alkalmazás-munkaterületről) végzett beágyazásához be kell szereznie a csoportban elérhető irányítópultok listáját az alábbi REST API-hívás használatával. Erről a REST API-hívásról további információt a [Get Dashboards](https://docs.microsoft.com/rest/api/power-bi/dashboards/getdashboards) hívás leírásában talál. A csoportban engedéllyel kell rendelkeznie, hogy a kérés eredményeket adjon vissza.

```
https://api.powerbi.com/v1.0/myorg/groups/{groupId}/dashboards
```

A fenti API az elérhető irányítópultok listáját adja vissza. Mindegyik irányítópult rendelkezik egy EmbedUrl tulajdonsággal, amelyet a csoportbeágyazás támogatására hoztak létre.

```
https://app.powerbi.com/dashboardEmbed?dashboardId={dashboardId}&groupId={groupId}
```

## <a name="limitations"></a>Korlátozások
* A beágyazott irányítópultokhoz hozzáférő végfelhasználóknak rendelkezniük kell egy Power BI-fiókkal, valamint hozzáféréssel az irányítópulthoz. Ehhez az szükséges, hogy a felhasználó legyen az irányítópult tulajdonosa, vagy valaki megossza vele az irányítópultot.
* A beágyazott irányítópultok jelenleg nem támogatják a Kérdések és válaszok szolgáltatást.
* Ideiglenes korlátozásként, biztonsági csoportokkal rendelkező irányítópultok megosztásakor a felhasználónak először meg kell nyitnia az irányítópultokat a PowerBI.com webhelyen, mielőtt láthatná a beágyazott változatukat.

## <a name="next-steps"></a>Következő lépések
Egy mintaalkalmazás elérhető a GitHubon, hogy áttekinthesse. A fenti példák azon a mintán alapulnak. További információkért lásd: [integrate-dashboard-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-dashboard-web-app).

További információk érhetők el a JavaScript API-ról a [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript) cikkben.

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

