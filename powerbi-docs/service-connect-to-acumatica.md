---
title: "Csatlakozás az Acumatica eszközhöz a Power BI-ban"
description: Acumatica a Power BI-ban
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
ms.openlocfilehash: dd64f4fb4651e393e770dda9323c10356424c780
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-acumatica-with-power-bi"></a>Csatlakozás az Acumatica eszközhöz a Power BI-ban
A Power BI-hoz készült Acumatica tartalomcsomaggal gyors elemzéseket kaphat a lehetőségadatokról. A Power BI lekéri többek között a lehetőségek, a fiókok és az ügyfelek adatait, majd ezek alapján felépíti az alapértelmezett irányítópultot és a kapcsolódó jelentéseket.

Kapcsolódjon az [Acumatica tartalomcsomaghoz](https://app.powerbi.com/getdata/services/acumatica), vagy tájékozódjon bővebben az [Acumatica és a Power BI integrációjáról](https://powerbi.microsoft.com/integrations/acumatica).

>[!NOTE]
>Ehhez a tartalomcsomaghoz az Acumatica v5.2-es vagy újabb verziója szükséges.

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
   ![](media/service-connect-to-acumatica/getdata3.png)
2. A **Szolgáltatások** mezőben kattintson a **Beolvasás** elemre.
   
   ![](media/service-connect-to-acumatica/getdata2.png)
3. Kattintson az **Acumatica** \> **Beolvasás** elemre.
   
   ![](media/service-connect-to-acumatica/acumatica.png)
4. Adja meg az Acumatica OData-végpontját. Az OData-végpont teszi lehetővé, hogy egy külső rendszer adatokat kérjen az Acumatica eszköztől. Az Acumatica OData-végpontja az alábbiak szerint van formázva, és HTTPS-t használ:
   
     https://[sitedomain]/odata/[companyname]
   
   A Cég neve adatra csak akkor van szükség, ha többvállalatos üzemelő példánnyal dolgozik. Az Acumatica-fiók ezen paraméterének megkereséséről alább talál további információkat.
   
   ![](media/service-connect-to-acumatica/parameters.png)
5. A Hitelesítési módszer beállításánál válassza az **Alapszintű** lehetőséget. Adja meg az Acumatica-fiókhoz tartozó felhasználónevét és a jelszavát, majd kattintson a **Bejelentkezés** elemre.
   
    ![](media/service-connect-to-acumatica/creds2.png)
6. Miután a Power BI importálta az adatokat, a bal oldali navigációs ablaktáblán új irányítópult, jelentés és modell jelenik meg. Az új elemeket sárga csillag jelöli \*, amely a rákattintás után eltűnik; az irányítópult kijelölése után az alábbi képhez hasonló elrendezés jelenik meg:
   
    ![](media/service-connect-to-acumatica/dashboard.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson az egyik csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor az **Azonnali frissítés** lehetőségre kattintva.

## <a name="system-requirements"></a>Rendszerkövetelmények
Ehhez a tartalomcsomaghoz az Acumatica v5.2-es vagy újabb verziója szükséges, ezért kérjük, hogy ellenőrizze a verziót az Acumatica rendszergazdájának segítségével.

## <a name="finding-parameters"></a>Paraméterek keresése
**Acumatica OData-végpont**

Az Acumatica OData-végpontja az alábbiak szerint van formázva, és HTTPS-t használ:

    https://[sitedomain]/odata/[companyname]

Ha be van jelentkezve az Acumatica szolgáltatásba, az alkalmazástartomány a böngésző címsorában látható. Az alábbi példában a webhely tartománya: „https://pbi.acumatica.com”, tehát a következő OData-végpontot kell megadnia: „https://pbi.acumatica.com/odata”.

 ![](media/service-connect-to-acumatica/url.png)

A Cég neve adatra csak akkor van szükség, ha többvállalatos üzemelő példánnyal dolgozik. Ez az információ az Acumatica bejelentkezési oldalán található.

![](media/service-connect-to-acumatica/signin2.png)

## <a name="troubleshooting"></a>Hibaelhárítás
Ha nem tud bejelentkezni, ellenőrizze hogy a helyesen formázott Acumatica OData-végpontot adta-e meg.

    https://<application site domain>/odata/<company name>

Ha nem sikerül a csatlakozás, kérje a rendszergazda segítségét az Acumatica verziójának ellenőrzéséhez. Ehhez a tartalomcsomaghoz 5.2-es, vagy újabb verzióra van szükség.

## <a name="next-steps"></a>Következő lépések
[Power BI – első lépések](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

