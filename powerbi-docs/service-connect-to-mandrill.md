---
title: Kapcsolódás a Mandrillhoz a Power BI használatával
description: Mandrill a Power BI-hoz
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 150277c4069be8c292e02caa495e8c545138227e
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/21/2018
ms.locfileid: "46546050"
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

* [Kérdéseket tehet fel a Q&A mezőben](consumer/end-user-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](consumer/end-user-tiles.md) a mögöttes jelentés megnyitásához.
* Noha az adatkészlet napi frissítésre van ütemezve, módosíthatja a frissítési ütemezést, vagy igény szerint frissíthet az **Azonnali frissítés** gombbal.

## <a name="next-steps"></a>Következő lépések
[Mi az a Power BI?](power-bi-overview.md)

[Power BI – Alapfogalmak](consumer/end-user-basic-concepts.md)

