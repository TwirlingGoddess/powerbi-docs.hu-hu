---
title: "Sorszintű biztonság (RLS) a Power BI Desktoppal – összefoglaló"
description: "Az importált adatkészletek és a DirectQuery sorszintű biztonságának konfigurálása a Power BI Desktopban."
services: powerbi
documentationcenter: 
author: markingmyname
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 10/12/2017
ms.author: maghan
ms.openlocfilehash: fccb2094158ed2dffaa0a80cc5609dfbf382be30
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/30/2018
---
# <a name="row-level-security-rls-with-power-bi-desktop"></a>Sorszintű biztonság (RLS) a Power BI Desktoppal
A sorszintű biztonság (RLS) a Power BI Desktoppal adott felhasználók adatokhoz való hozzáférésének korlátozására használható. A szűrők sorszinten korlátozzák az adatokat. A szűrőket a szerepkörökön belül adhatja meg.

Most már konfigurálhat RLS-t a Power BI Desktoppal a Power BI-be importált adatmodellekhez. Ezen kívül a DirectQueryt használó adatkészletekhez is konfigurálhat RLS-t, például az SQL Serverhez. Korábban csak a Power BI szolgáltatáson kívül, a helyszíni Analysis Services-modellekben lehetett RLS-t beállítani. Az Analysis Services élő kapcsolataihoz a helyszíni modellen konfigurálhatja a sorszintű biztonságot. A biztonság lehetőség nem fog megjelenni az elő kapcsolattal rendelkező adatkészleteknél.

> [!IMPORTANT]
> Ha szerepköröket/szabályokat adott meg a Power BI szolgáltatásban, újból létre kell hoznia ezeket a szerepköröket a Power BI Desktopon belül, és közzé kell tennie a jelentést a szolgáltatáshoz.
> 
> 

További információk az [RLS beállításairól a Power BI szolgáltatásban](service-admin-rls.md).

[!INCLUDE [include-short-name](./includes/rls-desktop-define-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-desktop-view-as-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-limitations.md)]

[!INCLUDE [include-short-name](./includes/rls-faq.md)]

## <a name="next-steps"></a>További lépések
[Sorszintű biztonság (RLS) a Power BI szolgáltatással](service-admin-rls.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

