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
ms.openlocfilehash: c2d8e22758e3d28a3851b99140876ff1646a6be0
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-troux-for-power-bi"></a>Csatlakozás a Troux-hoz a Power BI használatával
A Troux-tartalomcsomaggal teljesen új módon, közvetlenül a Power BI-ban jelenítheti meg a vállalati architektúra adattárát. A tartalomcsomag az üzleti képességekről, a képességeket biztosító alkalmazásokról, és az alkalmazásokat támogató technológiákról nyújt elemzéseket, amelyek a Power BI segítségével teljes körűen testre szabhatók.

Csatlakozzon a Power BI-hoz készült [Troux-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/troux).

## <a name="how-to-connect"></a>A csatlakozás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.
   
   ![](media/service-connect-to-troux/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-troux/services.png)
3. Kattintson a **Troux** \>  **Get** elemre.
   
   ![](media/service-connect-to-troux/troux.png)
4. Adja meg a Troux OData-csatornájának URL-címét. A [paraméterek megkereséséről](#FindingParams) alább olvashat részletesebben.
   
   ![](media/service-connect-to-troux/params.png)
5. **Hitelesítési módszerként** válassza az **Alapszintű** lehetőséget, adja meg a felhasználónevét és a jelszavát (figyeljen a kis- és nagybetűkre), majd kattintson a **Bejelentkezés** elemre.
   
    ![](media/service-connect-to-troux/creds.png)
6. A jóváhagyás után automatikusan megkezdődik az importálás. Ha befejeződött, a navigációs panelen megjelenik egy új irányítópult, jelentés és modell. Válassza ki az irányítópultot az importált adatok megtekintéséhez.
   
     ![](media/service-connect-to-troux/dashboard.png)

**Mi a következő lépés?**

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Noha az adatkészlet napi frissítésre van ütemezve, módosíthatja a frissítési ütemezést, vagy igény szerint frissíthet az **Azonnali frissítés** gombbal.

## <a name="system-requirements"></a>Rendszerkövetelmények
Hozzáférés szükséges a Troux OData-adatcsatornához és a Troux 9.5.1-es vagy újabb verziójához.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
Az egyedi Troux OData-adatcsatornája URL-címéért forduljon az Ügyféltámogatáshoz

## <a name="troubleshooting"></a>Hibaelhárítás
Ha a hitelesítő adatok megadása után időtúllépési hibát tapasztal, kísérelje meg újra a kapcsolódást.

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok lekérése a Power BI-ban](service-get-data.md)

