---
title: "Az SQL Server Analysis Services élő adatai a Power BI-ban"
description: "Az SQL Server Analysis Services élő adatai a Power BI-ban. Ez egy vállalati átjáróhoz konfigurált adatforrásban történik."
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
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/10/2017
ms.author: asaxton
ms.openlocfilehash: 6925dc9bcf3e500af18cf63c62f6cb33c297392b
ms.sourcegitcommit: b3ee37e1587f1269ee7dd9daf1685a06dea3b50c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/23/2017
---
# <a name="sql-server-analysis-services-live-data-in-power-bi"></a>Az SQL Server Analysis Services élő adatai a Power BI-ban
A Power BI szolgáltatásban kétféleképpen csatlakozhat egy SQL Server Analysis Services-kiszolgálóhoz. Az **Adatok lekérése** lehetőséggel csatlakozhat egy SQL Server Analysis Services-kiszolgálóhoz, vagy egy [Power BI Desktop-fájlhoz](service-desktop-files.md), vagy egy olyan [Excel-munkafüzethez](service-excel-workbook-files.md), amely már csatlakozik egy Analysis Services-kiszolgálóhoz.

 >[!IMPORTANT]
 >* Egy élő Analysis Services-kiszolgálóhoz való csatlakozáshoz egy rendszergazdának egy helyszíni adatátjárót kell telepítenie és konfigurálnia. További információ: [Helyszíni adatátjáró](service-gateway-onprem.md).
 >* Az átjáró használatakor az adatok a helyszínen maradnak.  Az adatok alapján létrehozott jelentéseket menti a Power BI szolgáltatás. 
 >* [A Q&A természetes nyelvű lekérdezés](service-q-and-a-direct-query.md) jelenleg előzetes verzióban érhető el az Analysis Services élő kapcsolataihoz.

## <a name="to-connect-to-a-model-from-get-data"></a>Csatlakozás egy modellhez az Adatok lekérése funkcióval
1. A **Saját munkaterületen** válassza az**Adatok lekérése** lehetőséget. Amennyiben elérhető, egy csoportos munkaterületre is válthat.
   
   ![](media/sql-server-analysis-services-tabular-data/connecttoas_getdatabutton.png)
2. Válassza az **Adatbázisok és továbbiak** lehetőséget.
   
   ![](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_1.png)
3. Válassza az **SQL Server Analysis Services** > **Csatlakozás** lehetőséget. 
   
   ![](media/sql-server-analysis-services-tabular-data/connecttoas_getdata_2.png)
4. Válasszon egy kiszolgálót. Ha nem lát egy kiszolgálót sem, akkor vagy egy átjáró vagy egy adatforrás nincs konfigurálva, vagy a fiókja nem szerepel az adatforrás **Felhasználók** lapján az átjáróban. Kérje a rendszergazda segítségét.
5. Válassza ki, melyik modellhez szeretne csatlakozni. Ez lehet egy táblázatos vagy többdimenziós típus.

Miután csatlakozott a modellhez, az megjelenik a saját Power BI-webhelyén a **Saját munkaterület/Adatkészletek** területen. Ha csoportos munkaterületre váltott, az adatkészlet a csoporton belül jelenik meg.

![](media/sql-server-analysis-services-tabular-data/connecttoas_dataset_5.png)

## <a name="dashboard-tiles"></a>Irányítópult csempéi
Ha vizualizációkat rögzít egy jelentésből az irányítópultra, a rögzített csempék 10 percenként automatikusan frissülnek. Ha frissülnek a helyszíni Analysis Services-adatok, a csempék 10 perc elteltével automatikusan frissülnek.

## <a name="next-steps"></a>Következő lépések
[Helyszíni adatátjáró](service-gateway-onprem.md)  
[Az Analysis Services adatforrásainak kezelése](service-gateway-enterprise-manage-ssas.md)  
[A helyszíni átjáró hibaelhárítása](service-gateway-onprem-tshoot.md)  
Több kérdése van? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

