---
title: "Kapcsolódás az IntelliBoardhoz a Power BI-jal"
description: IntelliBoard a Power BI-ban
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
ms.openlocfilehash: f668a1c9bfefb1b0b0c7c15f9d68c82312d38105
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-intelliboard-with-power-bi"></a>Kapcsolódás az IntelliBoardhoz a Power BI-jal
Az IntelliBoard jelentéskészítő szolgáltatások használatával biztosít egyszerűbb hozzáférést a Moodle tanuláskezelő rendszer adataihoz. A Power BI-hoz készült IntelliBoard-tartalomcsomag további elemzési lehetőségeket tartalmaz, köztük a tanfolyamok, a regisztrált felhasználók, az általános teljesítmény és az LMS-tevékenység metrikáit.

Kapcsolódjon a Power BI-hoz készült [IntelliBoard-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/intelliboard).

## <a name="how-to-connect"></a>A kapcsolódás menete
1. Kattintson az **Adatok beolvasása** elemre a bal oldalon lévő navigációs panel alján.  
   
    ![](media/service-connect-to-intelliboard/getdata.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** gombra.  
   
    ![](media/service-connect-to-intelliboard/services.png)
3. Válassza az **IntelliBoard**, majd a **Beolvasás** lehetőséget.  
   
    ![](media/service-connect-to-intelliboard/intelliboard.png)
4. Válassza ki az **OAuth 2**, majd a **Bejelentkezés** lehetőséget. Amikor a rendszer kéri, adja meg az IntelliBoard-fiókja hitelesítő adatait.
   
    ![](media/service-connect-to-intelliboard/creds.png)
   
    ![](media/service-connect-to-intelliboard/creds2.png)
5. A kapcsolódás után automatikusan betöltődik egy irányítópult, egy jelentés és egy adatkészlet. A befejezést követően a csempék frissülni fognak az Ön IntelliBoard-fiókjából származó adatokkal.
   
    ![](media/service-connect-to-intelliboard/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található.
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Válasszon ki egy csempét](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="whats-included"></a>A csomag tartalma
A tartalomcsomag a következő táblák adatait tartalmazza:  

    - Activity (Tevékenység)  
    - Agents (Ügynökök)  
    - Auth (Hitelesítés)  
    - Countries (Országok)  
    - CoursesProgress (Tanfolyamok haladása)  
    - Enrollments (Regisztrációk)
    - Lang (Nyelv)  
    - Platform  
    - Totals (Eredmények)  
    - UsersProgress (Felhasználók haladása)    

## <a name="system-requirements"></a>Rendszerkövetelmények
A tartalomcsomag példányának létrehozásához egy olyan IntelliBoard-fiók szükséges, amely rendelkezik engedélyekkel a fenti táblázatokhoz.

## <a name="next-steps"></a>További lépések
[Power BI ‒ Első lépések](service-get-started.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

