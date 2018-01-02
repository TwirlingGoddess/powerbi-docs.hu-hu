---
title: "Kapcsolódás az Azure Mobile Engagement szolgáltatáshoz a Power BI használatával"
description: "A Power BI-hoz készült Azure Mobile Engagement"
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: 85b43579785983da2ddc3ac2e302396d1a282792
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-azure-mobile-engagement-with-power-bi"></a>Kapcsolódás az Azure Mobile Engagement szolgáltatáshoz a Power BI használatával
A Power BI Azure Mobile Engagement tartalomcsomaggal gyors betekintést nyerhet az alkalmazása adataiba.

Kapcsolódjon a Power BI-hoz készült [Azure Mobile Engagement-tartalomcsomaghoz](https://app.powerbi.com/groups/me/getdata/services/azme).

## <a name="how-to-connect"></a>A kapcsolódás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
    ![](media/service-connect-to-azure-mobile/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
    ![](media/service-connect-to-azure-mobile/services.png)
3. Válassza ki az **Azure Mobile Engagement** \> **Beolvasás** elemet.
   
    ![](media/service-connect-to-azure-mobile/azme.png) 
4. Adja meg az alkalmazásgyűjteményt és az alkalmazásnevet. Ez az információ az Azure Mobile Engagement-fiókban található.
   
    ![](media/service-connect-to-azure-mobile/parameters.png) 
5. Hitelesítési módszernek adja meg a kulcsot, majd kattintson a Bejelentkezés gombra.
   
    ![](media/service-connect-to-azure-mobile/creds.png)
6. Miután a Power BI importálta az adatokat, a bal oldali navigációs ablaktáblán egy új irányítópult, jelentés és adatkészlet jelenik meg. A rendszer az új elemeket sárga csillaggal \* jelöli meg, amely kijelölés után eltűnik:
   
    ![](media/service-connect-to-azure-mobile/dashboard.png)

 **Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Válasszon ki egy csempét](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja a frissítési ütemezést, vagy igény szerint bármikor frissíthet az **Azonnali frissítés** elemre kattintva

## <a name="next-steps"></a>További lépések
[Power BI – első lépések](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

