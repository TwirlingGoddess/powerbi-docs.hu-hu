---
title: "Kapcsolódás a Ziosk Survey Analytics szolgáltatáshoz a Power BI-t használva"
description: "A Power BI-hoz készült Ziosk"
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
ms.openlocfilehash: 0f4cd7166334338e4b19586c189fd363c5b7c934
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-ziosk-survey-analytics-with-power-bi"></a>Kapcsolódás a Ziosk Survey Analytics szolgáltatáshoz a Power BI-t használva
A Power BI-hoz készített Ziosk Survey Analytics tartalomcsomag Ziosk táblagépekkel használva egyedülálló módon tárja az éttermek elé a Ziosk felmérések adataiból felismerhető összefüggéseket, többek között nap, hely és alkalmazott szerint is szegmentálva.

Kapcsolódjon a Power BI-hoz készített [Ziosk Survey Analytics tartalomcsomaghoz](https://app.powerbi.com/getdata/services/ziosk-survey-analytics).

## <a name="how-to-connect"></a>A kapcsolódás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs panel alján.  
   
    ![](media/service-connect-to-ziosk/getdata.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** gombra.  
   
    ![](media/service-connect-to-ziosk/services.png)
3. Kattintson a **Ziosk Survey Analytics**, majd a **Beolvasás** lehetőségre.  
   
    ![](media/service-connect-to-ziosk/ziosk.png)
4. Válassza ki az **OAuth 2**, majd a **Bejelentkezés** lehetőséget. Amikor a rendszer kéri, adja meg az Ziosk-fiókja hitelesítő adatait.
   
    ![](media/service-connect-to-ziosk/creds.png)
   
    ![](media/service-connect-to-ziosk/creds2.png)
5. A kapcsolódás után automatikusan betöltődik egy irányítópult, egy jelentés és egy adatkészlet. A befejezést követően a csempék frissülni fognak az Ön Ziosk-fiókjából származó adatokkal.
   
    ![](media/service-connect-to-ziosk/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A-mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson az egyik csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adathalmaz naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, a **Frissítés** lehetőségre kattintva

## <a name="whats-included"></a>A csomag tartalma
A tartalomcsomag a következő táblák adatait tartalmazza:  

    - Alkohol kategória  
    - Előétel kategória  
    - CommentKeywords  
    - Dátum  
    - Napszak  
    - Desszert kategória  
    - Freeform  
    - Gyerek kategória  
    - Üzenetek  
    - Prémium tartalom kategória  
    - Kérdés  
    - Áruház  
    - Felmérések  
    - Hétköznap  


## <a name="system-requirements"></a>Rendszerkövetelmények
A tartalomcsomag példányának létrehozásához egy olyan Ziosk-fiók szükséges, amely rendelkezik engedélyekkel a fenti táblázatokhoz.

## <a name="next-steps"></a>További lépések
[Power BI ‒ első lépések](service-get-started.md)

[Power BI – alapfogalmak](service-basic-concepts.md)

