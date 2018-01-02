---
title: "Power BI tartalmak terjesztése Azure AD B2B külső vendégfelhasználóknak"
description: "A Power BI integrálható az Azure Active Directory vállalatközi felhasználásra szánt verziójával (Azure AD B2B), ami lehetővé teszi, hogy a Power BI-tartalmakat cégen kívüli vendégfelhasználókkal is biztonságosan meg tudja osztani."
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
ms.date: 12/07/2017
ms.author: asaxton
ms.openlocfilehash: 147ec28e64cf271843fcffdd14abe005345170e0
ms.sourcegitcommit: 7248b5e449b2495d6baef385470d18edfacec457
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2017
---
# <a name="distribute-power-bi-content-to-external-guest-users-with-azure-ad-b2b"></a>Power BI tartalmak terjesztése Azure AD B2B külső vendégfelhasználóknak

A Power BI integrálható az Azure Active Directory vállalatközi felhasználásra szánt verziójával (Azure AD B2B), ami lehetővé teszi, hogy a Power BI-tartalmakat cégen kívüli vendégfelhasználókkal is biztonságosan meg tudja osztani, úgy, hogy közben teljes mértékben szabályozza a belső adatok felhasználását.

> [!VIDEO https://www.youtube.com/embed/xxQWEQ1NnlY]

> [!NOTE]
> Ez a funkció jelenleg nem érhető el Power BI-mobilalkalmazásokban. Az Azure AD B2B-vel megosztott Power BI-tartalmakat a mobileszközén böngészőben tekintheti meg. 

## <a name="invite-guest-users"></a>Vendégfelhasználók meghívása

Power BI bérlőjébe kétféleképpen hívat meg vendégeket: tervezett és ad-hoc módon. Meghívóra csak akkor van szükség, amikor először hív meg egy külső felhasználót a cégbe.

### <a name="planned-invites"></a>Tervezett meghívások

Tervezett meghívást az Azure AD-beli Microsoft Azure Portalon belül, PowerShellt használva hozhat létre és küldhet el. Ha tudja, mely felhasználókat szeretné meghívni, ezt a módszert kell használni. 

**Az Azure AD Portalon csak bérlői rendszergazdák hozhatnak létre vendégfelhasználókat.**

1. Nyissa meg az [Azure Portalt](https://portal.azure.com), és válassza az **Azure Active Directory** lehetőséget.

2. Navigáljon a **Felhasználók és csoportok** > **Minden felhasználó** > **Új vendégfelhasználó** lehetőséghez.

    ![Azure AD-portál – új vendégfelhasználó](media/service-admin-azure-ad-b2b/azuread-portal-new-guest-user.png)

3. Adja meg az **e-mail címet** és egy **személyes üzenetet**.

    ![Azure AD Portal – Új vendégfelhasználó meghívó üzenete](media/service-admin-azure-ad-b2b/azuread-portal-invite-message.png)

4. Kattintson a **Meghívás** lehetőségre.

Ha egynél több vendéget szeretne meghívni, használja a PowerShellt. Ha további információra van szüksége, tekintse át az [Azure Active Directory B2B együttműködési kódmintát és PowerShell-példákat](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-code-samples) tartalmazó cikket.

A vendégfelhasználónak az e-mailben kapott meghívóban rá kell majd kattintania az **Első lépések** (Get Started) lehetőségre. A rendszer ezután hozzá fogja adni a vendégfelhasználót a bérlőhöz.

![Vendégfelhasználó e-mailes meghívása](media/service-admin-azure-ad-b2b/guest-user-invite-email.png)

### <a name="ad-hoc-invites"></a>Ad-hoc meghívások

Bármikor végrehajthat egy meghívást úgy, hogy közzétételkor hozzáad egy külső felhasználót az alkalmazások hozzáférési listájához.

![Alkalmazás-hozzáférési listához hozzáadott külső felhasználó](media/service-admin-azure-ad-b2b/power-bi-app-access.png)

A vendégfelhasználó fog kapni egy e-mailt, amely azt jelzi, hogy megosztották vele az alkalmazást.

![Vendégfelhasználóval megosztott alkalmazásról szóló e-mail](media/service-admin-azure-ad-b2b/guest-user-invite-email2.png)

A vendégfelhasználónak a céges e-mail-címével kell bejelentkeznie. Bejelentkezés után a rendszer kérni fogja a meghívó elfogadását. Bejelentkezés után a vendégfelhasználót a rendszer átirányítja az alkalmazás tartalmához. Az alkalmazáshoz való visszatéréshez könyvjelzőzze a hivatkozást, és mentse el az e-mailt.

## <a name="licensing"></a>Licencelés

A meghívott felhasználónak megfelelő licencre lesz szüksége ahhoz, hogy megtekinthesse a megosztott alkalmazást. Ennek biztosítására három lehetőség van.

### <a name="use-power-bi-premium"></a>Prémium szintű Power BI használata

Ha az alkalmazás munkaterületét prémium szintű Power BI-kapacitáshoz rendeli, a vendégfelhasználó Power BI Pro-licenc nélkül is használhatja az alkalmazást. Az alkalmazások tekintetében további előnyöket is biztosít a Power BI prémium szintje: például gyakoribb frissítéseket, dedikált kapacitást és nagy modellméretet.

![Prémium szintű Power BI használata](media/service-admin-azure-ad-b2b/license-approach1.png)

### <a name="assign-power-bi-pro-license-to-guest-user"></a>Power BI Pro licenc hozzárendelése a vendégfelhasználóhoz

Ha a vendégfelhasználóhoz a bérlőn belül Power BI-Pro licencet rendel, a vendégfelhasználó meg fogja tudni tekinteni a tartalmat.

> [!NOTE]
> A bérlői Power BI Pro-licenccel a vendégfelhasználók csak a bérlőn tárolt tartalmakhoz férhetnek hozzá.

![Pro licenc hozzárendelése a bérlőről](media/service-admin-azure-ad-b2b/license-approach2.png)

### <a name="guest-user-brings-their-own-power-bi-pro-license"></a>A vendégfelhasználók hozzák saját Power BI Pro-licencüket

A vendégfelhasználó saját bérlőjén már rendelkezik Power BI Pro-licenccel.

![A vendégfelhasználók hozzák saját licencüket](media/service-admin-azure-ad-b2b/license-approach3.png)

## <a name="limitations"></a>Korlátozások

* A külső B2B-vendégeknek csak olvasási jogosultságuk van a tartalomhoz. A külső B2B-vendégek megtekinthetnek alkalmazásokat, irányítópultokat, jelentéseket, illetve adatokat exportálhatnak, és irányítópultokhoz és jelentésekhez kapcsolódó e-mail-értesítéseket hozhatnak létre. Nem férhetnek hozzá azonban munkaterületekhez, és nem tehetik közzé saját tartalmaikat.
* Ez a funkció jelenleg nem érhető el Power BI-mobilalkalmazásokban. Az Azure AD B2B-vel megosztott Power BI-tartalmakat a mobileszközén böngészőben tekintheti meg.
* A Power BI nem támogatja a vendégfelhasználókat független (kormányzati) felhőkben.

## <a name="next-steps"></a>További lépések

Ha részletesebb információkra van szüksége például a sorszintű adatvédelem működésével kapcsolatban, olvassa el ezt a [tanulmányt](https://aka.ms/powerbi-b2b-whitepaper).

Az Azure Active Directory B2B szolgáltatással kapcsolatban tekintse át a [Azure AD B2B együttműködésről](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b) szóló cikket.