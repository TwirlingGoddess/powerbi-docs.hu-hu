---
title: Kapcsolódás a Prevedere eszközhöz a Power BI-ban
description: Prevedere a Power BI-ban
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: e030d80a26b946d6b99c808c937dca4bb6eb3a62
ms.sourcegitcommit: 0ff358f1ff87e88daf837443ecd1398ca949d2b6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/21/2018
ms.locfileid: "46543487"
---
# <a name="connect-to-prevedere-with-power-bi"></a>Kapcsolódás a Prevedere eszközhöz a Power BI-ban
Exkluzív és kritikus fontosságú pénzügyi információkhoz juthat, amelyekkel magabiztosan és kezdeményezően fejlesztheti üzletét.

Csatlakozzon a Power BI-hoz készült [Prevedere tartalomcsomaghoz](https://app.powerbi.com/getdata/services/prevedere).

>[!NOTE]
>Ha Ön nem Prevedere-felhasználó, a kipróbáláshoz használja a [mintakulcsot](https://prevederepowerbiconnector.azurewebsites.net/static/learnmore.html).

## <a name="how-to-connect"></a>A csatlakozás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.
   
   ![](media/service-connect-to-prevedere/getdata.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** elemre.
   
   ![](media/service-connect-to-prevedere/services.png)
3. Kattintson a **Prevedere**, majd a **Beolvasás** elemre.
   
   ![](media/service-connect-to-prevedere/connect.png)
4. A **Hitelesítési módszer** beállításban kattintson a **Kulcs** lehetőségre, majd adja meg a Prevedere API-kulcsát.
   
    ![](media/service-connect-to-prevedere/creds.png)
5. A **Bejelentkezés** elemre kattintva kezdje el az importálási folyamatot. Amikor a folyamat befejeződik, a navigációs ablaktáblán új irányítópult, jelentés és modell jelenik meg. Válassza ki az irányítópultot az importált adatok megtekintéséhez.
   
     ![](media/service-connect-to-prevedere/dashboard.png)

**Mi a következő lépés?**

* [Kérdéseket tehet fel a Q&A mezőben](consumer/end-user-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](consumer/end-user-tiles.md) a mögöttes jelentés megnyitásához.
* Noha az adatkészlet napi frissítésre van ütemezve, módosíthatja a frissítési ütemezést, vagy igény szerint frissíthet az **Azonnali frissítés** gombbal.

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
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok lekérése a Power BI-ban](service-get-data.md)

