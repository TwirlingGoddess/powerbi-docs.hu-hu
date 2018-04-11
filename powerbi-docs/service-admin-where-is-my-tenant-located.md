---
title: Hol található a Power BI-bérlőm?
description: Tudja meg, hogy hol található a Power BI-bérlője, és hogy miként történt ennek a helynek a kiválasztása. Ennek a megértése fontos, mert hatással lehet a szolgáltatással kapcsolatos interakciókra.
services: powerbi
documentationcenter: ''
author: mgblythe
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/10/2017
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: 22b5319cf95beb3ea4a4a498c7174a701e56fb95
ms.sourcegitcommit: 8552a34df8e6141eb704314c1a019992901d6e78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/08/2018
---
# <a name="where-is-my-power-bi-tenant-located"></a>Hol található a Power BI-bérlőm?
<iframe width="560" height="315" src="https://www.youtube.com/embed/0fOxaHJPvdM?showinfo=0" frameborder="0" allowfullscreen></iframe>

Tudja meg, hogy hol található a Power BI-bérlője, és hogy miként történt ennek a helynek a kiválasztása. Ennek a megértése fontos, mert hatással lehet a szolgáltatással kapcsolatos interakciókra.

## <a name="how-to-determine-where-your-power-bi-tenant-is-located"></a>A Power BI-bérlő helyének meghatározása
A bérlő régiójának megkereséséhez tegye az alábbiakat.

1. Kattintson a **?** kérdőjelre a Power BI szolgáltatásban.
2. Kattintson **A Power BI bemutatása** elemre.
3. Nézze meg **Az adatok a következő helyeken vannak tárolva** melletti szöveget. Ebben a régióban található a bérlő.

![](media/service-admin-where-is-my-tenant-located/power-bi-data-region.png)

## <a name="how-the-data-region-is-selected"></a>Az adatrégió kiválasztásának módja
Az adatrégió a bérlő első létrehozásakor kiválasztott országon alapul. Ez a Power BI mellett az Office 365-re való regisztrációra is vonatkozik, mivel ez egy megosztott információ. Ha ez egy új bérlő, regisztrációkor meg fog jelenni az országok legördülő menüje.

![](media/service-admin-where-is-my-tenant-located/sign-up-country-selection.png)

Ettől a választástól függ, hogy hol lesznek az adatai tárolva. A Power BI a kiválasztott országhoz legközelebbi adatrégiót fogja választani.

> [!WARNING]
> Ez a választás nem módosítható!
> 
> 

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

