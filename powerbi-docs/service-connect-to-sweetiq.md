---
title: "Kapcsolódás a SweetIQ-hoz a Power BI-jal"
description: SweetIQ a Power BI-hoz
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
ms.openlocfilehash: df80e986a4ad42018c5ba036c2e47e684dba65d3
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-sweetiq-with-power-bi"></a>Kapcsolódás a SweetIQ-hoz a Power BI-jal
A Power BI-tartalomcsomag a SweetIQ-fiókban található adatait használja, és előre elkészített tartalmakat generál, hogy egyszerűen feltárhassa az adatokat. A SweetIQ-tartalomcsomagot a helyeire, listáira, minősítéseire és értékeléseire vonatkozó adatok elemzésére használhatja. Az alapértelmezett beállítások szerint az adatok naponta frissülnek, hogy Ön mindig naprakész adatokat ellenőrizhessen.

Kapcsolódjon a Power BI-hoz készült [SweetIQ-tartalomcsomaghoz](https://app.powerbi.com/groups/me/getdata/services/sweetiq).

## <a name="how-to-connect"></a>A csatlakozás menete
1. A bal oldali navigációs sávon kattintson az **Adatok lekérése** gombra.
   
    ![](media/service-connect-to-sweetiq/getdata.png)
2. Válassza a **SweetIQ** lehetőséget, és kattintson a **Beolvasás** gombra.
   
    ![](media/service-connect-to-sweetiq/sweetiq.png)
3. Adja meg a SweetIQ-beli ügyfél-azonosítóját. Ez általában egy alfanumerikus érték. Az érték megkeresésére vonatkozó további részleteket lásd alább.
   
    ![](media/service-connect-to-sweetiq/parameter.png)
4. Válassza a **Kulcs** hitelesítési típust, és adja meg a SweetIQ API-kulcsát. Ez általában egy alfanumerikus érték. Az érték megkeresésére vonatkozó további részleteket lásd alább.
   
    ![](media/service-connect-to-sweetiq/credentials.png)
5. A Power BI elkezdi betölteni az adatokat, ami eltarthat egy ideig a fiókban található adatok méretétől függően. Miután befejeződött a betöltés, a bal oldali navigációs ablaktáblán megjelenik egy új irányítópult, jelentés és adatkészlet.
   
    ![](media/service-connect-to-sweetiq/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található.
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson az egyik csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="finding-parameters"></a>Paraméterek keresése
Ennek a tartalomcsomagnak az ügyfél-azonosítója és API-kulcsa nem azonos a SweetIQ-beli felhasználónevével és jelszavával.

Válassza az egyik olyan ügyfél azonosítóját, amelyhez a fiókja rendelkezik hozzáféréssel. Az ügyfelek listáját a SweetIQ-fiókja „Client Management” (Ügyfélkezelés) területén találja.

Az adott ügyfél adainak eléréséhez szükséges API-kulcs beszerzéséért beszéljen a rendszergazdával.

## <a name="next-steps"></a>Következő lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatbeolvasás a Power BI-ban](service-get-data.md)

