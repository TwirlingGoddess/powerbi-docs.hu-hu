---
title: "Csatlakozás a comScore Digital Analytix eszközhöz a Power BI használatával"
description: comScore Digital Analytix a Power BI-hoz
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
ms.openlocfilehash: c53c7f5e0748e186c68bcc2642b381cf17c423eb
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-comscore-digital-analytix-with-power-bi"></a>Csatlakozás a comScore Digital Analytix eszközhöz a Power BI használatával
A Power BI-tartalomcsomag segítségével a Power BI-ban jelenítheti meg és elemezheti a comScore Digital Analytix adatait. Az adatok naponta egyszer automatikusan frissülnek.

Csatlakozzon a [Power BI-hoz készült comScore-tartalomcsomaghoz.](https://app.powerbi.com/getdata/services/comscore)

>[!NOTE]
>A tartalomcsomaghoz történő csatlakozáshoz szüksége van egy comScore DAx felhasználói fiókra, valamint hozzáféréssel kell rendelkeznie a comScore API-hoz. A [részleteket](#Requirements) alább találja.

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az Adatok lekérése elemre a bal oldalon lévő navigációs ablaktábla alján.
   
   ![](media/service-connect-to-connect-to/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-connect-to/services.png)
3. Kattintson a **comScore Digital Analytix** \> **Get** elemre.
   
   ![](media/service-connect-to-connect-to/comscore.png)
4. Adja meg az adatközpontot, a comScore ügyfél-azonosítót és azt a webhelyet, amelyhez kapcsolódni szeretne. A felsorolt adatok megtalálásáról lejjebb, a [comScore-paraméterek keresése](#FindingParams) részben tájékozódhat.
   
   ![](media/service-connect-to-connect-to/parameters.png)
5. A csatlakozáshoz adja meg comScore-felhasználónevét és -jelszavát. Az adat megtalálásáról lejjebb tájékozódhat.
   
   ![](media/service-connect-to-connect-to/creds.png)
6. Az importálási folyamat automatikusan elindul. Amikor befejeződik, a navigációs ablaktáblán megjelenik egy új irányítópult, jelentés és modell. Az importált adatok megtekintéséhez kattintson az ablaktáblára.

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

<a name="Requirements"></a>

## <a name="system-requirements"></a>Rendszerkövetelmények
A kapcsolódáshoz comScore DAx felhasználói fiókkal és comScore DAx API-hoz való hozzáféréssel kell rendelkeznie. Kérjük, forduljon a comScore DAx-rendszergazdához a fiók megerősítéséhez.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
Az alábbiakban olvashatók a comScore-paraméterek megkereséséhez szükséges információk.

**Adatközpont**

A csatlakoztatott adatközpontot a comScore-ból elért URL-cím határozza meg.

Ha a https://dax.comscore.com címet használja, az „US”, ha a https://dax.comscore.eu címet használja, az „EU” értéket kell megadnia.

![](media/service-connect-to-connect-to/comscore_url.png) 

**Ügyfél**

Az Ügyfél ugyanaz, mint amit a comScore DAx szolgáltatásba történő bejelentkezéskor ad meg.

![](media/service-connect-to-connect-to/comscore_signin.png) 

**Webhely**

A comScore-webhely azt határozza meg, hogy melyik webhelyről érkező adatokat kívánja megtekinteni. A comScore-fiókból elérheti a webhelyek listáját.

![](media/service-connect-to-connect-to/comscore_sites.png)

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

