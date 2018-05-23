---
title: Az Azure SQL Database ütemezett frissítésének hibaelhárítása
description: Az Azure SQL Database ütemezett frissítésének hibaelhárítása a Power BI-ban
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 12/06/2017
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 9439ac6bd0b4df568b964f548372fb94d2fd0b26
ms.sourcegitcommit: 998b79c0dd46d0e5439888b83999945ed1809c94
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
---
# <a name="troubleshooting-scheduled-refresh-for-azure-sql-databases-in-power-bi"></a>Az Azure SQL Database ütemezett frissítésének hibaelhárítása a Power BI-ban
Az ütemezett frissítés beállításának részletes leírásáért tekintse meg az [adatok a Power BI-ban történő frissítését](refresh-data.md) ismertető témakört.

Amikor ütemezett frissítést hoz létre egy Azure SQL Database-hez, és 400-as számú hibaüzenetet kap a hitelesítő adatok szerkesztése során, a következő módon állíthatja be a megfelelő tűzfalszabályt:

1. Jelentkezzen be az Azure felügyeleti portálján.
2. Keresse meg azt az Azure SQL Servert, amelyhez be kívánja állítani a frissítést.
3. Jelölje be a „Windows Azure-szolgáltatások” elemet az engedélyezett szolgáltatások szakaszában.

![](media/service-admin-troubleshooting-scheduled-refresh-azure-sql-databases/azurerefresh.png)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

