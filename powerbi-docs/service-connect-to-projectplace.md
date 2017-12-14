---
title: "Csatlakozás a Projectplace-hez a Power BI használatával"
description: Projectplace a Power BI-hoz
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
ms.openlocfilehash: 3327c193828dcdc28c2dd5b93c56615fdb367c70
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-projectplace-by-planview-with-power-bi"></a>Csatlakozás a Planview Projectplace tartalomcsomagjához a Power BI használatával
A Planview Projectplace tartalomcsomagjának segítségével egészen újszerű módon, közvetlenül a Power BI-ban jelenítheti meg az együttműködésen alapuló projektadatokat. A Projectplace-hez használt bejelentkezési hitelesítő adataival interaktívan tekintheti meg a Projectplace-fiók összes projektjének kulcsfontosságú statisztikáit, láthatja a csoport legaktívabb és leghatékonyabb tagjait, és azonosíthatja a kockázatos besorolású kártyákat valamint tevékenységeket. Az Ön számára legfontosabb elemzések megjelenítéséhez kibővítheti az előregyártott irányítópultot és a jelentéseket.

[Csatlakozás a Projectplace tartalomcsomaghoz a Power BI-ban](https://app.powerbi.com/getdata/services/projectplace)

>[!NOTE]
>Ahhoz, hogy a Power BI-ba importálhassa Projectplace-adatait, Projectplace-felhasználónak kell lennie. A további követelményeket alább tekintheti meg.

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs panel alján.
   
    ![](media/service-connect-to-projectplace/get.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** elemre.
   
    ![](media/service-connect-to-projectplace/services.png)
3. A Power BI oldalon jelölje ki a **Projectplace by Planview** lehetőséget, majd kattintson a **Beolvasás** elemre:  
   
    ![](media/service-connect-to-projectplace/projectplace.png)
4. Az OData-adatcsatorna URL-címe szövegmezőbe írja be a használni kívánt Projectplace OData-adatcsatorna URL-címét az alábbi ábra szerint:
   
    ![](media/service-connect-to-projectplace/params.png)
5. A Hitelesítési módszer listán kattintson az **OAuth** elemre, ha még nincs kijelölve. Kattintson a **Bejelentkezés** gombra, és haladjon végig a bejelentkezés folyamatán.  
   
   ![](media/service-connect-to-projectplace/creds.png)
6. A bal oldali ablaktáblán, az irányítópultok listáján válassza ki a **Projectplace** lehetőséget. A Power BI az irányítópultba importálja a Projectplace adatait. Vegye figyelembe, hogy az adatok betöltése időbe telhet.  
   
    Az irányítópult csempéi megjelenítik a Projectplace adatbázisából származó adatokat. Az alábbi mintán egy Power BI-beli alapértelmezett Projectplace-irányítópult látható.
   
    ![](media/service-connect-to-projectplace/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="system-requirements"></a>Rendszerkövetelmények
Ahhoz, hogy a Power BI-ba importálhassa Projectplace-adatait, Projectplace-felhasználónak kell lennie. Ez az eljárás feltételezi, hogy előzőleg már bejelentkezett a Microsoft Power BI kezdőlapjára egy Power BI-fiókkal. Ha még nincs Power BI-fiókja, hozzon létre egy új, ingyenes Power BI-fiókot a Power BI kezdőlapon, majd kattintson az Adatok lekérdezése elemre.

## <a name="next-steps"></a>Következő lépések
[Első lépések a Power BI használatával](service-get-started.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

