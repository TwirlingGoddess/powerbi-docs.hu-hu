---
title: "Csatlakozás a Project Online-hoz a Power BI használatával"
description: Project Online a Power BI-hoz
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
ms.openlocfilehash: 509b75d91611de827b236e45dc25ef893aff8177
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-project-online-with-power-bi"></a>Csatlakozás a Project Online-hoz a Power BI használatával
A Microsoft Project Online a projektportfólió-kezeléshez (PPM) és a mindennapi munkához nyújt rugalmas online megoldást. A Project Online lehetővé teszi a cég számára, hogy megtegye az előkészületeket, rangsorolja a projektporfólió-befektetéseket, és elérje a tervezett üzleti eredményt. A Power BI-hoz készült Project Online-tartalomcsomag segítségével olyan előregyártott mérőszámokkal elemezheti a projektadatokat, mint a portfólióállapot és a projektmegfelelőség.

Kapcsolódjon a Power BI-hoz készült [Project Online-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/project-online).

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
    ![](media/service-connect-to-project-online/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-project-online/services.png)
3. Válassza a **Microsoft Project Online** \> **Get** lehetőséget.
   
   ![](media/service-connect-to-project-online/mproject.png)
4. A **Project Web App URL** (Projekt Web App URL-címe) szövegdobozba írja be a csatlakoztatni kívánt Project Web App URL-címét, majd kattintson a **Következő** elemre. Vegye figyelembe, hogy ez az adat egyedi tartomány esetén eltérhet a példától.
   
    ![](media/service-connect-to-project-online/params.png)
5. A Hitelesítési módszer beállításánál válassza az **oAuth2** \> **Sign In** lehetőséget. Amikor a rendszer kéri, adja meg a saját Projekt Online hitelesítő adatait, majd haladjon végig a hitelesítési folyamaton.
   
    ![](media/service-connect-to-project-online/creds.png)
6. Egy értesítés jelzi, hogy az adatok betöltése folyamatban van. A fiók méretétől függően ez eltarthat egy ideig. Miután a Power BI importálta az adatokat, a bal oldali navigációs ablaktáblán egy új irányítópult, jelentés és adatkészlet jelenik meg. A Power BI ezt az alapértelmezett irányítópultot hozta létre az adatok megjelenítésére. Az irányítópultot módosíthatja, hogy az igényei szerint jelenítse meg az adatokat.
   
   ![](media/service-connect-to-project-online/dashboard2.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

