---
title: "A Power BI Desktop bejelentkezési űrlapjának rendszergazdák általi kezelése"
description: "Tudja meg, hogyan kezelheti a Power BI Desktop első megnyitásakor megjelenő bejelentkezési űrlapot."
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
ms.date: 01/24/2018
ms.author: davidi
ms.openlocfilehash: 519f8b56b5086292addf577d969a707a6d6efcc8
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/25/2018
---
# <a name="how-administrators-can-manage-the-power-bi-desktop-sign-in-form"></a>A Power BI Desktop bejelentkezési űrlapjának rendszergazdák általi kezelése
A Power BI Desktop első indításakor megjelenik egy bejelentkezési űrlap. Ki kell tölteni, vagy be kell jelentkezni a Power BI szolgáltatásba a folytatáshoz. A rendszergazdák egy beállításkulccsal kezelhetik ezt az űrlapot. 

![A Power BI Desktop első indításakor megjelenő bejelentkezési űrlap](media/desktop-admin-sign-in-form/sign-in-form.png)

A rendszergazdák az alábbi beállításkulccsal tilthatják le a bejelentkezési űrlapot. Ezt globális házirendek segítségével ki is lehet terjeszteni az egész szervezetre.

```
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Power BI Desktop
valueName: ShowLeadGenDialog
```

A 0 érték kikapcsolja a párbeszédpanelt.

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

