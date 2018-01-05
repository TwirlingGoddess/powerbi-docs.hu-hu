---
title: "Beágyazott alkalmazás hibaelhárítása"
description: "Ez a cikk azokat a gyakori problémákat ismerteti, amelyek Power BI-tartalmak beágyazása során merülhetnek fel."
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
ms.openlocfilehash: f6ffc56f524da84e865d17981faddef58534c785
ms.sourcegitcommit: 8f72ce6b35aa25979090a05e3827d4937dce6a0d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/27/2017
---
# <a name="troubleshooting-your-embedded-application"></a>Beágyazott alkalmazás hibaelhárítása

Ez a cikk azokat a gyakori problémákat ismerteti, amelyek Power BI-tartalmak beágyazása során merülhetnek fel.

## <a name="app-registration"></a>Alkalmazásregisztráció

**Sikertelen alkalmazásregisztráció**

Ha hibaüzenetet tapasztal az Azure Portal vagy a Power BI alkalmazásregisztrációs oldalán, akkor az a megfelelő jogosultságok hiányára utal. Alkalmazások regisztrációjához rendszergazdának kell lennie az Azure AD-bérlőjében, vagy engedélyezni kell az alkalmazások regisztrációját a nem rendszergazdai felhasználók számára.

**Új alkalmazás regisztrációja során nem jelenik meg a Power BI szolgáltatás az Azure Portalon**

Legalább egy felhasználónak regisztrálni kell a Power BI-ra. Ha nem látja a **Power BI szolgáltatást** az API-listában, akkor egyetlen felhasználó sem regisztrált a Power BI-ra.

## <a name="rest-api"></a>REST API

**401-es értékkel visszatérő API-hívás**

A hiba további felderítéséhez szükség lehet a Fidlerre a forgalom rögzítéséhez. Előfordulhat, hogy a regisztrált alkalmazás nem rendelkezik a szükséges jogosultságok körével az Azure AD-n belül. Ellenőrizze az Azure Portalon, hogy megtalálhatók-e az alkalmazásregisztrációban az Azure AD-hez szükséges jogkörök.

**403-as értékkel visszatérő API-hívás**

A hiba további felderítéséhez szükség lehet a Fidlerre a forgalom rögzítéséhez. A 403-as hibát több tényező is okozhatja.

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

**A token generálása sikertelen a hatályos identitás megadásakor**

Megadott hatályos identitás esetén a GenerateToken-hívás sikertelenségét több tényező is okozhatja.

* Az adatkészlet nem támogatja a hatályos identitás használatát
* Nem adta meg a felhasználónevet
* Nem adta meg a szerepkört
* Nem adta meg a DatasetId-t
* A felhasználó nem rendelkezik megfelelő engedélyekkel

Ahhoz, hogy eldönthesse, melyik okozza a hibát, próbálja meg a következőket.

* Hajtsa végre az [adatok lekérését](https://msdn.microsoft.com/library/mt784653.aspx). Az IsEffectiveIdentityRequired tulajdonság true (igaz) értékű?
* A felhasználónév megadása minden EffectiveIdentity esetén kötelező.
* Ha az IsEffectiveIdentityRolesRequired true (igaz) értékű, akkor kötelező megadni a szerepkört.
* A DatasetId megadása minden EffectiveIdentity esetén kötelező.
* Az Analysis Serviceshez használt fő felhasználónak az átjáró rendszergazdájának kell lennie.

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

## <a name="tools-for-troubleshooting"></a>Hibaelhárítási eszközök

### <a name="fiddler-trace"></a>Nyomon követés a Fiddlerrel

A [Fiddler](http://www.telerik.com/fiddler) a Telerik által kifejlesztett, HTTP-forgalmat figyelő ingyenes eszköz.  A Power BI API-k használatával megtekintheti a lekérdezések oda-vissza áramlását az ügyfélszámítógépen. Ebből kiderítheti az esetleges hibákat, illetve az egyéb kapcsolódó információkat.

![Nyomon követés a Fiddlerrel](../includes/media/gateway-onprem-tshoot-tools-include/fiddler.png)

### <a name="f12-in-browser-for-front-end-debugging"></a>F12 billentyű a böngészőben a kezelőfelületen történő hibakereséshez

Az F12 billentyű megnyitja a böngészőben a fejlesztői ablakot. Ezzel megtekintheti a hálózati forgalmat és az egyéb információkat.

![F12 billentyű a böngészőben történő hibakereséshez](media/embedded-troubleshoot/browser-f12.png)

A gyakori kérdésekre adott válaszokért tekintse meg a [Power BI Embedded – Gyakori kérdések](embedded-faq.md) című cikket.

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)