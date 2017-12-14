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
ms.openlocfilehash: b4f4a999ed9929366f58f719030490fc56f5364d
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-sendgrid-with-power-bi"></a>Csatlakozás a SendGridhez a Power BI segítségével
A Power BI SendGridhez készült tartalomcsomagja elemzések és statisztikák kinyerését teszi lehetővé a SendGrid-fiókjából. A SendGrid-tartalomcsomag használatával vizualizálni tudja SendGrid-statisztikáit egy irányítópulton.

Kapcsolódjon a Power BI-hoz készült [SendGrid-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/sendgrid).

## <a name="how-to-connect"></a>A kapcsolódás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs panel alján.
   
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

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található.
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Válasszon ki egy csempét](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet naponta frissül, de módosíthatja a frissítési ütemezést, és bármikor frissíthet igény szerint is az **Azonnali frissítés** lehetőséggel.

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

