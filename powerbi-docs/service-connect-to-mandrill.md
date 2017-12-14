---
title: "Kapcsolódás a Mandrillhoz a Power BI használatával"
description: Mandrill a Power BI-hoz
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
ms.openlocfilehash: 976ca32f0c43f6d8412f9468dc9f61ab9768fa4c
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-mandrill-with-power-bi"></a>Kapcsolódás a Mandrillhoz a Power BI használatával
A Power BI-tartalomcsomag lekéri a Mandrill-fiókban található adatokat, és létrehoz egy irányítópultot, több jelentést, valamint egy adathalmazt, amelyek segítségével elemezheti és megismerheti az adatokat. A Mandrill elemzései segítségével gyors betekintést nyerhet hírlevél- vagy marketingkampányába. Az alapértelmezett beállítások szerint az adatok naponta frissülnek, hogy Ön mindig naprakész adatokat ellenőrizhessen.

Kapcsolódás a [Power BI Mandrill-tartalomcsomagjához](http://app.powerbi.com/getdata/services/mandrill)

## <a name="how-to-connect"></a>A kapcsolódás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs panel alján.
   
    ![](media/service-connect-to-mandrill/getdata.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** elemre.
   
    ![](media/service-connect-to-mandrill/services.png)
3. Válassza a **Mandrill** > **Beolvasás** elemet.
   
    ![](media/service-connect-to-mandrill/mandrill.png)
4. A **Hitelesítési módszer**, beállításban válassza a **Kulcs** lehetőséget, és adja meg az API-kulcsot. A kulcs a Mandrill irányítópult **Beállítások** lapján található. Indítsa el az importálási folyamatot a **Bejelentkezés** elemre kattintva. A művelet a fiókban tárolt adatok mennyiségétől függően több percig is eltarthat.
   
    ![](media/service-connect-to-mandrill/auth.png)
5. Miután a Power BI importálta az adatokat, megjelenik egy új irányítópult, egy jelentés és egy adathalmaz a bal oldali navigációs ablaktáblán. Ez az az alapértelmezett irányítópult, amelyet a Power BI létrehozott az adatok megjelenítésére.
   
    ![](media/service-connect-to-mandrill/mandrill-dashboard1.jpg)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adathalmaz naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, a **Frissítés** lehetőségre kattintva

## <a name="next-steps"></a>Következő lépések
[Első lépések a Power BI használatával](service-get-started.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

