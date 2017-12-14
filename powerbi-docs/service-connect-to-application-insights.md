---
title: "Csatlakozás az Application Insightshoz Csatlakozás a Power BI-hoz"
description: "Power BI-hoz készült Application Insights"
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: 3aa07c88daccc84bcf09af9d31a73a4411a3e541
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-application-insights-with-power-bi"></a>Csatlakozás az Application Insightshoz Power BI-jal
A Power BI használatával nagyszerű egyéni irányítópultokat hozhat létre az [Application Insights](https://azure.microsoft.com/documentation/articles/app-insights-overview/) telemetriai adataiból. Alkalmazásai telemetriai adatait újszerű módokon jelenítheti meg. Több alkalmazás vagy szolgáltatás mutatóit egyetlen irányítópulton egyesítheti. Az Application Insights-hoz készült Power BI tartalomcsomagnak ez az első kiadása. Olyan általánosan elterjedt, használati metrikákkal kapcsolatos widgeteket tartalmaz, mint például az aktív felhasználók száma, oldalmegtekintések, munkamenetek, böngésző- és operációsrendszer-verziók, valamint a felhasználók földrajzi eloszlása egy térképen.

Csatlakozzon a [Power BI-hoz készített Application Insights tartalomcsomaghoz](https://app.powerbi.com/getdata/services/application-insights).

>[!NOTE]
>Ahhoz, hogy csatlakozni tudjon, hozzáféréssel kell rendelkeznie az alkalmazáshoz tartozó Application Insights panelhez az Azure Betekintő portálon. A követelményekről alább talál további információt.

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
    ![Adatok lekérése gomb](media/service-connect-to-application-insights/pbi_getdata.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** gombra.
   
    ![Beolvasás gomb](media/service-connect-to-application-insights/pbi_getservices.png)
3. Kattintson az **Application Insights** > **Letöltés most** lehetőségre.
   
    ![Application Insights tartalomcsomag](media/service-connect-to-application-insights/appinsights.png)
4. Adja meg annak az alkalmazásnak az adatait az **Application Insights Resource name** (Application Insights-erőforrás neve), a **Resource Group** (Erőforráscsoport) és a **Subscription** (Előfizetés azonosító) paramétereknél, amelyhez csatlakozni szeretne. Ha ezzel kapcsolatban további információra van szüksége, tekintse át alább az [Application Insights paraméterek megkeresése](#FindingAppInsightsParams) részt.
   
    ![Application Insights-kapcsolat párbeszédpanel](media/service-connect-to-application-insights/pbi_contpkappinsitconnectndialog.png)    
5. Kattintson a **Sign In** (Bejelentkezés) lehetőségre, majd a csatlakozáshoz kövesse a képernyőn olvasható lépéseket.
   
    ![Application Insights-kapcsolat bejelentkezési párbeszédpanelje](media/service-connect-to-application-insights/pbi_contpkappinsitconnectn2.png)
6. Az importálás automatikusan megkezdődik. Amikor befejeződik, megjelenik egy értesítés, a navigációs ablaktáblán pedig megjelenik egy új irányítópult, jelentés és modell, egy csillaggal jelölve.  Az importált adatok megtekintéséhez válassza ki az irányítópultot.
   
    ![Application Insights irányítópult](media/service-connect-to-application-insights/pbi_contpkappinsitdash.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson az egyik csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adathalmaz naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, a **Frissítés** lehetőségre kattintva

## <a name="whats-included"></a>A csomag tartalma
Az Application Insights tartalomcsomag a következő táblákat és metrikákat tartalmazza:  

    - ApplicationDetails  
    - UniqueUsersLast7Days   
    - UniqueUsersLast30Days   
    - UniqueUsersLast30Days  
    - UniqueUsersByCountryLast7Days  
    - UniqueUsersByCountryLast30Days   
    - PageViewsDailyLast30Days   
    - SessionsLast7Days   
    - SessionsLast30Days  
    - PageViewsByBrowserVersionDailyLast30Days   
    - UniqueUsersByOperatingSystemLast7Days   
    - UniqueUsersByOperatingSystemLast30Days    
    - SessionsDailyLast30Days   
    - SessionsByCountryLast7Days   
    - SessionsByCountryLast30Days   
    - PageViewsByCountryDailyLast30Days   

<a name="FindingAppInsightsParams"></a>

## <a name="finding-parameters"></a>Keresési paraméterek
Mind a Resource Name (Erőforrás neve), mind a Resource Group (Erőforráscsoport) és a Subscription ID (Előfizetés azonosítója) megtalálhatók az Azure Portalon. Ha a névre (Name) kattint, a rendszer megjelenít egy részteles nézetet, és az „Essentials” (Alapvető erőforrások) legördülő listából kikeresheti azokat az értékeket, amelyekre szüksége van.

![Application Insights paraméterek](media/service-connect-to-application-insights/pbi_contpkappinsitparams.png)

Másolja ki és illessze be a használni kívánt értékeket a Power BI-hoz beadandó mezőkbe:

![Application Insights paraméterek](media/service-connect-to-application-insights/pbi_contpkappinsitparam2.png)

## <a name="next-steps"></a>Következő lépések
[Power BI - első lépések](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

