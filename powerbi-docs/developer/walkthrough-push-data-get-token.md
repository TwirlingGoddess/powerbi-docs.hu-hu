---
title: "Hitelesítési hozzáférési token beszerzése"
description: "Útmutatás az adatok leküldéséhez – Hitelesítéshez szükséges hozzáférési jogkivonat beszerzése"
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
ms.topic: get-started-article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/10/2017
ms.author: asaxton
ms.openlocfilehash: 068baa78315bfc7e4f7078ed47596a480dbe3765
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="step-2-get-an-authentication-access-token"></a>2. lépés: Hitelesítéshez szükséges hozzáférési jogkivonat beszerzése
Ez a cikk az [adatok az adatkészletekbe való küldését](walkthrough-push-data.md) ismertető részletes útmutató része.

Az adatok adatkészletbe történő leküldésének **1. lépésében** ([Alkalmazás regisztrálása az Azure AD-vel](walkthrough-push-data-register-app-with-azure-ad.md)) regisztrált egy ügyfélalkalmazást az Azure AD-ben. Ebben a lépésben hitelesítéshez szükséges hozzáférési jogkivonatot fogja beszerezni. A Power BI-alkalmazások integrálva vannak az **Azure AD**-vel, hogy biztonságos bejelentkezést és hitelesítést biztosítsanak az alkalmazáshoz. Az **Azure AD**-hitelesítéshez és a Power BI-erőforrásokhoz való hozzáféréshez jogkivonatokat használhat.

A továbbiakban ismertetjük, hogyan szerezhet be a hitelesítéshez szükséges hozzáférési jogkivonatot.

## <a name="get-an-authentication-access-token"></a>Hitelesítési hozzáférési token beszerzése
> **Megjegyzés**: Mielőtt elkezdené, győződjön meg arról, hogy követte az [adatok leküldése az adatkészletbe](walkthrough-push-data.md) bemutatóban található korábbi lépéseket.
> 
> 

1. A Visual Studio 2015-ben hozzon létre egy **Konzolalkalmazás** projektet.
2. Telepítse az [Azure AD Authentication Library for .NET NuGet csomagot](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/). Ha egy .NET-alkalmazásban szeretne beszerezni hitelesítéshez szükséges biztonsági jogkivonatot, használja ezt a csomagot. A csomagot az alábbiakban leírt módon telepítheti:
   
     a. A Visual Studio 2015-ben válassza a **Tools** (Eszközök) > **NuGet Package Manager** (NuGet-csomagkezelő) > **Package Manager Console** (Csomagkezelő konzol) elemet.
   
     b. A **csomagkezelő konzolban** lépjen be az Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612 elembe.
3. Adja az alábbi kódot a Program {...} osztályba.
4. Cserélje le a „{ClientID}” kifejezést az alkalmazás regisztrálásakor kapott **ügyfél-azonosítóra**. Lásd az [alkalmazás Azure AD-vel történő regisztrálását](walkthrough-push-data-register-app-with-azure-ad.md) ismertető cikket.
5. A Microsoft.IdentityModel.Clients.ActiveDirectory csomag telepítése után adja a **using Microsoft.IdentityModel.Clients.ActiveDirectory;** kifejezést a Program.cs fájlhoz.
6. Futtassa a Konzolalkalmazást, és jelentkezzen be a Power BI-fiókjába. A konzolablakban látnia kell egy jogkivonat-karakterláncot.

**Hitelesítéshez szükséges biztonsági jogkivonat beszerzésére szolgáló mintakód**

Adja ezt a kódot a Program {...} elemhez.

* Műveletek hívására szolgáló jogkivonat-változó:
  
  ```
  private static string token = string.Empty;
  
  static void Main(string[] args)
  {
  }
  ```
* Static void Main(string[] args):
  
  ```
  static void Main(string[] args)
  {
    //Get an authentication access token
    token = GetToken();
  }
  ```
* GetToken() metódus hozzáadása:

```
       #region Get an authentication access token
       private static string GetToken()
       {
           // TODO: Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612
           // and add using Microsoft.IdentityModel.Clients.ActiveDirectory

           //The client id that Azure AD created when you registered your client app.
           string clientID = "{Client_ID}";

           //RedirectUri you used when you register your app.
           //For a client app, a redirect uri gives Azure AD more details on the application that it will authenticate.
           // You can use this redirect uri for your client app
           string redirectUri = "https://login.live.com/oauth20_desktop.srf";

           //Resource Uri for Power BI API
           string resourceUri = "https://analysis.windows.net/powerbi/api";

           //OAuth2 authority Uri
           string authorityUri = "https://login.windows.net/common/oauth2/authorize";

           //Get access token:
           // To call a Power BI REST operation, create an instance of AuthenticationContext and call AcquireToken
           // AuthenticationContext is part of the Active Directory Authentication Library NuGet package
           // To install the Active Directory Authentication Library NuGet package in Visual Studio,
           //  run "Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory" from the nuget Package Manager Console.

           // AcquireToken will acquire an Azure access token
           // Call AcquireToken to get an Azure token from Azure Active Directory token issuance endpoint
           AuthenticationContext authContext = new AuthenticationContext(authorityUri);
           string token = authContext.AcquireToken(resourceUri, clientID, new Uri(redirectUri)).AccessToken;

           Console.WriteLine(token);
           Console.ReadLine();

           return token;
       }

       #endregion
```

A hitelesítési jogkivonat beszerzése után bármilyen Power BI-műveletet hívhat. A következő lépés bemutatja, hogyan hívhatja meg az [Adatkészlet létrehozása](https://msdn.microsoft.com/library/mt203562.aspx) műveletet adatkészlet létrehozásához, hogy képes legyen adatok leküldésére az irányítópultokra.

A következő lépés bemutatja, hogyan [hozhat létre adatkészletet a Power BI-ban](walkthrough-push-data-create-dataset.md).

Az alábbiakban megtalálja a [teljes kódlistát](#code).

<a name="code"/>

## <a name="complete-code-listing"></a>Teljes kódlista
    using System;
    using Microsoft.IdentityModel.Clients.ActiveDirectory;

    namespace walkthrough_push_data
    {
        class Program
        {
            private static string token = string.Empty;

            static void Main(string[] args)
            {

                //Get an authentication access token
                token = GetToken();

            }

            #region Get an authentication access token
            private static string GetToken()
            {
                // TODO: Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory -Version 2.21.301221612
                // and add using Microsoft.IdentityModel.Clients.ActiveDirectory

                //The client id that Azure AD created when you registered your client app.
                string clientID = "{Client_ID}";

                //RedirectUri you used when you register your app.
                //For a client app, a redirect uri gives Azure AD more details on the application that it will authenticate.
                // You can use this redirect uri for your client app
                string redirectUri = "https://login.live.com/oauth20_desktop.srf";

                //Resource Uri for Power BI API
                string resourceUri = "https://analysis.windows.net/powerbi/api";

                //OAuth2 authority Uri
                string authorityUri = "https://login.windows.net/common/oauth2/authorize";

                //Get access token:
                // To call a Power BI REST operation, create an instance of AuthenticationContext and call AcquireToken
                // AuthenticationContext is part of the Active Directory Authentication Library NuGet package
                // To install the Active Directory Authentication Library NuGet package in Visual Studio,
                //  run "Install-Package Microsoft.IdentityModel.Clients.ActiveDirectory" from the nuget Package Manager Console.

                // AcquireToken will acquire an Azure access token
                // Call AcquireToken to get an Azure token from Azure Active Directory token issuance endpoint
                AuthenticationContext authContext = new AuthenticationContext(authorityUri);
                string token = authContext.AcquireToken(resourceUri, clientID, new Uri(redirectUri)).AccessToken;

                Console.WriteLine(token);
                Console.ReadLine();

                return token;
            }

            #endregion

        }
    }


[Következő lépés >](walkthrough-push-data-create-dataset.md)

## <a name="next-steps"></a>Következő lépések
[Adatkészlet létrehozása a Power BI-ban](walkthrough-push-data-create-dataset.md)  
[Alkalmazás regisztrálása az Azure AD-ben](walkthrough-push-data-register-app-with-azure-ad.md)  
[Azure AD Authentication Library for .NET NuGet csomag](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/)  
[Adatok leküldése Power BI-adatkészletekbe](walkthrough-push-data.md)  
[A Power BI REST API áttekintése](overview-of-power-bi-rest-api.md)  
[A Power BI REST API-jainak leírása](https://msdn.microsoft.com/library/mt147898.aspx)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)
