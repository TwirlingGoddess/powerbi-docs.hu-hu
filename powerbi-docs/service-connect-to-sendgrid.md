---
title: Csatlakozás a SendGridhez a Power BI segítségével
description: A Power BI SendGrid
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: a0ae99e2dfad889840cc29ca4fa9f0f29397bf04
ms.sourcegitcommit: e8d924ca25e060f2e1bc753e8e762b88066a0344
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/29/2018
ms.locfileid: "37135375"
---
# <a name="connect-to-sendgrid-with-power-bi"></a>Csatlakozás a SendGridhez a Power BI segítségével
A Power BI SendGridhez készült tartalomcsomagja elemzések és statisztikák kinyerését teszi lehetővé a SendGrid-fiókjából. A SendGrid-tartalomcsomag használatával vizualizálni tudja SendGrid-statisztikáit egy irányítópulton.

Kapcsolódjon a Power BI-hoz készült [SendGrid-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/sendgrid).

## <a name="how-to-connect"></a>A kapcsolódás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.
   
   ![](media/service-connect-to-sendgrid/pbi_getdata.png) 
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-sendgrid/pbi_getservices.png) 
3. Válassza ki a **SendGrid**-tartalomcsomagot, és kattintson a **Letöltés most** elemre.
   
   ![](media/service-connect-to-sendgrid/sendgrid.png) 
4. Amikor a rendszer kéri, adja meg a SendGrid-felhasználónevét és -jelszavát. Válassza a **Bejelentkezés** lehetőséget.
   
   ![](media/service-connect-to-sendgrid/pbi_sendgridsignin.png)
5. Miután a Power BI importálta az adatokat, a navigációs ablaktáblán megjelenik egy új irányítópult, jelentés és adatkészlet, az elmúlt 90 nap levelezési statisztikáival. Az új elemeket sárga csillag \* jelöli.
   
   ![](media/service-connect-to-sendgrid/pbi_sendgriddash.png)

**Hogyan tovább?**

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Noha az adatkészlet napi frissítésre van ütemezve, módosíthatja a frissítési ütemezést, vagy igény szerint frissíthet az **Azonnali frissítés** gombbal.

## <a name="whats-included"></a>A csomag tartalma
A SendGrid-irányítópulton a következő metrikák érhetők el:

* Teljes körű levelezési statisztika: kérelmek, kézbesítések, sikertelen kézbesítések, blokkolt levélszemét, levélszemét-jelentés stb.
* Levelezési statisztika kategória szerint
* Levelezési statisztika földrajzi hely szerint
* Levelezési statisztika internetszolgáltató szerint
* Levelezési statisztika eszköz, ügyfél, böngésző szerint

## <a name="next-steps"></a>Következő lépések
[A Power BI bemutatása](power-bi-overview.md)

[Adatok lekérése](service-get-data.md)

