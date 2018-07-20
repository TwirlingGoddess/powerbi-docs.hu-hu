---
title: Power BI tartalom beágyazása egy alkalmazásba a cége számára
description: 'Útmutató: hogyan integrálhat vagy ágyazhat be jelentést, irányítópultot vagy csempét cége számára egy webalkalmazásba a Power BI API-kkal.'
author: markingmyname
ms.author: maghan
ms.date: 07/13/2018
ms.topic: tutorial
ms.service: powerbi
ms.component: powerbi-developer
ms.custom: mvc
manager: kfile
ms.openlocfilehash: cfc450216202f332f518955d28cb71df6aa0b800
ms.sourcegitcommit: f2b106b5eb338a64f903e8ce6793bccb07f9440a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2018
ms.locfileid: "39105269"
---
# <a name="tutorial-embed-a-power-bi-report-dashboard-or-tile-into-an-application-for-your-organization"></a>Oktatóanyag: Power BI-jelentés, -irányítópult vagy -csempe beágyazása egy alkalmazásba a cége részére
Ez az oktatóanyag bemutatja, hogyan integrálhat egy jelentést az alkalmazásokba a **Power BI .NET SDK** és a **Power BI JavaScript API** segítségével, amikor beágyazza a **Power BI** szolgáltatásait egy céges alkalmazásba. A **Power BI** segítségével jelentéseket, irányítópultokat és csempéket ágyazhat be az alkalmazásokba **a felhasználó az adatok tulajdonosa** forgatókönyvnek megfelelően. **A felhasználó az adatok tulajdonosa** forgatókönyv lehetővé teszi, hogy az alkalmazás kiterjessze a Power BI szolgáltatást.

![Alkalmazás megtekintése](media/embed-sample-for-your-organization/embed-sample-for-your-organization-035.png)

Az oktatóanyag a következőket ismerteti:
>[!div class="checklist"]
>* Alkalmazás regisztrálása az Azure-ban.
>* Ágyazzon be egy Power BI-jelentést egy alkalmazásba.

## <a name="prerequisites"></a>Előfeltételek
A kezdéshez szüksége van egy **Power BI Pro**-fiókra és egy **Microsoft Azure**-előfizetésre.

* Ha még nem regisztrált a **Power BI Pro** szolgáltatásra, a kezdés előtt [hozzon létre egy ingyenes próbaverziós fiókot](https://powerbi.microsoft.com/en-us/pricing/).
* Ha még nincs Azure-előfizetése, kezdés előtt hozzon létre egy [ingyenes fiókot](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* Állítson be egy saját [Azure Active Directory-bérlőt](create-an-azure-active-directory-tenant.md).
* Telepítse a [Visual Studio](https://www.visualstudio.com/) 2013-as vagy későbbi verzióját.

## <a name="setup-your-embedded-analytics-development-environment"></a>A beágyazott elemzési fejlesztési környezet beállítása

Mielőtt jelentéseket, irányítópultokat és csempéket ágyazna be az alkalmazásba, győződjön meg arról, hogy a környezete be van állítva a beágyazás engedélyezéséhez. A beállítás részeként a következőket kell elvégeznie.

A gyors indulás érdekében követheti az [Előkészítési eszköz](https://aka.ms/embedsetup/UserOwnsData) lépéseit, és letölthet egy mintaalkalmazást, amely végigvezeti Önt a környezet létrehozásán és egy jelentés beágyazásán.

Ha mégis a környezet manuális létrehozása mellett dönt, folytathatja az alábbiak szerint.
### <a name="register-an-application-in-azure-active-directory-azure-ad"></a>Alkalmazás regisztrálása az Azure Active Directoryban (Azure AD)

Az alkalmazás Azure Active Directoryban történő regisztrálása lehetővé teszi az alkalmazás számára a Power BI REST API-k elérését. Így identitást hozhat létre az alkalmazás számára, és meghatározhatja a Power BI REST-erőforrásokhoz való engedélyeket.

1. Fogadja el a [Microsoft Power BI API használati feltételeit](https://powerbi.microsoft.com/api-terms).

2. Jelentkezzen be az [Azure Portalon](https://portal.azure.com).

    ![Az Azure Portal főoldala](media/embed-sample-for-your-organization/embed-sample-for-your-organization-002.png)

3. A bal oldali navigációs ablakban válassza ki az **Összes szolgáltatás** lehetőséget, és kattintson az **Alkalmazásregisztráció**, majd az **Új alkalmazás regisztrálása** elemre.

    ![Alkalmazásregisztráció keresése](media/embed-sample-for-your-organization/embed-sample-for-your-organization-003.png)</br>
    ![Új alkalmazás regisztrálása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-004.png)

4. Kövesse az utasításokat az új alkalmazás létrehozásához. **A felhasználó az adatok tulajdonosa** forgatókönyv esetében **webalkalmazást/API-t** kell használnia alkalmazástípusként. Adja meg azt a **Bejelentkezési URL-címet**, amelyet a **Microsoft Azure Active Directory** a jogkivonatválaszok visszaadására használ. Adja meg az alkalmazáshoz tartozó értéket, például : http://localhost:13526/).

    ![Alkalmazás létrehozása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-005.png)

### <a name="apply-permissions-to-your-application-within-azure-active-directory"></a>Engedélyek alkalmazása a saját alkalmazásra az Azure AD-ben

Az alkalmazás részére további engedélyeket is meg kell adnia az alkalmazásregisztrációs oldalon már megadottakon felül. Az engedélyek megadásához egy *globális rendszergazdai* fiókkal kell bejelentkezve lennie.

### <a name="use-the-azure-active-directory-portal"></a>Az Azure Active Directory portál használata

1. Az Azure Portal [Alkalmazásregisztrációk](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ApplicationsListBlade) szakaszában keresse meg azt az alkalmazást, amelyet a beágyazáshoz kíván használni.

    ![Az alkalmazás kiválasztása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-006.png)

2. Kattintson a **Beállítások** elemre, majd az **API-hozzáférés** területen válassza az **Szükséges engedélyek** lehetőséget.

    ![Szükséges engedélyek](media/embed-sample-for-your-organization/embed-sample-for-your-organization-008.png)

3. Válassza a **Windows Azure Active Directory** elemet, majd győződjön meg arról, hogy a **Hozzáférés a címtárhoz a bejelentkezett felhasználóként** beállítás be van jelölve. Kattintson a **Mentés** gombra.

    ![Windows Azure AD-engedélyek](media/embed-sample-for-your-organization/embed-sample-for-your-organization-011.png)

4. Válassza a **Hozzáadás** elemet.

    ![Engedélyek hozzáadása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-012.png)

5. Kattintson az **API kiválasztása** lehetőségre.

    ![API-hozzáférés hozzáadása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-013.png)

6. Kattintson a **Power BI szolgáltatás**, majd a **Kiválasztás** lehetőségre.

    ![PBI szolgáltatás kiválasztása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-014.png)

7. Jelölje be az összes engedélyt a **Delegált engedélyek** szakaszban. Ezeket egyenként kell kijelölnie, hogy menteni tudja a kijelöléseket. Ha végzett, kattintson a **Mentés** gombra.

    ![Delegált engedélyek kiválasztása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-015.png)

## <a name="setup-your-power-bi-environment"></a>A Power BI-környezet beállítása

### <a name="create-an-app-workspace"></a>Alkalmazás munkaterületének létrehozása

Amikor beágyazza a jelentéseket, irányítópultokat vagy csempéket az ügyfelei számára, akkor egy alkalmazás-munkaterületen kell elhelyeznie a tartalmakat.

1. Kezdjük a munkaterület létrehozásával. Kattintson a **munkaterületek** > **Alkalmazás-munkaterületek létrehozása** lehetőségre. A tartalmat itt kell elhelyeznie, hogy elérhető legyen az alkalmazás számára.

    ![Munkaterület létrehozása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-020.png)

2. Nevezze el a munkaterületet. Ha a megfelelő **munkaterület-azonosító** nem használható, szerkesztéssel hozzon létre egy egyedi azonosítót. Ez lesz az alkalmazás neve is.

    ![Munkaterület elnevezése](media/embed-sample-for-your-organization/embed-sample-for-your-organization-021.png)

3. Néhány beállítást meg kell adnia. Ha **nyilvánosra** állítja a munkaterületet, a szervezet bármely tagja megtekintheti annak tartalmát. A **Privát** beállítás ezzel szemben azt jelenti, hogy a munkaterület tartalmát csak a tagok láthatják.

    ![Privát/Nyilvános](media/embed-sample-for-your-organization/embed-sample-for-your-organization-022.png)

    A Nyilvános/Privát beállítás a csoport létrehozását követően nem módosítható.

4. Azt is beállíthatja, hogy a tagok **szerkeszthetik-e** a tartalmakat vagy **csak megtekintési** jogosultságuk van.

    ![Tagok felvétele](media/embed-sample-for-your-organization/embed-sample-for-your-organization-023.png)

5. Vegye fel az adott személyek e-mail-címét, akiknek hozzáférést kíván adni a munkaterülethez, majd kattintson a **Hozzáadás** gombra. Csoportaliasokat nem adhat hozzá, csak egyéneket.

6. Döntse le, hogy az egyes személyek egyszerű tagok vagy adminisztrátorok legyenek-e. Az adminisztrátorok szerkeszthetik magát a munkaterületet is, és tagokat is felvehetnek. A tagok a munkaterület tartalmát szerkeszthetik, amennyiben nem csak megtekintési jogosultsággal rendelkeznek. Az alkalmazást az adminisztrátorok és a tagok egyaránt közzétehetik.

    Most megtekintheti az új munkaterületet. A Power BI létrehozza és megnyitja a munkaterületet. Ekkor megjelenik az olyan munkaterületek listájában, amelyeknek Ön a tagja. Mivel adminisztrátori jogosultsággal rendelkezik, a három pontra (...) kattintva visszaléphet, és szerkesztheti a munkaterületet, például új tagokat adhat hozzá vagy módosíthatja a tagok jogosultságait.

    ![Munkaterület létrehozása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-025.png)

### <a name="create-and-publish-your-reports"></a>Saját jelentések létrehozása és közzététele

A Power BI Desktop segítségével létrehozhatja jelentéseit és adatkészleteit, majd közzéteheti ezeket a jelentéseket egy alkalmazás-munkaterületen. A jelentéseket közzétevő végfelhasználónak Power BI Pro-licencre van szüksége az alkalmazás-munkaterületen történő közzétételhez.

1. Töltse le a [Blog Demo](https://github.com/Microsoft/powerbi-desktop-samples) mintát a GitHubról.

    ![jelentésminta](media/embed-sample-for-your-organization/embed-sample-for-your-organization-026-1.png)

2. PBIX-mintajelentés megnyitása a **Power BI Desktopban**

   ![PBI desktop jelentés](media/embed-sample-for-your-organization/embed-sample-for-your-organization-027.png)

3. Közzététel az **alkalmazás-munkaterületen**

   ![PBI desktop jelentés](media/embed-sample-for-your-organization/embed-sample-for-your-organization-028.png)

    A jelentést mostantól online megtekintheti a Power BI szolgáltatásban.

   ![PBI desktop jelentés](media/embed-sample-for-your-organization/embed-sample-for-your-organization-029.png)

## <a name="embed-your-content-using-the-sample-application"></a>Tartalom beágyazása a mintaalkalmazással

A mintaalkalmazás segítségével történő tartalombeágyazáshoz kövesse az alábbi lépéseket.

1. A kezdéshez töltse le a [User Owns Data mintát](https://github.com/Microsoft/PowerBI-Developer-Samples) a GitHubról.  Három eltérő mintaalkalmazás áll rendelkezésre egy a [jelentések](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-report-web-app), egy az [irányítópultok](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-dashboard-web-app) és egy a [csempék](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/User%20Owns%20Data/integrate-tile-web-app) számára.  Ez a cikk az alábbiakban a lépések megbeszélésekor a **reports** (jelentések) alkalmazásra hivatkozik.

    ![User Owns Data alkalmazásminta](media/embed-sample-for-your-organization/embed-sample-for-your-organization-026.png)

2. Nyissa meg a Cloud.config fájlt ugyanebben az alkalmazásban. Az alkalmazás sikeres futtatásához néhány mezőt ki kell töltenie: A **ClientID** (Ügyfélazonosító) és a **ClientSecret** (Titkos ügyfélkulcs) mezőt.

    ![Cloud Config fájl](media/embed-sample-for-your-organization/embed-sample-for-your-organization-030.png)

    A **ClientID** mezőbe az **Azure-beli** **Alkalmazásazonosítót** kell beírni. Az alkalmazás a **ClientID** használatával azonosítja magát azon felhasználóknál, akiktől Ön engedélyeket kér.

    A **ClientID** beszerzéséhez kövesse az alábbi lépéseket:

    Jelentkezzen be az [Azure Portalon](https://portal.azure.com).

    ![Az Azure Portal főoldala](media/embed-sample-for-your-organization/embed-sample-for-your-organization-002.png)

    A bal oldali navigációs ablaktáblán válassza az **Összes szolgáltatást**, és kattintson az **Alkalmazásregisztrációk** lehetőségre.

    ![Alkalmazásregisztráció keresése](media/embed-sample-for-your-organization/embed-sample-for-your-organization-003.png)

    Válassza ki azt az alkalmazást, amelynek használnia kell a **ClientID** azonosítót.

    ![Az alkalmazás kiválasztása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-006.png)

    Megjelenik egy GUID-ként listázott **alkalmazásazonosító**. Használja ezt az **alkalmazásazonosítót** az alkalmazás **ClientID** mezőjében.

    ![Ügyfélazonosító](media/embed-sample-for-your-organization/embed-sample-for-your-organization-007.png)

    Másolja be a **ClientSecret** (Titkos ügyfélkulcs) adatot az **Azure** **Alkalmazásregisztrációk** szakaszának **Kulcsok** szakaszából.

    A **ClientSecret** (Titkos ügyfélkulcs) beszerzéséhez kövesse az alábbi lépéseket:

    Jelentkezzen be az [Azure Portalon](https://portal.azure.com).

    ![Az Azure Portal főoldala](media/embed-sample-for-your-organization/embed-sample-for-your-organization-002.png)

    A bal oldali navigációs ablaktáblán válassza az **Összes szolgáltatást**, és kattintson az **Alkalmazásregisztrációk** lehetőségre.

    ![Alkalmazásregisztráció keresése](media/embed-sample-for-your-organization/embed-sample-for-your-organization-003.png)

    Válassza ki azt az alkalmazást, amelynek használnia kell a **ClientSecret** kulcsot.

    ![Az alkalmazás kiválasztása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-006.png)

    Kattintson a **Beállítások** elemre.

    ![Beállítások](media/embed-sample-for-your-organization/embed-sample-for-your-organization-038.png)

    Válassza a **Kulcsok** lehetőséget.

    ![Kulcsok](media/embed-sample-for-your-organization/embed-sample-for-your-organization-039.png)

    Töltse ki a **Leírás** mezőt egy névvel, majd válasszon egy **időtartam** értéket, majd válassza a **Mentés** lehetőséget az **Érték** betöltéséhez az alkalmazáshoz. Miután a **kulcsérték** mentését követően bezárja a **Kulcsok** panelt, az érték mező csak **_Rejtett_** tulajdonságúként jelenik meg, és nem ekkor nem fogja tudni lekérni a **kulcsértéket**. Amennyiben elveszíti a **kulcsértéket**, egy újat kell létrehoznia az **Azure Portalon**.

    ![Kulcsok](media/embed-sample-for-your-organization/embed-sample-for-your-organization-031.png)

     A **csoportazonosító** mezőbe írja be a Power BI-ban szereplő **alkalmazás-munkaterület GUID-azonosítóját**.

    ![csoportazonosító](media/embed-sample-for-customers/embed-sample-for-customers-031.png)

    A **jelentésazonosító** mezőbe írja be a Power BI-ban szereplő **jelentés GUID-azonosítóját**.

    ![jelentésazonosító](media/embed-sample-for-customers/embed-sample-for-customers-032.png)

3. Futtassa az alkalmazást!

    Először is kattintson a **Futtatás** elemre a **Visual Studióban**.

    ![Alkalmazás futtatása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-033.png)

    Majd válassza a **Jelentés beolvasása** lehetőséget.

    ![Tartalom kiválasztása](media/embed-sample-for-your-organization/embed-sample-for-your-organization-034.png)

    Most megtekintheti a jelentést a mintaalkalmazásban.

    ![Alkalmazás megtekintése](media/embed-sample-for-your-organization/embed-sample-for-your-organization-035.png)

## <a name="embed-your-content-within-your-application"></a>Tartalom beágyazása az alkalmazásba
Bár a tartalombeágyazás lépései elvégezhetők a [Power BI REST API-kkal](https://docs.microsoft.com/rest/api/power-bi/), a cikkben bemutatott mintakódok hajtanak a **.NET SDK-val** készültek.

Egy jelentés webalkalmazásba való beágyazására használja a **Power BI REST API-t** vagy a **Power BI C# SDK-t**, valamint egy Azure Active Directory (AD) engedélyezési **hozzáférési tokent** a jelentés lekéréséhez. Ezután töltse be a jelentést ugyanezen **hozzáférési token** használatával. A **Power BI Rest API** szoftveres hozzáférést biztosít meghatározott **Power BI**-erőforrásokhoz. További információt a [Power BI REST API](https://docs.microsoft.com/rest/api/power-bi/) és a [Power BI JavaScript API](https://github.com/Microsoft/PowerBI-JavaScript) című cikkekben talál.

### <a name="get-an-access-token-from-azure-ad"></a>Hozzáférési token lekérése a Microsoft Azure Active Directory-ból
Az alkalmazásban először egy **hozzáférési tokent** kell beszereznie az Azure AD-ből, mielőtt hívásokat indíthatna a Power BI REST API-hoz. További információkért lásd [a felhasználók hitelesítésével és a Power BI-alkalmazáshoz Azure AD hozzáférési token beszerzésével](get-azuread-access-token.md) kapcsolatos cikket.

### <a name="get-a-report"></a>Jelentés lekérése
**Power BI**-jelentés lekéréséhez használja a [Jelentések lekérése](https://docs.microsoft.com/rest/api/power-bi/reports/getreports) műveletet, amely a **Power BI**-jelentések listáját kéri le. A jelentések listájából lekérheti a jelentésazonosítót.

### <a name="get-reports-using-an-access-token"></a>Jelentések lekérése hozzáférési token használatával
A [Jelentések lekérése](https://docs.microsoft.com/rest/api/power-bi/reports/getreports) művelet jelentések listáját adja vissza. A jelentések listájából lekérhet egyetlen jelentést.

A REST API-hívásához egy *Engedélyezési* fejlécet is meg kell adnia a *Tulajdonos {hozzáférési token}* formátumában.

#### <a name="get-reports-with-the-rest-api"></a>Jelentések lekérése a REST API-val

Íme egy kódminta, hogyan kérjünk le jelentéseket a **REST API-val**.

*A beágyazni kívánt tartalomelemek (jelentés, irányítópult vagy csempe) a [mintaalkalmazás](#embed-your-content-using-the-sample-application) **_Default.aspx.cs_** fájljában érhetők el.*

```csharp
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
A .NET SDK használatával lekérheti a jelentések listáját ahelyett, hogy közvetlenül a REST API-t hívná. Íme egy kódminta a jelentések listázásához.

```csharp
using Microsoft.IdentityModel.Clients.ActiveDirectory;
using Microsoft.PowerBI.Api.V2;
using Microsoft.PowerBI.Api.V2.Models;

var tokenCredentials = new TokenCredentials(<ACCESS TOKEN>, "Bearer");

// Create a Power BI Client object. It is used to call Power BI APIs.
using (var client = new PowerBIClient(new Uri(ApiUrl), tokenCredentials))
{
    // Get the first report all reports in that workspace
    ODataResponseListReport reports = client.Reports.GetReports();

    Report report = reports.Value.FirstOrDefault();

    var embedUrl = report.EmbedUrl;
}
```

### <a name="load-a-report-using-javascript"></a>Jelentés betöltése a JavaScript használatával
A JavaScript használatával egy jelentést tölthet be a div elembe a weblapon.

Itt láthat arra mintakódot, hogyan kérhető le egy jelentés egy adott munkaterületről.

*A tartalomelemek, például jelentés, irányítópult vagy a beágyazni kívánt csempe betöltéséhez minta a [mintaalkalmazás](#embed-your-content-using-the-sample-application) **_Default.aspx_** fájljában érhető el.*

```javascript
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

```javascript
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
    }
  );
}
```

## <a name="using-a-power-bi-premium-dedicated-capacity"></a>Dedikált Power BI Premium-kapacitás használata

Most, hogy elkészült az alkalmazás fejlesztésével, ideje dedikált kapacitással ellátni az alkalmazás munkaterületét.

### <a name="create-a-dedicated-capacity"></a>Dedikált kapacitás létrehozása
Dedikált kapacitás létrehozásával kihasználhatja annak az előnyeit, hogy egy dedikált erőforrás áll rendelkezésre az alkalmazás-munkaterületen a tartalom számára. Ha egy munkaterület nincs hozzárendelve dedikált kapacitáshoz, akkor megosztott kapacitásnak számít. Dedikált kapacitást létrehozhat a [Power BI Premium ](../service-admin-premium-purchase.md) használatával.

### <a name="assign-an-app-workspace-to-a-dedicated-capacity"></a>Alkalmazás-munkaterület hozzárendelése dedikált kapacitáshoz

A dedikált kapacitás létrehozása után hozzárendelheti az alkalmazás-munkaterületet ehhez a kapacitáshoz. Ehhez kövesse az alábbi lépéseket.

1. A **Power BI szolgáltatásban** bontsa ki a munkaterületeket, és kattintson a három pont elemre azon munkaterület mellett, amelyiket tartalombeágyazáshoz használ. Válassza a **Munkaterületek szerkesztése** lehetőséget.

    ![Munkaterület szerkesztése](media/embed-sample-for-your-organization/embed-sample-for-your-organization-036.png)

2. Bontsa ki a **Speciális** elemet, engedélyezze a **Dedikált kapacitást**, majd kattintson a létrehozott dedikált kapacitásra. Kattintson a **Mentés** gombra.

    ![Dedikált kapacitás hozzárendelése](media/embed-sample-for-your-organization/embed-sample-for-your-organization-024.png)

3. A **Mentés** kiválasztása után meg kell jelennie egy **gyémántnak** az alkalmazás-munkaterület neve mellett.

    ![egy kapacitáshoz hozzárendelt alkalmazás-munkaterület](media/embed-sample-for-your-organization/embed-sample-for-your-organization-037.png)

## <a name="next-steps"></a>Következő lépések
Ebben az oktatóanyagban bemutattuk, hogyan lehet Power BI-tartalmat beágyazni egy alkalmazásba a **céges Power BI-fiók** használva. Most megpróbálhatja alkalmazások használatával beágyazni a Power BI-tartalmat egy alkalmazásba.  Megpróbálkozhat Power BI-tartalom beágyazásával külső ügyfelek számára is.

> [!div class="nextstepaction"]
> [Beágyazás alkalmazásokból](embed-from-apps.md)

> [!div class="nextstepaction"]
>[Beágyazás külső ügyfelek számára](embed-sample-for-customers.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)
