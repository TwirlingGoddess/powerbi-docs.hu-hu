---
title: "Csatlakozás a SendGridhez a Power BI segítségével"
description: A Power BI SendGrid
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
ms.openlocfilehash: d077bedcc1faa10af79cf3eba258b1dac969ae10
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/19/2018
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

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok lekérése](service-get-data.md)

