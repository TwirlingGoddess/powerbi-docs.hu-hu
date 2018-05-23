---
title: A Power BI Desktop bejelentkezési űrlapjának rendszergazdák általi kezelése
description: Tudja meg, hogyan kezelheti a Power BI Desktop első megnyitásakor megjelenő bejelentkezési űrlapot.
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 04/24/2018
ms.author: davidi
ms.openlocfilehash: 98bf9579ae7ee551634eed765138c0e78156464c
ms.sourcegitcommit: 998b79c0dd46d0e5439888b83999945ed1809c94
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
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

