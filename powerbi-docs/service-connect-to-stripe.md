---
title: Csatlakozás a Stripe-hoz a Power BI segítségével
description: Power BI Stripe
services: powerbi
documentationcenter: ''
author: SarinaJoan
manager: kfile
backup: maggiesMSFT
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 8d5c99f901471d61ec8483e1f8c898071ce8c25c
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="connect-to-stripe-with-power-bi"></a>Csatlakozás a Stripe-hoz a Power BI segítségével
A Power BI-tartalomcsomag segítségével megtekintheti és elemezheti Stripe-adatait. A Power BI Stripe-tartalomcsomag adatokat nyer ki ügyfelekről, díjakról, eseményekről és számlákról. Az adatok a legutóbbi tízezer eseményre és ötezer díjtételre vonatkoznak az utolsó 30 napra kiterjedően. A tartalom naponta egyszer automatikusan frissül az Ön által beállított ütemezés szerint. 

Kapcsolódás a [Power BI Stripe-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/stripe).

## <a name="how-to-connect"></a>A kapcsolódás menete
1. Válassza az Adatok lekérése elemet a bal oldalon lévő navigációs ablaktábla alján.  
   
    ![](media/service-connect-to-stripe/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.  
   
    ![](media/service-connect-to-stripe/services.png)  
3. Válassza a **Stripe** &gt; **Letöltés most** elemet.  
   
    ![](media/service-connect-to-stripe/stripe.png)  
4. A kapcsolódáshoz adja meg a Stripe-[API-kulcsát](https://dashboard.stripe.com/account/apikeys).  
   
    ![](media/service-connect-to-stripe/creds.png)
5. Az importálás automatikusan megkezdődik. Amikor befejeződik, a navigációs ablaktáblán megjelenik az új irányítópult, jelentés és modell, egy csillaggal jelölve. Az importált adatok megtekintéséhez kattintson az irányítópultra.
   
    ![](media/service-connect-to-stripe/dashboard.png)

**Mi a következő lépés?**

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja a frissítési ütemezést, vagy igény szerint bármikor frissíthet az **Azonnali frissítés** elemre kattintva

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Power BI – Adatok lekérése](service-get-data.md)

