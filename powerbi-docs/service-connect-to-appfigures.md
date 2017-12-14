---
title: "Csatlakozás az appFigures-hoz a Power BI használatával"
description: appFigures a Power BI-hoz
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
ms.openlocfilehash: 502135583f4d62144a2a2bdb908724c4f8e6b579
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-appfigures-with-power-bi"></a>Csatlakozás az appFigures-hoz a Power BI használatával
A Power BI és az appFigures-tartalomcsomag segítségével egyszerűen nyomon követheti az alkalmazásait leíró fontos statisztikákat. A Power BI adatokat kér le többek között az alkalmazás értékesítéséről, letöltéseiről és hirdetési statisztikáiról, majd felépít egy alapértelmezett irányítópultot, és létrehozza a kapcsolódó jelentéseket.

Csatlakozzon az [appFigures-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/appfigures), vagy tájékozódjon bővebben [az appFigures és a Power BI integrációjáról.](https://powerbi.microsoft.com/integrations/appfigures)

## <a name="how-to-connect"></a>A csatlakozás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
   ![](media/service-connect-to-appfigures/pbi_getdata.png)
2. A **Szolgáltatások** mezőben válassza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-appfigures/pbi_getservices.png)
3. Kattintson az **appFigures** \>  **Get** elemre.
   
   ![](media/service-connect-to-appfigures/appfigures.png)
4. A **Hitelesítési módszer** beállításánál válassza az **oAuth2** \> **Bejelentkezés** lehetőséget. Amikor a rendszer kéri, adja meg az appFigures-beli hitelesítő adatait, majd haladjon végig a hitelesítés folyamatán.
   
   Az első kapcsolódás alkalmával a Power BI kérni fogja, hogy engedélyezze az olvasási hozzáférést a fiókjához. Az **Engedélyezés** elemre kattintva kezdje el az importálási folyamatot. Ez a fiókban tárolt adatok mennyiségétől függően néhány percet is igénybe vehet.
   
   ![](media/service-connect-to-appfigures/appfiguresdoc_06.png)
5. Miután a Power BI importálta az adatokat, a bal oldali navigációs ablaktáblán egy új irányítópult, jelentés és adatkészlet jelenik meg. Az új elemeket sárga csillag jelöli \*:
   
    ![](media/service-connect-to-appfigures/pbi_appfigures3.png)
6. Válassza ki az appFigures irányítópultját. A Power BI ezt az alapértelmezett irányítópultot hozta létre az adatok megjelenítésére. Az irányítópultot módosíthatja, hogy az igényei szerint jelenítse meg az adatokat.
   
    ![](media/service-connect-to-appfigures/appfiguresdoc_01.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](service-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Az adatkészlet naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, az **Azonnali frissítés** lehetőségre kattintva.

## <a name="whats-included"></a>A csomag tartalma
A Power BI-ban a következő, appFigures-ból származó adatok érhetők el.

| **Tábla neve** | **Leírás** |
| --- | --- |
| Országok |Ez a táblázat az országnevekről ad tájékoztatást. |
| Dátumok |Ez a táblázat az appFigures-fiókban lévő aktív és látható alkalmazásokhoz tartozó dátumokat tartalmazza a mai naptól visszamenőleg az adatok közzétételének (PublishDate) legkorábbi időpontjáig. |
| Események |Ez a táblázat a letöltések, értékesítések és hirdetések napi adatait tartalmazza országok szerint az egyes alkalmazásokról. Vegye figyelembe, hogy az alkalmazásértékesítési és az alkalmazáson belüli értékesítési adatok egyaránt ebben a táblázatban szerepelnek – a különbségtételre a <strong>Típus</strong> oszlopot használhatja. |
| Alkalmazáson belüli vásárlások |Ez a táblázat az appFigures-fiókban lévő aktív és látható alkalmazásokhoz hozzárendelt különböző típusú alkalmazáson belüli vásárlások adatait tartalmazza. |
| Termékek |Ez a táblázat az appFigures-fiókban lévő különféle aktív és látható alkalmazások adatait tartalmazza. |

## <a name="troubleshooting"></a>Hibaelhárítás
Ha egy alkalmazás adatai nem jelennek meg a Power BI-ban, ellenőrizze, hogy az alkalmazás látható és aktív-e az appFigures-oldal **alkalmazások** lapján.

![](media/service-connect-to-appfigures/appfiguresdoc_11.png)

## <a name="next-steps"></a>Következő lépések
* [Első lépések a Power BI-ban](service-get-started.md)
* [Adatok beolvasása a Power BI-ban](service-get-data.md)

