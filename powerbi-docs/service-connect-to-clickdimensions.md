---
title: "Csatlakozás a ClickDimensions eszközhöz a Power BI-ban"
description: ClickDimensions a Power BI-ban
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
ms.openlocfilehash: cde6ca545d37b2ba490578bf43e7de95b10931d7
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-clickdimensions-with-power-bi"></a>Csatlakozás a ClickDimensions eszközhöz a Power BI-ban
A Power BI-hoz készült ClickDimensions tartalomcsomag lehetővé teszi, hogy a felhasználók a ClickDimensions marketingadataival dolgozhassanak a Power BI-ban, és további elemzéseket nyújt a vezetői csoportoknak a marketingmunka és az értékesítések elemzéséhez. A Power BI irányítópultjainak és jelentéseinek segítségével vizualizálhatja és elemezheti az e-mail-interakciókat, a webes látogatásokat és az űrlapbeküldéseket.

Csatlakozzon a Power BI-hoz készült [ClickDimensions tartalomcsomaghoz](https://app.powerbi.com/getdata/services/click-dimensions).

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktáblán.
   
   ![](media/service-connect-to-clickdimensions/getdata.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** elemre.
   
   ![](media/service-connect-to-clickdimensions/services.png)
3. Kattintson a **ClickDimensions** \> **Beolvasás** elemre.
   
   ![](media/service-connect-to-clickdimensions/clickdimensions.png)
4. Adja meg az adatközpontja helyét (Egyesült Államok, Európa vagy Ausztrália), és kattintson a **Tovább** elemre.
   
   ![](media/service-connect-to-clickdimensions/params.png)
5. A **Hitelesítési módszer** beállításánál kattintson az **Alapszintű** \> **Bejelentkezés** elemre. Amikor a rendszer kéri, adja meg a ClickDimensions eszközben használt hitelesítő adatait. A [paraméterek megkereséséről](#FindingParams) alább olvashat részletesebben
   
    ![](media/service-connect-to-clickdimensions/creds.png)
6. A jóváhagyás után automatikusan megkezdődik az importálás. Amikor a folyamat befejeződik, a navigációs ablaktáblán új irányítópult, jelentés és modell jelenik meg. Az importált adatok megtekintéséhez kattintson az irányítópultra.
   
     ![](media/service-connect-to-clickdimensions/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson az egyik csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor az **Azonnali frissítés** lehetőségre kattintva.

## <a name="system-requirements"></a>Rendszerkövetelmények
A Power BI-hoz történő csatlakozáshoz meg kell adnia a fiókjához tartozó adatközpontot, és be kell jelentkeznie a ClickDimensions-fiókjával. Ha nem tudja pontosan, hogy melyik adatközpontot kell megadnia, forduljon a rendszergazdához.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
A fiókkulcs a CRM Beállítások \> ClickDimensions Beállítások helyen található. Másolja ki a fiókkulcsot a ClickDimensions Beállítások helyről, és illessze be a Felhasználónév mezőbe.  

![](media/service-connect-to-clickdimensions/crm.png)  

Másolja ki a Power BI-jogkivonatot a ClickDimensions Beállítások helyről, és illessze be a Jelszó mezőbe. A Power BI-jogkivonat a CRM Beállítások \> ClickDimensions Beállítások helyen található.  

![](media/service-connect-to-clickdimensions/crm2.png)  

## <a name="next-steps"></a>Következő lépések
[Power BI – első lépések](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

