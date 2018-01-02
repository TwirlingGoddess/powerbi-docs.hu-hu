---
title: "Adatkészlet lekérése és sorok hozzáadása"
description: "Útmutatás az adatok leküldéséhez – Adatkészlet lekérése, és sorok hozzáadása egy Power BI-táblához"
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
ms.openlocfilehash: f0ca594b6f87ab2e186909f10a8ba4b7e1bce062
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="step-4-get-a-dataset-to-add-rows-into-a-power-bi-table"></a>4. lépés: Adatkészlet lekérése, és sorok hozzáadása egy Power BI-táblához
Ez a cikk az [adatok adatkészletbe történő leküldését](walkthrough-push-data.md) ismertető részletes útmutató része.

Az Adatok adatkészletbe való leküldésének **3. lépésében**, amelynek címe [Adatkészlet létrehozása a Power BI-ban](walkthrough-push-data-create-dataset.md), az [Adatkészlet létrehozása](https://msdn.microsoft.com/library/mt203562.aspx) művelet meghívásával létrehozott egy adatkészletet a Power BI-ban. Ebben a lépésben az [Adatkészletek lekérése](https://msdn.microsoft.com/library/mt203567.aspx) műveletet és a Newtonsoft.Jsont fogja használni az adatkészlet azonosítójának lekéréséhez. Az adatkészlet azonosítóját a 4. lépésben fogja használni, hogy sorokat adjon hozzá egy adatkészlethez. A Power BI REST API használatáról szóló példák a [Power BI REST API az Apiaryn](http://docs.powerbi.apiary.io/) című cikkben találhatók.

Ha adatokat szeretne elküldeni Power BI-adatkészletbe, akkor az adatkészletben hivatkoznia kell a táblára. Ha egy táblára kíván hivatkozni egy adatkészletben, először le kell kérnie az **Adatkészlet azonosítóját**. Az **adatkészlet azonosítójának** lekéréséhez használja az [Adatkészletek lekérése](https://msdn.microsoft.com/library/mt203567.aspx) műveletet. Az **Adatkészlet lekérése** művelet egy JSON-karakterláncot ad vissza, amely tartalmazza a Power BI-ban tárolt összes adatkészlet listáját. A JSON-karakterlánc deszerializálásának ajánlott módja a [Newtonsoft.JSON](http://www.newtonsoft.com/json) használata.

Az adatkészlet lekérésének menete:

## <a name="get-a-power-bi-dataset"></a>Power BI-adatkészlet lekérése
> **Megjegyzés**: Mielőtt elkezdené, győződjön meg arról, hogy követte az [adatok elküldése az adatkészletbe](walkthrough-push-data.md) bemutatóban található, korábbi lépéseket.
> 
> 

1. Az adatok elküldéséről szóló útmutató 2. lépésében ([Hitelesítéshez szükséges hozzáférési jogkivonat beszerzése](walkthrough-push-data-get-token.md)) létrehozott konzolalkalmazás-projektben telepítse a Newtonsoft.Json NuGet-csomagot. A csomagot az alábbiakban leírt módon telepítheti:
   
     a. A Visual Studio 2015-ben kattintson a **Tools** (Eszközök)  >  **NuGet Package Manager** (NuGet-csomagkezelő) > **Package Manager Console** (Csomagkezelő konzol) elemre.
   
     b. A **csomagkezelő konzolban** lépjen be az Install-Package Newtonsoft.Json elembe.
2. A csomag telepítése után adja hozzá a **using NewtonsoftJson;** karakterláncot a Program.cs fájlhoz.
3. Az **Adatkészlet azonosítójának** lekéréséhez adja hozzá a Program.cs fájlhoz az alábbi kódot.
4. Futtassa a Konzolalkalmazást, és jelentkezzen a Power BI-fiókjába. A konzolablakban megjelenik az **Adatkészlet azonosítója:** mező, amelyet egy azonosító követ.

**Adatkészlet-lekérési minta**

Adja hozzá ezt a kódot a Program.cs fájlhoz.

* Static void Main(string[] args):
  
  ```
  static void Main(string[] args)
  {
  
    //Get an authentication access token
    token = GetToken();
  
    //Create a dataset in Power BI
    CreateDataset();
  
    //Get a dataset to add rows into a Power BI table
    string datasetId = GetDataset();
  }
  ```
* Adjon hozzá egy GetDataset() metódust:
  
  ```
    #region Get a dataset to add rows into a Power BI table
    private static string GetDataset()
    {
        string powerBIDatasetsApiUrl = "https://api.powerbi.com/v1.0/myorg/datasets";
        //POST web request to create a dataset.
        //To create a Dataset in a group, use the Groups uri: https://api.PowerBI.com/v1.0/myorg/groups/{group_id}/datasets
        HttpWebRequest request = System.Net.WebRequest.Create(powerBIDatasetsApiUrl) as System.Net.HttpWebRequest;
        request.KeepAlive = true;
        request.Method = "GET";
        request.ContentLength = 0;
        request.ContentType = "application/json";
  
        //Add token to the request header
        request.Headers.Add("Authorization", String.Format("Bearer {0}", token));
  
        string datasetId = string.Empty;
        //Get HttpWebResponse from GET request
        using (HttpWebResponse httpResponse = request.GetResponse() as System.Net.HttpWebResponse)
        {
            //Get StreamReader that holds the response stream
            using (StreamReader reader = new System.IO.StreamReader(httpResponse.GetResponseStream()))
            {
                string responseContent = reader.ReadToEnd();
  
                //TODO: Install NuGet Newtonsoft.Json package: Install-Package Newtonsoft.Json
                //and add using Newtonsoft.Json
                var results = JsonConvert.DeserializeObject<dynamic>(responseContent);
  
                //Get the first id
                datasetId = results["value"][0]["id"];
  
                Console.WriteLine(String.Format("Dataset ID: {0}", datasetId));
                Console.ReadLine();
  
                return datasetId;
            }
        }
    }
    #endregion
  ```

A következő lépés bemutatja, [hogyan adhat hozzá sorokat a Power BI-táblákhoz](walkthrough-push-data-add-rows.md).

Az alábbiakban megtalálja a [teljes kódlistát](#code).

<a name="code"/>

## <a name="complete-code-listing"></a>Teljes kódlista
    using System;
    using Microsoft.IdentityModel.Clients.ActiveDirectory;
    using System.Net;
    using System.IO;
    using Newtonsoft.Json;

    namespace walkthrough_push_data
    {
        class Program
        {
            private static string token = string.Empty;

            static void Main(string[] args)
            {

                //Get an authentication access token
                token = GetToken();

                //Create a dataset in Power BI
                CreateDataset();

                //Get a dataset to add rows into a Power BI table
                string datasetId = GetDataset();

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

            #region Create a dataset in Power BI
            private static void CreateDataset()
            {
                //TODO: Add using System.Net and using System.IO

                string powerBIDatasetsApiUrl = "https://api.powerbi.com/v1.0/myorg/datasets";
                //POST web request to create a dataset.
                //To create a Dataset in a group, use the Groups uri: https://api.PowerBI.com/v1.0/myorg/groups/{group_id}/datasets
                HttpWebRequest request = System.Net.WebRequest.Create(powerBIDatasetsApiUrl) as System.Net.HttpWebRequest;
                request.KeepAlive = true;
                request.Method = "POST";
                request.ContentLength = 0;
                request.ContentType = "application/json";

                //Add token to the request header
                request.Headers.Add("Authorization", String.Format("Bearer {0}", token));

                //Create dataset JSON for POST request
                string datasetJson = "{\"name\": \"SalesMarketing\", \"tables\": " +
                    "[{\"name\": \"Product\", \"columns\": " +
                    "[{ \"name\": \"ProductID\", \"dataType\": \"Int64\"}, " +
                    "{ \"name\": \"Name\", \"dataType\": \"string\"}, " +
                    "{ \"name\": \"Category\", \"dataType\": \"string\"}," +
                    "{ \"name\": \"IsCompete\", \"dataType\": \"bool\"}," +
                    "{ \"name\": \"ManufacturedOn\", \"dataType\": \"DateTime\"}" +
                    "]}]}";

                //POST web request
                byte[] byteArray = System.Text.Encoding.UTF8.GetBytes(datasetJson);
                request.ContentLength = byteArray.Length;

                //Write JSON byte[] into a Stream
                using (Stream writer = request.GetRequestStream())
                {
                    writer.Write(byteArray, 0, byteArray.Length);

                    var response = (HttpWebResponse)request.GetResponse();

                    Console.WriteLine(string.Format("Dataset {0}", response.StatusCode.ToString()));

                    Console.ReadLine();
                }
            }
            #endregion

            #region Get a dataset to add rows into a Power BI table
            private static string GetDataset()
            {
                string powerBIDatasetsApiUrl = "https://api.powerbi.com/v1.0/myorg/datasets";
                //POST web request to create a dataset.
                //To create a Dataset in a group, use the Groups uri: https://api.PowerBI.com/v1.0/myorg/groups/{group_id}/datasets
                HttpWebRequest request = System.Net.WebRequest.Create(powerBIDatasetsApiUrl) as System.Net.HttpWebRequest;
                request.KeepAlive = true;
                request.Method = "GET";
                request.ContentLength = 0;
                request.ContentType = "application/json";

                //Add token to the request header
                request.Headers.Add("Authorization", String.Format("Bearer {0}", token));

                string datasetId = string.Empty;
                //Get HttpWebResponse from GET request
                using (HttpWebResponse httpResponse = request.GetResponse() as System.Net.HttpWebResponse)
                {
                    //Get StreamReader that holds the response stream
                    using (StreamReader reader = new System.IO.StreamReader(httpResponse.GetResponseStream()))
                    {
                        string responseContent = reader.ReadToEnd();

                        //TODO: Install NuGet Newtonsoft.Json package: Install-Package Newtonsoft.Json
                        //and add using Newtonsoft.Json
                        var results = JsonConvert.DeserializeObject<dynamic>(responseContent);

                        //Get the first id
                        datasetId = results["value"][0]["id"];

                        Console.WriteLine(String.Format("Dataset ID: {0}", datasetId));
                        Console.ReadLine();

                        return datasetId;
                    }
                }
            }
            #endregion
        }
    }

[Következő lépés >](walkthrough-push-data-add-rows.md)

## <a name="next-steps"></a>Következő lépések
[Sorok hozzáadása egy Power BI-táblához](walkthrough-push-data-add-rows.md)  
[Newtonsoft.Json](http://www.newtonsoft.com/json)  
[Adatkészletek lekérése](https://msdn.microsoft.com/library/mt203567.aspx)  
[Adatok leküldése a Power BI-ba](walkthrough-push-data.md)  
[A Power BI REST API áttekintése](overview-of-power-bi-rest-api.md)  
[A Power BI REST API-jainak leírása](https://msdn.microsoft.com/library/mt147898.aspx)  
[Power BI REST API az APIARY-n](http://docs.powerbi.apiary.io/)  

További kérdései vannak? [Forduljon a Power BI közösségéhez](http://community.powerbi.com/)

