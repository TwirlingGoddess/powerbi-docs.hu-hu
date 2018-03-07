---
title: "Csatlakozás a Project Online-hoz a Power BI használatával"
description: Project Online a Power BI-hoz
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
ms.openlocfilehash: 6272b3f175d7da851e5d8086c574a91f0f00c933
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="connect-to-project-online-with-power-bi"></a>Csatlakozás a Project Online-hoz a Power BI használatával
A Microsoft Project Online a projektportfólió-kezeléshez (PPM) és a mindennapi munkához nyújt rugalmas online megoldást. A Project Online lehetővé teszi a cég számára, hogy megtegye az előkészületeket, rangsorolja a projektporfólió-befektetéseket, és elérje a tervezett üzleti eredményt. A Power BI-hoz készült Project Online-tartalomcsomag segítségével olyan előregyártott mérőszámokkal elemezheti a projektadatokat, mint a portfólióállapot és a projektmegfelelőség.

Kapcsolódjon a Power BI-hoz készült [Project Online-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/project-online).

## <a name="how-to-connect"></a>A csatlakozás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.
   
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

**Mi a következő lépés?**

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja a frissítési ütemezést, vagy igény szerint bármikor frissíthet az **Azonnali frissítés** elemre kattintva

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok lekérése a Power BI-ban](service-get-data.md)

