---
title: "Az Azure SQL Database ütemezett frissítésének hibaelhárítása"
description: "Az Azure SQL Database ütemezett frissítésének hibaelhárítása a Power BI-ban"
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: ff219e3032837e91f3c63e0c08f3abd1121e72ff
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="troubleshooting-scheduled-refresh-for-azure-sql-databases-in-power-bi"></a>Az Azure SQL Database ütemezett frissítésének hibaelhárítása a Power BI-ban
Az ütemezett frissítés beállításának részletes leírásáért tekintse meg az [adatok a Power BI-ban történő frissítését](refresh-data.md) ismertető témakört.

Amikor ütemezett frissítést hoz létre egy Azure SQL Database-hez, és 400-as számú hibaüzenetet kap a hitelesítő adatok szerkesztése során, a következő módon állíthatja be a megfelelő tűzfalszabályt:

1. Jelentkezzen be az Azure felügyeleti portálján.
2. Keresse meg azt az Azure SQL Servert, amelyhez be kívánja állítani a frissítést.
3. Jelölje be a „Windows Azure-szolgáltatások” elemet az engedélyezett szolgáltatások szakaszában.

![](media/service-admin-troubleshooting-scheduled-refresh-azure-sql-databases/azurerefresh.png)  

További kérdései vannak? [Forduljon a Power BI közösségéhez](http://community.powerbi.com/)

