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
ms.openlocfilehash: 92b069bded7fc6a22480d8190c1b8d0f53f959e4
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/19/2018
---
# <a name="connect-to-mandrill-with-power-bi"></a>Kapcsolódás a Mandrillhoz a Power BI használatával
A Power BI-tartalomcsomag lekéri a Mandrill-fiókban található adatokat, és létrehoz egy irányítópultot, több jelentést, valamint egy adathalmazt, amelyek segítségével elemezheti és megismerheti az adatokat. A Mandrill elemzései segítségével gyors betekintést nyerhet hírlevél- vagy marketingkampányába. Az alapértelmezett beállítások szerint az adatok naponta frissülnek, hogy Ön mindig naprakész adatokat ellenőrizhessen.

Kapcsolódás a [Power BI Mandrill-tartalomcsomagjához](http://app.powerbi.com/getdata/services/mandrill)

## <a name="how-to-connect"></a>A kapcsolódás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.
   
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

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja a frissítési ütemezést, vagy igény szerint bármikor frissíthet az **Azonnali frissítés** elemre kattintva

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

