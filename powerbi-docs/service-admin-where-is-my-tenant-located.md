---
title: Hol található a Power BI-bérlőm?
description: Tudja meg, hogy hol található a Power BI-bérlője, és hogy miként történt ennek a helynek a kiválasztása. Ennek a megértése fontos, mert hatással lehet a szolgáltatással kapcsolatos interakciókra.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 08/10/2017
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: c0c6de63292d3087aaa78dd97b73f868ef9d804e
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34293651"
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

