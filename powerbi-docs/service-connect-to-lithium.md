---
title: "Kapcsolódás a Power BI-ból a Lithiumhoz"
description: Lithium a Power BI-hoz
services: powerbi
documentationcenter: 
author: SarinaJoan
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
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 501395503ef3c4b3bde8e6d7f0ae732af5a4cc6a
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="connect-to-lithium-with-power-bi"></a>Kapcsolódás a Power BI-ból a Lithiumhoz
A Lithium megbízható kapcsolatokat épít ki a világ legjobb márkái és az ügyfeleik között, és segít az embereknek választ kapni a kérdéseikre és megosztani a tapasztalataikat. Ha csatlakoztatja a Lithium-tartalomcsomagot a Power BI-hoz, akkor mérni tudja az online közössége legfontosabb metrikáit, így serkentheti az eladásokat, csökkentheti a szolgáltatási díjakat és növelheti ügyfelei hűségét. 

Kapcsolódjon a Power BI-hoz készült [Lithium-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/lithium).

>[!NOTE]
>A Power BI-tartalomcsomag a Lithium API-t használja. A túlzottan sok API-hívás további költségeket vonhat maga után a Lithium oldaláról. Kérjük, egyeztessen a Lithium-rendszergazdájával.

## <a name="how-to-connect"></a>A kapcsolódás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.
   
   ![](media/service-connect-to-lithium/pbi_getdata.png) 
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-lithium/pbi_getservices.png) 
3. Válassza a **Lithium** \> **Beolvasás** lehetőséget.
   
   ![](media/service-connect-to-lithium/lithiumconnect.png)
4. Adja meg a Lithium-közössége URL-címét. Ez *https://community.yoursite.com* formájú lesz.
   
   ![](media/service-connect-to-lithium/params.png)
5. Amikor a rendszer kéri, adja meg a Lithium-fiókja hitelesítő adatait. Válassza ki az **oAuth 2** hitelesítési mechanizmust, kattintson a **Bejelentkezés** elemre, majd kövesse a Lithium-fiók hitelesítési folyamatát.
   
   ![](media/service-connect-to-lithium/creds.png)
   
   ![](media/service-connect-to-lithium/creds2.png)
6. A sikeres bejelentkezési folyamat után megkezdődik az importálási folyamat. Ha befejeződött, a navigációs panelen megjelenik egy új irányítópult, jelentés és modell. Válassza ki az irányítópultot az importált adatok megtekintéséhez.
   
    ![](media/service-connect-to-lithium/lithium.png)

**Mi a következő lépés?**

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Noha az adatkészlet napi frissítésre van ütemezve, módosíthatja a frissítési ütemezést, vagy igény szerint frissíthet az **Azonnali frissítés** gombbal.

## <a name="system-requirements"></a>Rendszerkövetelmények
A Lithium-tartalomcsomaghoz 15.9-es vagy újabb verziójú Lithium-közösség szükséges. A verzió megerősítéséhez, kérjük, egyeztessen Lithium-rendszergazdájával.

## <a name="next-steps"></a>Következő lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

