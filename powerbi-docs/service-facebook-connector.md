---
title: "Külső szolgáltatás: Facebook-összekötő a Power BI Desktophoz"
description: "Külső szolgáltatás: Facebook-összekötő a Power BI Desktophoz"
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 02/22/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 894791ddc4eb632ad4dc0ee55f19bbadad5e28d6
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="facebook-connector-for-power-bi-desktop"></a>Facebook-összekötő a Power BI Desktophoz
A **Power BI Desktop** Facebook-összekötője a Facebook Graph API-ra támaszkodik, ezért az idő során változhatnak a funkciók, és módosulhat az elérhetőség.

Tekintse meg [a Power BI Desktophoz készült Facebook-összekötő útmutatóját](desktop-tutorial-facebook-analytics.md).

A Facebook Graph API 1.0-s verziója 2015. április 30-án lejárt. A Power BI a Facebook-összekötő hátterében működő Graph API-t használja az adatokhoz történő csatlakozáshoz és az adatelemzéshez.

Lehet, hogy a 2015. április 30. előtt készült lekérdezések már nem működnek, vagy kevesebb adatot adnak vissza. 2015. április 30<sup></sup>. óta a Power BI a Facebook API-ra érkező összes híváshoz a 2.8-as verziót használja. Ha a lekérdezése 2015. április 30. előtt készült, és azóta nem használta, valószínűleg újra kell hitelesítenie, hogy jóváhagyást kapjon az általunk kért új engedélyekre.

Bár minden változást igyekszünk követni a frissítések kibocsátásával, az API esetleges módosulásai befolyásolhatják az általunk létrehozott lekérdezések eredményeit. Egyes esetekben előfordulhat, hogy bizonyos lekérdezések már nem kapnak támogatást. E függőség miatt az említett összekötő használata esetén nem garantálhatjuk az eredményes lekérdezéseket.

A Facebook API változásáról további részleteket tekinthet meg [itt](https://developers.facebook.com/docs/apps/changelog#v2_0).

