---
title: "Kapcsolódás a Smartsheethez a Power BI-jal"
description: Smartsheet Power BI-hoz
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
ms.openlocfilehash: 6e212f1a3cf114ebdd4eeba59aee20cfa4e02182
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-smartsheet-with-power-bi"></a>Kapcsolódás a Smartsheethez a Power BI-jal
A Smartsheet könnyen használható platformot kínál az együttműködéshez és fájlmegosztáshoz. A Power BI-hoz készült Smartsheet-tartalomcsomag a Smartsheet-fiók áttekintését megjelenítő irányítópultot, jelentéseket és adatkészletet biztosít. A fiók egyes lapjaihoz közvetlenül is kapcsolódhat a [Power BI Desktop](desktop-connect-to-data.md) használatával. 

Kapcsolódjon a Power BI-hoz készült [Smartsheet-tartalomcsomaghoz](https://app.powerbi.com/groups/me/getdata/services/smartsheet).

>[!NOTE]
>A Power BI-tartalomcsomag betöltéséhez rendszergazdai fiók szükséges a Smartsheet szolgáltatásban, mivel ennek további hozzáférési engedélyei vannak.

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
   ![](media/service-connect-to-smartsheet/pbi_getdata.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** gombra.
   
   ![](media/service-connect-to-smartsheet/pbi_getservices.png) 
3. Kattintson a **Smartsheet \> Beolvasás** gombra.
   
   ![](media/service-connect-to-smartsheet/smartsheet.png)
4. A Hitelesítési módszer beállításnál válassza az **oAuth2 \> Bejelentkezés** lehetőséget.
   
   Amikor a rendszer kéri, adja meg saját Smartsheet-beli hitelesítő adatait, majd haladjon végig a hitelesítési folyamaton.
   
   ![](media/service-connect-to-smartsheet/creds.png)
   
   ![](media/service-connect-to-smartsheet/creds2.png)
5. Miután a Power BI importálta az adatokat, megjelenik egy új irányítópult, egy jelentés és egy adathalmaz a bal oldali navigációs ablaktáblán. Az új elemeket egy sárga csillag \* jelöli, válassza ki a Smartsheet bejegyzést.
   
   ![](media/service-connect-to-smartsheet/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található.
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson az egyik csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="whats-included"></a>A csomag tartalma
A Power BI-hoz készült Smartsheet-tartalomcsomag tartalmazza a Smartsheet-fiók áttekintését, például a munkateretek, jelentések és lapok számát, ezek módosításának időpontját stb. A rendszergazdák számára a rendszer felhasználóira vonatkozó információk is megjelennek, például a legtöbb lapot létrehozó felhasználók.  

Egyéni lapokhoz való közvetlen kapcsolódáshoz a fiókban használhatja a Smartsheet-összekötőt a [Power BI Desktop](desktop-connect-to-data.md) alkalmazásban.  

## <a name="next-steps"></a>Következő lépések:

[Első lépések a Power BI-ban](service-get-started.md)

[Adatbeolvasás a Power BI-ban](service-get-data.md)