---
title: "Csatlakozás a Troux-hoz a Power BI használatával"
description: Troux a Power BI-hoz
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
ms.openlocfilehash: ec225639ed23f57735081d556c1ac3283dc4d691
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-troux-for-power-bi"></a>Csatlakozás a Troux-hoz a Power BI használatával
A Troux-tartalomcsomaggal teljesen új módon, közvetlenül a Power BI-ban jelenítheti meg a vállalati architektúra adattárát. A tartalomcsomag az üzleti képességekről, a képességeket biztosító alkalmazásokról, és az alkalmazásokat támogató technológiákról nyújt elemzéseket, amelyek a Power BI segítségével teljes körűen testre szabhatók.

Csatlakozzon a Power BI-hoz készült [Troux-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/troux).

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
   ![](media/service-connect-to-troux/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-troux/services.png)
3. Kattintson a **Troux** \>  **Get** elemre.
   
   ![](media/service-connect-to-troux/troux.png)
4. Adja meg a Troux OData-csatornájának URL-címét. A [paraméterek megkereséséről](#FindingParams) alább olvashat részletesebben.
   
   ![](media/service-connect-to-troux/params.png)
5. **Hitelesítési módszerként** válassza az **Alapszintű** lehetőséget, adja meg a felhasználónevét és a jelszavát (figyeljen a kis- és nagybetűkre), majd kattintson a **Bejelentkezés** elemre.
   
    ![](media/service-connect-to-troux/creds.png)
6. A jóváhagyás után automatikusan megkezdődik az importálás. Amikor befejeződik, a navigációs ablaktáblán megjelenik egy új irányítópult, jelentés és modell. Az importált adatok megtekintéséhez kattintson az irányítópultra.
   
     ![](media/service-connect-to-troux/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="system-requirements"></a>Rendszerkövetelmények
Hozzáférés szükséges a Troux OData-adatcsatornához és a Troux 9.5.1-es vagy újabb verziójához.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
Az egyedi Troux OData-adatcsatornája URL-címéért forduljon az Ügyféltámogatáshoz

## <a name="troubleshooting"></a>Hibaelhárítás
Ha a hitelesítő adatok megadása után időtúllépési hibát tapasztal, kísérelje meg újra a kapcsolódást.

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

