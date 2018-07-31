---
title: Sorszintű biztonság használata beágyazott Power BI tartalommal
description: Megismerheti Power BI-tartalmak az alkalmazásba való beágyazásának lépéseit.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 02/22/2018
ms.author: maghan
ms.openlocfilehash: d41b0a84d512c5ef6cebf810a89fd74a838c672e
ms.sourcegitcommit: 9efb94ddb254e9c03e9871ad232509065ee24bf2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/06/2018
ms.locfileid: "37864353"
---
# <a name="use-row-level-security-with-power-bi-embedded-content"></a>Sorszintű biztonság használata beágyazott Power BI tartalommal
A sorszintű biztonság (RLS) a felhasználók adatokhoz való hozzáférésének korlátozására használható irányítópultoknál, csempéknél, jelentéseknél és adatkészleteknél. Ugyanazokkal az összetevőkkel több felhasználó is dolgozhat egyszerre úgy, hogy más-másféle adatokat látnak. A beágyazás támogatja a RLS-t.

Ha nem Power BI-felhasználóknak végez beágyazást (alkalmazás tulajdonában lévő adatok, ez általában a szoftverszolgáltatóknál fordul elő), akkor ez a cikk Önnek szól. Konfigurálnia kell a beágyazási tokent a felhasználó és a szerepkör figyelembe vételéhez. Olvasson tovább ennek megismeréséhez.

Ha Power BI-felhasználóknak végez beágyazást (a felhasználó az adatok tulajdonosa) a cégen belül, az RLS ugyanúgy működik, mintha közvetlenül a Power BI szolgáltatásban lenne. Nem kell semmi mást csinálnia az alkalmazásban. További információkat a [Power BI sorszintű biztonság (RLS) használatával kapcsolatos](../service-admin-rls.md) részben találhat.

![A sorszintű biztonságban szereplő elemek.](media/embedded-row-level-security/powerbi-embedded-rls-components.png)

Az RLS kihasználása érdekében fontos megérteni a három fő alapelvet: a felhasználókat, a szerepköröket és a szabályokat. Lássuk mindegyiket közelebbről:

**Felhasználók** – Az összetevőket (irányítópultokat, csempéket, jelentéseket vagy adatkészleteket) megtekintő tényleges végfelhasználók. A Power BI Embedded esetében a felhasználókat beágyazási jogkivonatban lévő felhasználónév tulajdonság azonosítja.

**Szerepkörök** – A felhasználók szerepkörökhöz tartoznak. A szerepkörök szabályok tárolói és olyan nevük lehet, mint *Értékesítési igazgató* vagy *Értékesítési képviselő*. A Power BI Desktopban hozhat létre szerepköröket. További információkat a [sorszintű biztonság (RLS) Power BI Desktoppal való használatával kapcsolatos](../desktop-rls.md) részben találhat.

**Szabályok** – A szerepkörök szabályokkal rendelkeznek, és ezek a szabályok az adatokra alkalmazott tényleges szűrők. Ez olyan egyszerű lehet, mint a „Country = USA”, vagy sokkal dinamikusabb lehet.
A cikk hátralévő részében megadunk egy példát az RLS elkészítésére, majd beágyazott alkalmazásban használjuk azt. A példánk a [Kiskereskedelmi elemzési minta](http://go.microsoft.com/fwlink/?LinkID=780547) PBIX-fájlját használja.

![Jelentéspélda](media/embedded-row-level-security/powerbi-embedded-report-example.png)

## <a name="adding-roles-with-power-bi-desktop"></a>Szerepkörök hozzáadása a Power BI Desktoppal
A Kiskereskedelmi elemzési minta egy kiskereskedelmi láncban lévő összes áruház értékesítéseit jeleníti meg. Az RLS nélkül nem számít, hogy melyik kerület menedzsere jelentkezik be és tekinti meg a jelentést, mindegyik ugyanazokat az adatokat látja. A felső vezetőség meghatározta, hogy mindegyik kerületi menedzser csak az általuk kezelt áruházak értékesítéseit láthatja, és ehhez használhatjuk az RLS-t.

Az RLS a Power BI Desktopban készül. Az adatkészlet és a jelentés megnyitásakor diagramnézetre válthatunk a séma megtekintéséhez:

![Diagramnézet a Power BI Desktopban](media/embedded-row-level-security/powerbi-embedded-schema.png)

Ebben a sémában a következőket érdemes megfigyelni:

* Minden mérték (például a **Total Sales** (Összes értékesítés)) a **Sales** (Értékesítések) ténytáblában van tárolva.
* Négy további kapcsolódó dimenziótábla van: **Item** (Tétel), **Time** (Idő), **Store** (Áruház) és **District** (Kerület).
* A kapcsolatvonalakon lévő nyilak jelzik, milyen irányba haladhatnak a szűrők az egyik táblából egy másikba. Ha például egy szűrő a **Time[Date]** (Idő [Dátum]) táblára van helyezve, a jelenlegi sémában csak a **Sales** (Értékesítések) táblába szűrne lefelé értékeket. Ez a szűrő nem lenne hatással más táblákra, mert a kapcsolatvonalakon lévő összes nyíl az értékesítések táblára mutat, és nem a másik irányba.
* A **District** (Kerület) tábla jelzi, hogy ki az egyes kerületek menedzsere:
  
    ![A District (Kerület) táblában lévő sorok](media/embedded-row-level-security/powerbi-embedded-district-table.png)

Ezen séma alapján, ha szűrőt alkalmazunk a **District** (Kerület) táblában lévő **District Manager** (Kerületi menedzser) oszlopra, és ha ez a szűrő megfelel a jelentést megtekintő felhasználónak, akkor a szűrő a **Store** (Áruház) és a **Sales** (Értékesítések) táblákra is leszűr, hogy csak az adott menedzser adatait jelenítse meg.

Ezt a következőképpen teheti meg:

1. A **Modellezés** lapon válassza a **Szerepkörök kezelése** lehetőséget.
   
    ![Modellezés lap a Power BI Desktopban](media/embedded-row-level-security/powerbi-embedded-manage-roles.png)
2. Hozzon létre egy **Manager** (Menedzser) nevű új szerepkört.
   
    ![Új szerepkör létrehozása](media/embedded-row-level-security/powerbi-embedded-new-role.png)
3. A **District** (Kerület) táblában írja be a következő DAX-kifejezést: **[District Manager] = USERNAME()**.
   
    ![DAX-utasítás RLS-szabályhoz](media/embedded-row-level-security/powerbi-embedded-new-role-dax.png)
4. A szabályok működésének biztosítása érdekében a **Modellezés** lapon válassza a **Megtekintés szerepkörökként** lehetőséget, majd válassza ki a most létrehozott **Manager** szerepkört és az **Egyéb felhasználó** szerepkört is. Írja be felhasználóként az **AndrewMa** nevet.
   
    ![Megtekintés szerepkörökként párbeszédpanel](media/embedded-row-level-security/powerbi-embedded-new-role-view.png)
   
    A jelentések most úgy jelenítenek meg adatokat, mintha **AndrewMa** néven lenne bejelentkezve.

A szűrő alkalmazásakor, ahogyan itt tettük, a **District** (Kerület), **Store** (Áruház) és **Sales** (Értékesítések) táblákban lévő összes rekordhoz. A **Sales** (Értékesítések) és a **Time** (Idő) közötti kapcsolat szűrőiránya miatt azonban a **Sales** (Értékesítések) és az **Item** (Tétel), és az **Item** (Tétel) és a **Time** (Idő) táblákra nem szűr le. A kétirányú keresztszűrésről további információért töltse le az [SQL Server Analysis Services 2016-ban és a Power BI Desktopban használatható kétirányú keresztszűrést ismertető](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) tanulmányt.

## <a name="applying-user-and-role-to-an-embed-token"></a>Felhasználó és szerepkör alkalmazása beágyazási tokenre
Most, hogy konfigurálva vannak a Power BI Desktop-szerepkörök, el kell végezni néhány dolgot az alkalmazásban a szerepkörök kihasználása érdekében.

Az alkalmazás hitelesíti és engedélyezi a felhasználókat és beágyazási tokenekkel ad hozzáférést ezeknek a felhasználóknak egy adott Power BI Embedded-jelentéshez. A Power BI Embedded nem rendelkezik konkrét információkkal arról, hogy ki a felhasználó. Az RLS működéséhez további kontextust kell megadnia a beágyazási token részeként identitások formájában. Ez az [Embed Token](https://docs.microsoft.com/rest/api/power-bi/embedtoken) (Beágyazási Token) API-n keresztül végezhető el.

Az API olyan identitások listáját fogadja el, amelyben jelezve vannak a kapcsolódó adatkészletek. Az RLS működéséhez a következőt kell megadnia az identitás részeként.

* **username (kötelező)** – Ez olyan sztring, amellyel azonosítható a felhasználó az RLS-szabályok alkalmazásakor. Csak egyetlen felhasználó sorolható fel.
* **roles (kötelező)** – Sorszintű biztonsági szabályok alkalmazásakor kiválasztható szerepköröket tartalmazó sztring. Több szerepkör átadásakor sztringtömbként kell azokat átadni.
* **dataset (kötelező)** – Az épp beágyazott összetevőre érvényes adatkészlet. 

A beágyazási token létrehozásához használja a **PowerBIClient.Reports** **GenerateTokenInGroup** metódusát. 

Módosíthatja például a [PowerBIEmbedded_AppOwnsData](https://github.com/Microsoft/PowerBI-Developer-Samples/tree/master/App%20Owns%20Data) mintát. A *Home\HomeController.cs 76. és 77. sora* a következőről frissíthető:

```
// Generate Embed Token.
var generateTokenRequestParameters = new GenerateTokenRequest(accessLevel: "view");

var tokenResponse = await client.Reports.GenerateTokenInGroupAsync(GroupId, report.Id, generateTokenRequestParameters);
```

erre:

```
var generateTokenRequestParameters = new GenerateTokenRequest("View", null, identities: new List<EffectiveIdentity> { new EffectiveIdentity(username: "username", roles: new List<string> { "roleA", "roleB" }, datasets: new List<string> { "datasetId" }) });

var tokenResponse = await client.Reports.GenerateTokenInGroupAsync("groupId", "reportId", generateTokenRequestParameters);
```

Ha a REST API-t hívja meg, a frissített API már elfogad egy további, **identities** nevű JSON-tömböt, amely tartalmaz egy felhasználónevet, a szerepkörök sztringlistáját és az adatkészletek karakterlánclistáját, pl.:

```
{
    "accessLevel": "View",
    "identities": [
        {
            "username": "EffectiveIdentity",
            "roles": [ "Role1", "Role2" ],
            "datasets": [ "fe0a1aeb-f6a4-4b27-a2d3-b5df3bb28bdc" ]
        }
    ]
}
```

Most, hogy minden együtt van, amikor valaki bejelentkezik az alkalmazásba az összetevő megtekintéséhez, csak a számukra engedélyezett adatokat láthatja, ahogyan azt a sorszintű biztonság meghatározza.

## <a name="working-with-analysis-services-live-connections"></a>Élő Analysis Services-kapcsolatok használata
A sorszintű biztonság használható az élő Analysis Services-kapcsolatokkal a helyszíni kiszolgálókhoz. Néhány speciális alapelvet meg kell értenie, amikor ilyen típusú kapcsolatot használ.

A felhasználónév tulajdonsághoz megadott hatályos identitásnak Windows-felhasználónak kell lennie, amely rendelkezik engedélyekkel az Analysis Services-kiszolgálóhoz.

**Helyszíni adatátjáró konfigurációja**

Az élő Analysis Services-kapcsolatok használatakor [helyszíni adatátjárót](../service-gateway-onprem.md) kell használni. Az identitást tartalmazó beágyazási token létrehozásakor a fő fióknak az átjáró rendszergazdájaként kell szerepelnie. Ha a fő fiók nincs felsorolva, a sorszintű biztonság nincs megfelelően alkalmazva az adatokra. Az átjáró nem rendszergazda felhasználója megadhat szerepköröket, de a saját felhasználónevét kell megadnia a hatályos identitáshoz.

**Szerepkörök használata**

A szerepkörök az identitással adhatók meg a beágyazási tokenekben. Ha nincs megadva szerepkör, a rendszer a megadott felhasználónévvel oldja fel a társított szerepköröket.

**A CustomData funkció használata**

A CustomData funkcióval szabad szövegeket (sztringeket) adhat át a CustomData kapcsolatisztring-tulajdonsággal, amelyet az AS használ (A CUSTOMDATA() függvényen keresztül).
Ez egy alternatív mód az adatfelhasználás testreszabására.
A szerepkör DAX-lekérdezésében is használhatja, valamint szerepkör nélkül egy mérték DAX-lekérdezésében.
A CustomData funkció az alábbi összetevők tokenlétrehozási funkcióinak egyik eleme: irányítópult, jelentés és csempe. Az irányítópultok több CustomData-identitással rendelkezhetnek (csempénként/modellenként eggyel).

> [!NOTE]
> A CustomData funkció csak az Azure Analysis Servicesben található modelleken, és csak élő módban működik. A felhasználókkal és a szerepkörökkel ellentétben a CustomData funkció nem használható .pbix-fájlokban. Ha a CustomData funkcióval hoz létre tokent, felhasználónévvel kell rendelkeznie.
>
>

**A CustomData SDK-bővítményei**

A CustomData sztringtulajdonságot hozzáadtuk a tokenlétrehozási forgatókönyvbeli hatályos identitásunkhoz.
        
        [JsonProperty(PropertyName = "customData")]
        public string CustomData { get; set; }

Az identitás egyéni adatokkal, az alábbi hívással hozható létre:

        public EffectiveIdentity(string username, IList<string> datasets, IList<string> roles = null, string customData = null);

**A CustomData SDK-használata**

A REST API meghívásánál minden identitáshoz egyéni adatokat adhat meg, például:

```
{
    "accessLevel": "View",
    "identities": [
        {
            "username": "EffectiveIdentity",
            "roles": [ "Role1", "Role2" ],
            "customData": "MyCustomData",
            "datasets": [ "fe0a1aeb-f6a4-4b27-a2d3-b5df3bb28bdc" ]
        }
    ]
}
```

## <a name="considerations-and-limitations"></a>Megfontolandó szempontok és korlátozások
* A Power BI szolgáltatásban a felhasználók szerepkörökhöz rendelése nincs hatással az RLS-re beágyazási token használatakor.
* Bár a Power BI szolgáltatás nem alkalmazza az RLS beállítást a rendszergazdákra vagy a szerkesztési engedélyekkel rendelkező tagokra, amikor beágyazási tokennel ad meg egy identitást, azt az adatokra alkalmazza.
* Az élő Analysis Services-kapcsolatok a helyszíni kiszolgálókhoz támogatottak.
* Az Azure Analysis Services élő kapcsolatai támogatják a szerepkör szerinti szűrést, de nem támogatják a felhasználónév szerinti dinamikus szűrést. Dinamikus szűrést a CustomData használatával végezhet.
* Ha a mögöttes adatkészlethez nincs szükség RLS-re, a GenerateToken kérés **nem** tartalmazhat hatályos identitást.
* Ha a mögöttes adatkészlet felhőalapú modell (gyorsítótárazott modell vagy DirectQuery), a hatályos identitásnak tartalmaznia kell legalább egy szerepkört, mert ellenkező esetben a szerepkör-hozzárendelés sikertelen lesz.
* Az identitáslista lehetővé teszi, hogy az irányítópultok beágyazásánál több identitásból álló tokent is lehessen használni. A lista minden más összetevő esetében csak egyetlen identitást tartalmaz.

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)
