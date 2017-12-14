---
title: "Csatlakozás a SparkPosthoz a Power BI használatával"
description: SparkPost a Power BI-hoz
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
ms.openlocfilehash: 93d124bef56bbb6aeb266844e9b3b633df057fa0
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-sparkpost-with-power-bi"></a>Csatlakozás a SparkPosthoz a Power BI használatával
A Power BI SparkPosthoz készült tartalomcsomagja lehetővé teszi a SparkPost-fiók értékes adatkészleteinek kinyerését egyetlen informatív irányítópultra. A SparkPost-tartalomcsomag segítségével megjelenítheti a teljes levelezés statisztikai adatait, beleértve a tartományokat, a kampányokat és az internetszolgáltató által generált érdeklődést is.

Csatlakozás a [Power BI-hoz készült SparkPost-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/spark-post).

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
   ![](media/service-connect-to-sparkpost/getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-sparkpost/services.png)
3. Válassza ki a **SparkPost**-tartalomcsomagot, és kattintson a **Beolvasás** elemre. 
   
   ![](media/service-connect-to-sparkpost/sparkpost.png)
4. Amikor a rendszer kéri, adja meg a SparkPost API-kulcsot, és kattintson a Bejelentkezés elemre. A [paraméter megkereséséről](#FindingParams) alább olvashat részletesebben.
   
   ![](media/service-connect-to-sparkpost/creds.png)
5. Megkezdődik az adatok betöltése, ami a fiók méretétől függően eltarthat egy ideig. Miután a Power BI importálta az adatokat, a bal oldali navigációs ablaktáblán megjelenik az alapértelmezett irányítópult, a jelentés és az adatkészlet, amely az elmúlt 90 nap levelezési statisztikáit tartalmazza. Az új elemeket sárga csillag jelöli \*.
   
   ![](media/service-connect-to-sparkpost/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="whats-included"></a>A csomag tartalma
A Power BI-hoz készült SparkPost-tartalomcsomag többek között ezeket az információkat tartalmazza: egyedi kattintások, elfogadások aránya, visszapattanások aránya, késleltetések aránya, visszautasítások aránya.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
A tartalomcsomag egy API-kulcsot használ a SparkPost-fiók és a Power BI csatlakoztatásához. Az API-kulcsot a fiókjában találja meg a Fiók \> API & SMTP helyen (további részletek [itt](https://support.sparkpost.com/customer/portal/articles/1933377-create-api-keys)). Javasoljuk, hogy olyan API-kulcsot használjon, amely a következő engedélyekkel rendelkezik: `Message Events: Read-only ` és `Metrics: Read-only`

![](media/service-connect-to-sparkpost/sparkpost1.png)

