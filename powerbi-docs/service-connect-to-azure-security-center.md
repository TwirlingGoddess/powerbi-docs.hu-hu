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
ms.openlocfilehash: d052bc054e55eabfab53ad3b1ac9229f0a750785
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-azure-security-center-with-power-bi"></a>Csatlakozás az Azure Security Centerhez a Power BI használatával
Az Azure Security-adatok Power BI-ba történő csatlakoztatásával elemzési adatokat nyerhet az Azure-beli számítási feladatok biztonságáról. Az Azure Security Center adatai alapján a Power BI automatikusan létrehoz egy irányítópultot és egy jelentést, amely lehetővé teszi az adatok elemzését és feltárását.

Kapcsolódjon a Power BI-hoz készült [Azure Security Center-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/azure-security-center).

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
   ![](media/service-connect-to-azure-security-center/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-azure-security-center/services.png)
3. Kattintson az **Azure Security Center** \> **Get** elemre.
   
   ![](media/service-connect-to-azure-security-center/asc.png)
4. Adja meg az előfizetési kulcsot. A [paraméterek megkereséséről](#FindingParams) alább olvashat részletesebben.
   
   ![](media/service-connect-to-azure-security-center/params.png)
5. A **Hitelesítési módszer** beállításánál válassza az **oAuth2** \> **Bejelentkezés** lehetőséget. Amikor a rendszer kéri, adja meg az Azure-fiókja hitelesítő adatait.
   
    ![](media/service-connect-to-azure-security-center/creds.png)
6. A jóváhagyás után automatikusan elkezdődik az importálás. Amikor befejeződik, a navigációs ablaktáblán megjelenik egy új irányítópult, jelentés és modell. Kattintson az irányítópultra az importált adatok megtekintéséhez.
   
     ![](media/service-connect-to-azure-security-center/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

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

[Adatok lekérdezése a Power BI-ban](service-get-data.md)

