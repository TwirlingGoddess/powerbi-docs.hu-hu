---
title: "Csempe rögzítése az irányítópultra a Q&A kérdésmezőből"
description: "Csempe rögzítése Power BI-irányítópultra a Q&A kérdésmezőből – dokumentáció"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/20/2017
ms.author: mihart
ms.openlocfilehash: 8a876c5a05fcdadff1a874148f5d56465bcc8c62
ms.sourcegitcommit: 6ea8291cbfcb7847a8d7bc4e2b6abce7eddcd0ea
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/21/2017
---
# <a name="pin-a-tile-to-a-dashboard-from-qa"></a>Csempe rögzítése az irányítópultra a Q&A kérdésmezőből
## <a name="how-to-pin-a-tile-from-qa"></a>Hogyan rögzíthet csempét a Q&A kérdésmezőből
A Q&A-rendszer a Power BI alkalmi jelentéskészítő eszköze. Konkrét elemzésre van szüksége? Ha feltesz egy kérdést az adatairól, vizualizáció formájában kapja meg a választ.

A Q&A irányítópultokon és jelentésekben érhető el. Ebben a cikkben a Q&A-t egy irányítópulton fogjuk megnyitni. Az irányítópultok csak a Power BI szolgáltatásban érhető el, a Power BI Desktopban nem. Annak érdekében, hogy követni tudja a lépéseket, nyissa meg a [Kiskereskedelmi elemzési minta irányítópultját](sample-retail-analysis.md).
> 
> 

1. Nyisson meg egy [irányítópultot](service-dashboards.md), amelyen már rögzítve van legalább egy csempe valamelyik jelentésből. A kérdés begépelésekor a Power BI minden olyan adatkészletben választ keres, amelyhez az irányítópulton csempe tartozik.  További tudnivalókért lásd: [Adatok beolvasása](service-get-data.md).
2. Az irányítópult tetején látható kérdésmezőbe kezdje beleírni (angolul), hogy mire kíváncsi az adatokkal kapcsolatban.  
   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-question-box.png)
3. Például ha ezt írja: „last year sales by month and territory" (tavalyi eladások hónapok és területek szerint)...  
   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-type-q-and-a.png)
   
   akkor a kérdésmező javaslatokat kínál fel.
4. Ha csempe formájában kívánja rögzíteni a grafikont az irányítópultra, kattintson a gombostű ![](media/service-dashboard-pin-tile-from-q-and-a/pbi_pintile.png) ikonra a vászon jobb felső sarkában.
5. A csempét egy meglévő vagy egy új irányítópultra is rögzítheti. 

   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pin-to-dashboard.png)

   * Meglévő irányítópult: válassza ki az irányítópult nevét a legördülő listából. Csak az aktuális munkaterületeken lévő irányítópultok közül választhat.
   * Új irányítópult: írja be az új irányítópult nevét, és az létrejön a munkaterületen.
6. Kattintson a **Rögzítés** elemre.
   
   A jobb felső sarokban megjelenik a sikert jelző üzenet, amely tájékoztatja, hogy a vizualizáció csempeként hozzá lett adva az irányítópulthoz.  
   
   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pin.png)
7. Az új csempe megtekintéséhez kattintson az **Ugrás az irányítópultra** lehetőségre. Itt [többek között átnevezheti, átméretezheti és áthelyezheti a csempét az irányítópulton, és hivatkozást adhat hozzá](service-dashboard-edit-tile.md). 
   
   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pinned.png)

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
* Amikor elkezdi beírni a kérdést, a Q&A-rendszer máris keresni kezdi a legjobb választ az aktuális irányítópulttal társított adatkészletekben.  Az „aktuális irányítópult” neve a felső navigációs sávon látható. Ezt a kérdést például a **mihart** alkalmazás-munkaterülethez tartozó **Kiskereskedelmi elemzési minta** irányítópulton tették fel.
  
  ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-navbar.png)
* **Honnan tudja a Q&A-rendszer, hogy mely adatkészleteket kell felhasználnia**?  A Q&A minden adatkészlethez hozzáfér, amelynek rögzített vizualizációja van az irányítópulton.

## <a name="next-steps"></a>Következő lépések
[Csempe átnevezése, átméretezése, áthelyezése, hivatkozás hozzáadása, stb.](service-dashboard-edit-tile.md)    
[Irányítópult csempéjének megjelenítése Fókusz módban](service-focus-mode.md)     
[Vissza a Q&A a Power BI-ban című témakörhöz](service-q-and-a.md)  
Több kérdése van? [Felteheti azokat a Power BI-közösségnek](http://community.powerbi.com/)

