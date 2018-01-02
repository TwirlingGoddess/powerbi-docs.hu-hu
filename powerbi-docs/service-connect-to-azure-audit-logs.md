---
title: "Kapcsolódás Azure-auditnaplókhoz a Power BI-jal"
description: "Azure-auditnaplók a Power BI-hoz"
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
ms.openlocfilehash: cb52b8dc6aefc199ef09946bf8b58c98171c5aba
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-azure-audit-logs-with-power-bi"></a>Kapcsolódás Azure-auditnaplókhoz a Power BI-jal
Az Azure-auditnaplók tartalomcsomagjával elemezheti és vizualizálhatja az auditnaplókban tárolt információt. A Power BI lekéri az adatait, előregyártott irányítópultot készít, és jelentéseket hoz létre az adatok alapján.

[Kapcsolódjon az Azure-auditnaplók tartalomcsomaghoz](https://app.powerbi.com/getdata/services/azure-audit-logs), vagy olvasson továbbiakat az [Azure-auditnaplók és a Power BI integrációjáról](https://powerbi.microsoft.com/integrations/azure-audit-logs).

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.  
   
    ![](media/service-connect-to-azure-audit-logs/getdata.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** gombra.  
   
    ![](media/service-connect-to-azure-audit-logs/services.png) 
3. Kattintson az **Azure-auditnaplók** > **Beolvasás** gombra.  
   
   ![](media/service-connect-to-azure-audit-logs/azureauditlogs.png)
4. Amikor az alkalmazás kéri, adja meg az **Azure-beli előfizetés-azonosítóját**. Az [előfizetés-azonosító](#FindingParams) megkereséséről az alábbiakban olvashat részletesen.   
   
    ![](media/service-connect-to-azure-audit-logs/parameters.png)
5. A **Hitelesítési módszer** beállításánál válassza az **oAuth2** \> **Bejelentkezés** lehetőséget.
   
    ![](media/service-connect-to-azure-audit-logs/creds.png)
6. A bejelentkezési folyamat befejezéséhez adja meg a fiók hitelesítő adatait.
   
    ![](media/service-connect-to-azure-audit-logs/login.png)
7. A Power BI le fogja tölteni az Azure-auditnapló adatait, és használatra kész irányítópultot és jelentést hoz létre. 
   
    ![](media/service-connect-to-azure-audit-logs/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található.
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson az egyik csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="system-requirements"></a>Rendszerkövetelmények
Az Azure-auditnaplók tartalomcsomagnak hozzáférésre van szüksége az auditnaplókhoz az Azure Portalon. A részleteket [itt](https://azure.microsoft.com/en-us/documentation/articles/insights-debugging-with-events/) találja.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
Az előfizetés-azonosítót két egyszerű módon találhatja meg.

1. A https://portal.azure.com helyről -&gt; Tallózás -&gt; Előfizetések -&gt; Előfizetés-azonosító
2. A https://manage.windowsazure.com helyről -&gt; Beállítások -&gt; Előfizetési azonosító

Az előfizetés-azonosító egy hosszú betű- és számsor, ami a fenti \#4. lépésben láthatóhoz hasonlít. 

## <a name="troubleshooting"></a>Hibaelhárítás
Ha hitelesítési hibát tapasztal vagy frissítési próbálkozáskor érvénytelen hitelesítő adatok miatti hibát, akkor próbálja törölni az Azure-auditnaplók tartalomcsomag összes példányát, és próbáljon újrakapcsolódni.

## <a name="next-steps"></a>Következő lépések
[Első lépések a Power BI-ban](service-get-started.md)  
[Power BI – Alapfogalmak](service-basic-concepts.md)  

