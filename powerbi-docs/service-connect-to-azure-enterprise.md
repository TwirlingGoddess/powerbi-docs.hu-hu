---
title: "Csatlakozás a Microsoft Azure Enterprise-hoz a Power BI használatával"
description: Microsoft Azure Enterprise a Power BI-hoz
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
ms.openlocfilehash: 39c3fd776e3aed821c7c10c1e905d7400ca64efd
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-microsoft-azure-enterprise-with-power-bi"></a>Csatlakozás a Microsoft Azure Enterprise-hoz a Power BI használatával
A Power BI-tartalomcsomag segítségével a Power BI-ban vizsgálhatja és figyelheti Microsoft Azure Enterprise-beli adatait. Az adatok naponta egyszer automatikusan frissülnek.

Csatlakozás a [Microsoft Azure Enterprise-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/azure-enterprise) a Power BI használatával.

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
    ![](media/service-connect-to-azure-enterprise/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-azure-enterprise/services.png)
3. Kattintson a **Microsoft Azure Enterprise** \> **Beolvasás** elemre.
   
   ![](media/service-connect-to-azure-enterprise/mazureenterprise.png)
4. Adja meg az Azure-környezet URL-címét, az Azure Enterprise regisztrációs számát, és azt, hogy hány havi adatot kíván importálni. Az Azure-környezet URL-címe `https://ea.azure.com` vagy `https://ea.windowsazure.cn`. A [paraméterek megkereséséről](#FindingParams) alább olvashat részletesebben.
   
    ![](media/service-connect-to-azure-enterprise/params.png)
5. A csatlakozáshoz adja meg a hozzáférési kulcsot. A regisztrációjához tartozó kulcsot az Azure EA-portálon találja meg.
   
    ![](media/service-connect-to-azure-enterprise/creds.png)
6. Az importálás automatikusan megkezdődik. Amikor befejeződik, a navigációs ablaktáblán megjelenik egy új irányítópult, jelentés és modell. Kattintson az irányítópultra az importált adatok megtekintéséhez.
   
   ![](media/service-connect-to-azure-enterprise/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="whats-included"></a>A csomag tartalma
Az Azure Enterprise-tartalomcsomag havi adatjelentéseket nyújt a kapcsolódási folyamat során megadott hónapok időtartamára. A tartomány változó időintervalluma miatt az adatkészlet frissülésével a benne foglalt adatok is frissülnek.

## <a name="system-requirements"></a>Rendszerkövetelmények
A tartalomcsomag használatához hozzáférésre van szükség az Azure Portal-beli Enterprise-funkciókhoz.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
A Power BI jelentései elérhetőek az EA mindazon közvetlen, partner- és közvetett ügyfelei számára, akik láthatják a számlázási adatokat. A kapcsolódási folyamathoz szükséges értékek megkereséséről alább tájékozódhat.

**Az Azure-környezet URL-címe**

* Ez általában a https://ea.azure.com, de bejelentkezéskor ellenőrizheti a megjelenő URL-címet.
  
    ![](media/service-connect-to-azure-enterprise/params3.png)

**Hónapok száma**

* 1 és 36 közötti érték, amely a jelentésben elemzett (mai naptól számított) hónapok számát adja meg.

**Regisztrációs szám**

* Az Ön Azure Enterprise regisztrációs száma, amely az [Azure Enterprise Portal](https://ea.azure.com/) kezdőképernyőjén jelenik meg az „Enrollment Detail” (Regisztrációs adatok) felirat alatt.
  
    ![](media/service-connect-to-azure-enterprise/params2.png)

**Hozzáférési kulcs**

* A kulcs az Azure Enterprise portálon található meg, a „Download Usage" > „API Access Key" résznél.
  
    ![](media/service-connect-to-azure-enterprise/creds2.png)

**További segítség**

* A Power BI-hoz készült Azure Enterprise-tartalomcsomaghoz további segítséget kaphat az Azure Enterprise portálon, az API súgófájl „Súgó” részében, valamint a Reports -> Download Usage -> API Access Key további instrukcióiban.

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

