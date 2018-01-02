---
title: "Kapcsolódás a Prevedere eszközhöz a Power BI-ban"
description: Prevedere a Power BI-ban
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
ms.openlocfilehash: 44871137e63572d801525c1f070dac5d07a32308
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-prevedere-with-power-bi"></a>Kapcsolódás a Prevedere eszközhöz a Power BI-ban
Exkluzív és kritikus fontosságú pénzügyi információkhoz juthat, amelyekkel magabiztosan és kezdeményezően fejlesztheti üzletét.

Csatlakozzon a Power BI-hoz készült [Prevedere tartalomcsomaghoz](https://app.powerbi.com/getdata/services/prevedere).

>[!NOTE]
>Ha Ön nem Prevedere-felhasználó, a kipróbáláshoz használja a [mintakulcsot](https://prevederepowerbiconnector.azurewebsites.net/static/learnmore.html).

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktáblán.
   
   ![](media/service-connect-to-prevedere/getdata.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** elemre.
   
   ![](media/service-connect-to-prevedere/services.png)
3. Kattintson a **Prevedere**, majd a **Beolvasás** elemre.
   
   ![](media/service-connect-to-prevedere/connect.png)
4. A **Hitelesítési módszer** beállításban kattintson a **Kulcs** lehetőségre, majd adja meg a Prevedere API-kulcsát.
   
    ![](media/service-connect-to-prevedere/creds.png)
5. A **Bejelentkezés** elemre kattintva kezdje el az importálási folyamatot. Amikor a folyamat befejeződik, a navigációs ablaktáblán új irányítópult, jelentés és modell jelenik meg. Az importált adatok megtekintéséhez kattintson az irányítópultra.
   
     ![](media/service-connect-to-prevedere/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson az egyik csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor az **Azonnali frissítés** lehetőségre kattintva.

## <a name="whats-included"></a>Tartalom
A tartalomcsomag elemzési adatokat nyújt többek között a kiskereskedelmi előrejelzésekről, az előrejelzési modellekről, és a fő mutatókról.

## <a name="system-requirements"></a>Rendszerkövetelmények
A tartalomcsomag megköveteli a hozzáférést egy Prevedere API-kulcshoz vagy a mintakulcshoz (lásd alább).

## <a name="finding-parameters"></a>Paraméterek keresése
<a name="FindingParams"></a>

A meglévő ügyfelek a saját API-kulcs segítségével férhetnek hozzá az adataikhoz. Ha Ön még nem ügyfél, a [mintakulcs](https://prevederepowerbiconnector.azurewebsites.net/static/learnmore.html) használatával tekintheti meg az adat- és az elemzési mintákat.

## <a name="troubleshooting"></a>Hibaelhárítás
Az adatok betöltése a példány méretétől függően időbe telhet.

## <a name="next-steps"></a>Következő lépések
[Power BI – első lépések](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

