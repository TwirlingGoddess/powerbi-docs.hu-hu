---
title: "Csatlakozás a QuickBooks Online-hoz a Power BI használatával"
description: QuickBooks Online a Power BI-hoz
services: powerbi
documentationcenter: 
author: SarinaJoan
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
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 770daa9965f44d655fb60b8b723f83e260daccb6
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="connect-to-quickbooks-online-with-power-bi"></a>Csatlakozás a QuickBooks Online-hoz a Power BI használatával
Amikor Power BI-ból csatlakozik a QuickBooks Online-adatokhoz, azonnal megjelenik egy Power BI-irányítópult és néhány Power BI-jelentés, amelyek alapján pénzforgalmával, jövedelmezőségével, ügyfeleivel és sok más területtel kapcsolatban összefüggéseket tárhat fel. Az irányítópultot és a jelentéseket a megjelenített formában is használhatja, illetve igényei szerint át is alakíthatja azokat, hogy azokat az információkat emeljék ki, melyek az Ön számára a legfontosabbak. Az adatokat naponta egyszer automatikusan frissíti a rendszer.

Kapcsolódjon a Power BI-hoz készült [QuickBooks Online-tartalomcsomaghoz](https://dxt.powerbi.com/getdata/services/quickbooks-online).

>[!NOTE]
>A QuickBooks Online adatok Power BI-ba történő importálásához, QuickBooks Online-fiókjában rendszergazdának kell lennie, és rendszergazdai hitelesítő adataival kell bejelentkeznie.

## <a name="how-to-connect"></a>A csatlakozás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.
   
   ![](media/service-connect-to-quickbooks-online/pbi_getdata.png) 
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** lehetőségre.
   
   ![](media/service-connect-to-quickbooks-online/pbi_getservices.png) 
3. Válassza ki **QuickBooks Online**, majd kattintson a **Letöltés most** lehetőségre.
   
   ![](media/service-connect-to-quickbooks-online/qbo.png)
4. Hitelesítési módszerként válassza az **oAuth2** eljárást, majd kattintson a **Bejelentkezés** lehetőségre. 
5. Amikor a rendszer kéri, adja meg QuickBooks Online hitelesítő adatait, majd haladjon végig a hitelesítési folyamaton. Ha böngészőjében már bejelentkezett a QuickBooks Online-ba, a rendszer nem feltétlenül fogja kérni hitelesítő adatait.
   >[!NOTE]
   >A QuickBooks Online-fiókjába rendszergazdai hitelesítő adatokkal kell bejelentkeznie.
6. A következő képernyőn válassza ki azt a céget, amelyet csatlakoztatni szeretne a Power BI-hoz.
   
   ![](media/service-connect-to-quickbooks-online/pbi_qbo_almost.png)
7. Az importálási folyamat elindításához a következő képernyőn kattintson az **Authorize** (Engedélyezés) elemre. Ez a vállalati adatok méretétől függően néhány percet is igénybe vehet. 
   
   ![](media/service-connect-to-quickbooks-online/pbi_qbo_authorizesm.png)
   
   Miután a Power BI importálta az adatokat, a bal oldali navigációs ablaktáblán megjelenik egy új irányítópult, egy új jelentés és egy új adatkészlet. Az új elemeket sárga csillag \* jelöli.
   
   ![](media/service-connect-to-quickbooks-online/pbi_qbo_leftnavnew.png)
8. Válassza ki a QuickBooks Online irányítópultot. Ez a Power BI által automatikusan létrehozott irányítópult az importált adatok megjelenítéséhez. Az irányítópultot módosíthatja, hogy az igényei szerint jelenítse meg az adatokat. 
   
   ![](media/service-connect-to-quickbooks-online/pbi_qbo_dash.png)

**Hogyan tovább?**

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="troubleshooting"></a>Hibaelhárítás
**„Hoppá! Hiba történt.”**

Ha az **Authorize** (Engedélyezés) választása után ezt az üzenetet kapja:

„Hoppá! Hiba történt.” Zárja be ezt az ablakot, és próbálkozzon újra.

Az alkalmazásra már feliratkozott a cég egy másik felhasználója. Az előfizetés módosításához írjon a [rendszergazda e-mail-címe] címre.”

![](media/service-connect-to-quickbooks-online/pbi_qbo_oopssm.png)

... Ez azt jelenti, hogy a cég egy másik rendszergazdája már csatlakozott a vállalati adatokhoz a Power BI-jal. Kérje meg azt a rendszergazdát, hogy ossza meg Önnel az irányítópultot. Jelenleg csak egy rendszergazdai jogú felhasználó csatlakoztathat egy adott QuickBooks Online céges adatkészletet a Power BI-hoz. Ha a Power BI létrehozta az irányítópultot, a rendszergazda megoszthatja az ugyanazon a Power BI bérlőn található munkatársakkal.

**„Az alkalmazásban nincs beállítva az Ön országából induló kapcsolatok engedélyezése"**

A Power BI jelenleg csak a QuickBooks Online egyesült államokbeli kiadásait támogatja. 

![](media/service-connect-to-quickbooks-online/pbi_qbo_countrynotsupported.png)

## <a name="next-steps"></a>Következő lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

