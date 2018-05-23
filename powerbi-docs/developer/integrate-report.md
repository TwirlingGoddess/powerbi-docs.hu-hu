---
title: Power BI-jelentés integrálása a szervezet egy alkalmazásába
description: Ismerje meg, hogyan integrálhat vagy ágyazhat be egy jelentést webalkalmazásba a Power BI API-kkal.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 10/05/2017
ms.author: maghan
ms.openlocfilehash: d2fa65587fdbd85aabd429d531b79e9e614d2f49
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
---
# <a name="integrate-a-report-into-an-app-for-your-organization"></a>Jelentés integrálása a szervezet egy alkalmazásába
Ismerje meg, hogyan integrálhat vagy ágyazhat be egy jelentést a webalkalmazásba REST API-hívásokkal és a Power BI JavaScript API-val együtt, ha a szervezete számára ágyaz be.

![Minta beágyazott jelentés](media/integrate-report/powerbi-embedded-report.png)

Az útmutató megkezdéséhez egy **Power BI**-fiókra van szükség. Ha nincs fiókja, [regisztrálhat egy ingyenes Power BI-fiókot](../service-self-service-signup-for-power-bi.md), vagy létrehozhat saját [Azure Active Directory-bérlőt](create-an-azure-active-directory-tenant.md) tesztelési célra.

> [!NOTE]
> Inkább beágyazási tokennel szeretne jelentést beágyazni az ügyfelei számára? Tekintse meg az [Irányítópult, csempe vagy jelentés beágyazása az alkalmazásba ügyfelek számára](embed-sample-for-customers.md) című cikket.
> 
> 

Egy jelentés beágyazásához a webalkalmazásba használja a **Power BI** REST API-t vagy a Power BI C# SDK-t, valamint egy Azure Active Directory (AD) engedélyezési **hozzáférési tokent** a jelentés lekéréséhez. Ezután töltse be a jelentést ugyanezen hozzáférési token használatával. A **Power BI** API szoftveres hozzáférést biztosít egyes **Power BI**-erőforrásokhoz. További információkért lásd: [A Power BI REST API áttekintése](https://msdn.microsoft.com/library/dn877544.aspx) és [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript).

## <a name="download-the-sample"></a>A minta letöltése
Ez a cikk a GitHubon, az [integrate-report-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-report-web-app) mintában használt kódot mutatja be. A bemutató követéséhez letöltheti a mintát.

## <a name="step-1---register-an-app-in-azure-ad"></a>1. lépés – alkalmazás regisztrálása az Azure AD-ben
A REST API-hívások indításához az alkalmazásokat regisztrálni kell az Azure AD-ben. További információkért lásd: [Azure AD alkalmazás regisztrálása Power BI-tartalmak beágyazásához](register-app.md).

Ha letöltötte az [integrate-report-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-report-web-app) mintát, használja a regisztráció után kapott **Ügyfél-azonosítót** és a **Titkos ügyfélkulcsot**, így a minta hitelesítést végezhet az Azure AD-ben. A minta konfigurálásához módosítsa az **Ügyfél-azonosítót** és a **Titkos ügyfélkulcsot** a *cloud.config* fájlban.

![](media/integrate-report/powerbi-embed-dashboard-register-app4.png)

## <a name="step-2---get-an-access-token-from-azure-ad"></a>2. lépés – hozzáférési token lekérése az Azure AD-ből
Az alkalmazásban először egy **hozzáférési tokent** kell beszereznie az Azure AD-ből, mielőtt hívásokat indíthatna a Power BI REST API-hoz. További információkért lásd [a felhasználók hitelesítésével és a Power BI-alkalmazáshoz Azure AD hozzáférési token beszerzésével](get-azuread-access-token.md) kapcsolatos cikket.

## <a name="step-3---get-a-report"></a>3. lépés – jelentés lekérése
**Power BI**-jelentés lekéréséhez használja a [Jelentések lekérése](https://msdn.microsoft.com/library/mt634543.aspx) műveletet, amely a **Power BI**-jelentések listáját kéri le. A jelentések listájából lekérheti a jelentésazonosítót.

### <a name="get-reports-using-an-access-token"></a>Jelentések lekérése hozzáférési token használatával
A [2. lépésben](#step-2-get-an-access-token-from-azure-ad) lekért **hozzáférési token** segítségével meghívhatja a [Jelentések lekérése](https://msdn.microsoft.com/library/mt634543.aspx) műveletet. A [Jelentések lekérése](https://msdn.microsoft.com/library/mt634543.aspx) művelet jelentések listáját adja vissza. A jelentések listájából lekérhet egyetlen jelentést. Alul látható egy teljes C# metódus jelentés lekéréséhez. 

A REST API-hívásához egy *Engedélyezési* fejlécet is meg kell adnia a *Tulajdonos {hozzáférési token}* formátumában.

#### <a name="get-reports-with-the-rest-api"></a>Jelentések lekérése a REST API-val
**Default.aspx.cs**

```
using Newtonsoft.Json;

//Get a Report. In this sample, you get the first Report.
protected void GetReport(int index)
{
    //Configure Reports request
    System.Net.WebRequest request = System.Net.WebRequest.Create(
        String.Format("{0}/Reports",
        baseUri)) as System.Net.HttpWebRequest;

    request.Method = "GET";
    request.ContentLength = 0;
    request.Headers.Add("Authorization", String.Format("Bearer {0}", accessToken.Value));

    //Get Reports response from request.GetResponse()
    using (var response = request.GetResponse() as System.Net.HttpWebResponse)
    {
        //Get reader from response stream
        using (var reader = new System.IO.StreamReader(response.GetResponseStream()))
        {
            //Deserialize JSON string
            PBIReports Reports = JsonConvert.DeserializeObject<PBIReports>(reader.ReadToEnd());

            //Sample assumes at least one Report.
            //You could write an app that lists all Reports
            if (Reports.value.Length > 0)
            {
                var report = Reports.value[index];

                txtEmbedUrl.Text = report.embedUrl;
                txtReportId.Text = report.id;
                txtReportName.Text = report.name;
            }
        }
    }
}

//Power BI Reports used to deserialize the Get Reports response.
public class PBIReports
{
    public PBIReport[] value { get; set; }
}
public class PBIReport
{
    public string id { get; set; }
    public string name { get; set; }
    public string webUrl { get; set; }
    public string embedUrl { get; set; }
}
```

#### <a name="get-reports-using-the-net-sdk"></a>Jelentések lekérése a .NET SDK használatával
A .NET SDK használatával lekérheti a jelentések listáját ahelyett, hogy közvetlenül a REST API-t hívná.

```
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

var tokenCredentials = new TokenCredentials(<ACCESS TOKEN>, "Bearer");

// Create a Power BI Client object. It will be used to call Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Get the first report all reports in that workspace
    ODataResponseListReport reports = client.Reports.GetReports();

    Report report = reports.Value.FirstOrDefault();

    var embedUrl = report.EmbedUrl;
}
```

## <a name="step-4---load-a-report-using-javascript"></a>4. lépés – jelentés betöltése a JavaScript használatával
A JavaScript használatával egy jelentést tölthet be a div elembe a weblapon.

**Default.aspx**

```
<!-- Embed Report-->
<div> 
    <asp:Panel ID="PanelEmbed" runat="server" Visible="true">
        <div>
            <div><b class="step">Step 3</b>: Embed a report</div>

            <div>Enter an embed url for a report from Step 2 (starts with https://):</div>
            <input type="text" id="tb_EmbedURL" style="width: 1024px;" />
            <br />
            <input type="button" id="bEmbedReportAction" value="Embed Report" />
        </div>

        <div id="reportContainer"></div>
    </asp:Panel>
</div>
```

**Site.master**

```
window.onload = function () {
    // client side click to embed a selected report.
    var el = document.getElementById("bEmbedReportAction");
    if (el.addEventListener) {
        el.addEventListener("click", updateEmbedReporte, false);
    } else {
        el.attachEvent('onclick', updateEmbedReport);
    }

    // handle server side post backs, optimize for reload scenarios
    // show embedded report if all fields were filled in.
    var accessTokenElement = document.getElementById('MainContent_accessTokenTextbox');
    if (accessTokenElement !== null) {
        var accessToken = accessTokenElement.value;
        if (accessToken !== "")
            updateEmbedReport();
    }
};

// update embed report
function updateEmbedReport() {

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
        type: 'report',
        accessToken: accessToken,
        embedUrl: embedUrl
    };

    // Grab the reference to the div HTML element that will host the report.
    var reportContainer = document.getElementById('reportContainer');

    // Embed the report and display it within the div container.
    var report = powerbi.embed(reportContainer, config);

    // report.on will add an event handler which prints to Log window.
    report.on("error", function (event) {
        var logView = document.getElementById('logView');
        logView.innerHTML = logView.innerHTML + "Error<br/>";
        logView.innerHTML = logView.innerHTML + JSON.stringify(event.detail, null, "  ") + "<br/>";
        logView.innerHTML = logView.innerHTML + "---------<br/>";
    });
}
```

Ha letöltötte és futtatta az [integrate-report-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-report-web-app) mintát, a minta az alább láthatóhoz fog hasonlítani.

![Minta beágyazott jelentés](media/integrate-report/powerbi-embedded-report.png)

## <a name="working-with-groups-app-workspaces"></a>A csoportok kezelése (alkalmazás-munkaterületek)
Egy jelentés beágyazásához egy csoportból (alkalmazás-munkaterületről) be kell szereznie az egy csoport irányítópultján belül elérhető jelentések listáját az alábbi REST API-hívás használatával. További információ erről a REST API-hívásról: [Jelentések lekérése](https://msdn.microsoft.com/library/mt634543.aspx). A csoportban engedéllyel kell rendelkeznie, hogy a kérés eredményeket adjon vissza.

```
https://api.powerbi.com/v1.0/myorg/groups/{group_id}/reports
```

A fenti API az elérhető jelentések listáját adja vissza. Mindegyik jelentés rendelkezik egy EmbedUrl-tulajdonsággal, amely a csoportbeágyazás támogatására lett létrehozva.

```
https://app.powerbi.com/reportEmbed?reportId={report_id}&groupId={group_id}
```

## <a name="next-steps"></a>További lépések
Egy mintaalkalmazás elérhető a GitHubon, hogy áttekinthesse. További információkért lásd: [integrate-report-web-app](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-report-web-app).

További információk érhetők el a JavaScript API-ról a [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript) cikkben.

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

