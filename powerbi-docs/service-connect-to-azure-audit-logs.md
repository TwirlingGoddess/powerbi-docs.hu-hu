---
title: Kapcsolódás Azure-auditnaplókhoz a Power BI-jal
description: Azure-auditnaplók a Power BI-hoz
services: powerbi
documentationcenter: ''
author: SarinaJoan
manager: kfile
backup: maggiesMSFT
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 02/06/2018
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: bb88ca524df5dd8c683c38a1a54a9bd626dad840
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="connect-to-azure-audit-logs-with-power-bi"></a>Kapcsolódás Azure-auditnaplókhoz a Power BI-jal
Az Azure-auditnaplók tartalomcsomagjával elemezheti és vizualizálhatja az auditnaplókban tárolt információt. A Power BI lekéri az adatait, előregyártott irányítópultot készít, és jelentéseket hoz létre az adatok alapján.

[Kapcsolódjon az Azure-auditnaplók tartalomcsomaghoz](https://app.powerbi.com/getdata/services/azure-audit-logs), vagy olvasson továbbiakat az [Azure-auditnaplók és a Power BI integrációjáról](https://powerbi.microsoft.com/integrations/azure-audit-logs).

## <a name="how-to-connect"></a>A csatlakozás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.  
   
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

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Noha az adatkészlet napi frissítésre van ütemezve, módosíthatja a frissítési ütemezést, vagy igény szerint frissíthet az **Azonnali frissítés** gombbal.

## <a name="system-requirements"></a>Rendszerkövetelmények
Az Azure-auditnaplók tartalomcsomagnak hozzáférésre van szüksége az auditnaplókhoz az Azure Portalon. A részleteket [itt](https://azure.microsoft.com/documentation/articles/insights-debugging-with-events/) találja.

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

