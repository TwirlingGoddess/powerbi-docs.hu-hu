---
title: Sorszintű biztonság (RLS) a Power BI Desktoppal – összefoglaló
description: Az importált adatkészletek és a DirectQuery sorszintű biztonságának konfigurálása a Power BI Desktopban.
services: powerbi
documentationcenter: ''
author: markingmyname
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 05/03/2018
ms.author: maghan
LocalizationGroup: Create reports
ms.openlocfilehash: 0985aa06a76e93b1e437b53dae22146aa2a4598c
ms.sourcegitcommit: 50016425005d2e929c8c606c2d0d393342e05d39
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/12/2018
---
# <a name="row-level-security-rls-with-power-bi-desktop"></a>Sorszintű biztonság (RLS) a Power BI Desktoppal
A Power BI Desktoppal használható sorszintű biztonsági (RLS) funkció adott felhasználók adatokhoz való hozzáférésének korlátozására szolgál. A szűrők sorszinten korlátozzák az adatokat. A szűrőket a szerepkörökön belül adhatja meg.

Most már konfigurálhat RLS-t a Power BI Desktoppal a Power BI-be importált adatmodellekhez. Ezen kívül a DirectQueryt használó adatkészletekhez is konfigurálhat RLS-t, például az SQL Serverhez. Korábban csak a Power BI szolgáltatáson kívül, a helyszíni Analysis Services-modellekben lehetett RLS-t beállítani. Az Analysis Services élő kapcsolataihoz a helyszíni modellen konfigurálhatja a sorszintű biztonságot. Az élő kapcsolatok adatkészleteinél nem fog megjelenni a biztonsági beállítás.

> [!IMPORTANT]
> Ha szerepköröket és szabályokat adott meg a Power BI szolgáltatásban, újból létre kell hoznia ezeket a szerepköröket a Power BI Desktopon belül, és közzé kell tennie a jelentést a szolgáltatásban.
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

