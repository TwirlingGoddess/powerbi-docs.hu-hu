---
title: "Csatlakozás az Azure Security Centerhez a Power BI használatával"
description: Azure Security Center a Power BI-hoz
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
ms.openlocfilehash: e26a26d7cba2ae3d68586a2e0dcdf87481009bd6
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-azure-security-center-with-power-bi"></a>Csatlakozás az Azure Security Centerhez a Power BI használatával
Az Azure Security-adatok Power BI-ba történő csatlakoztatásával elemzési adatokat nyerhet az Azure-beli számítási feladatok biztonságáról. Az Azure Security Center adatai alapján a Power BI automatikusan létrehoz egy irányítópultot és egy jelentést, amely lehetővé teszi az adatok elemzését és feltárását.

Kapcsolódjon a Power BI-hoz készült [Azure Security Center-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/azure-security-center).

## <a name="how-to-connect"></a>A csatlakozás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.
   
   ![](media/service-connect-to-azure-security-center/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-azure-security-center/services.png)
3. Kattintson az **Azure Security Center** \> **Get** elemre.
   
   ![](media/service-connect-to-azure-security-center/asc.png)
4. Adja meg az előfizetési kulcsot. A [paraméterek megkereséséről](#FindingParams) alább olvashat részletesebben.
   
   ![](media/service-connect-to-azure-security-center/params.png)
5. A **Hitelesítési módszer** beállításánál válassza az **oAuth2** \> **Bejelentkezés** lehetőséget. Amikor a rendszer kéri, adja meg az Azure-fiókja hitelesítő adatait.
   
    ![](media/service-connect-to-azure-security-center/creds.png)
6. A jóváhagyás után automatikusan elkezdődik az importálás. Ha befejeződött, a navigációs panelen megjelenik egy új irányítópult, jelentés és modell. Válassza ki az irányítópultot az importált adatok megtekintéséhez.
   
     ![](media/service-connect-to-azure-security-center/dashboard.png)

**Mi a következő lépés?**

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Noha az adatkészlet napi frissítésre van ütemezve, módosíthatja a frissítési ütemezést, vagy igény szerint frissíthet az **Azonnali frissítés** gombbal.

## <a name="whats-included"></a>A csomag tartalma
A tartalomcsomag az erőforrások biztonsági állapotáról, a riasztási elemzésekről és a megelőzési elemzésekről tartalmaz információkat.

## <a name="system-requirements"></a>Rendszerkövetelmények
A tartalomcsomag használatához szükség van a hozzáférésre egy előfizetés-azonosítóhoz, amelyen engedélyezve van az Azure Security Center. További információkért keresse fel az [Azure Security Centert](https://portal.azure.com/#blade/Microsoft_Azure_Security/SecurityDashboardStartBladeV2) az Azure Portalon.

A tartalomcsomag használatához arra is szükség van, hogy a felhasználó céges (nem személyes) fiókkal kapcsolódjon.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
Az előfizetés-azonosítót két egyszerű módon találhatja meg.

1. A https://portal.azure.com helyről -&gt; Tallózás -&gt; Előfizetések -&gt; Előfizetés-azonosító
2. A https://manage.windowsazure.com helyről -&gt; Beállítások -&gt; Előfizetési azonosító

Az előfizetés-azonosító egy hosszú betű- és számsor, ami a fenti \#4. lépésben láthatóhoz hasonlít. 

## <a name="troubleshooting"></a>Hibaelhárítás
Az adatok betöltése a fiók méretétől függően időbe telhet. Ha a bejelentkezés során hibát észlel, győződjön meg róla, hogy helyesek-e a paraméterek, és a fiókján engedélyezve van-e az Azure Security Center.

Ha a tartalomcsomag betöltődik, de nem jeleníti meg az adatokat, ellenőrizze, hogy céges fiókkal kapcsolódott-e. Bár az Azure Security Center támogatja a személyes fiókokat, az API (és ennélfogva a tartalomcsomag) csak akkor adja vissza az elvárás szerinti értékeket, ha a felhasználó céges fiókkal kapcsolódik. Adjon hozzáférést egy céges fiókhoz, és kísérelje meg újra a csatlakozást.

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok lekérése a Power BI-ban](service-get-data.md)

