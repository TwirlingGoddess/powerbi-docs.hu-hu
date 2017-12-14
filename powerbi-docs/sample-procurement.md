---
title: "Beszerzéselemzési minta: bemutató"
description: "Beszerzéselemzési minta a Power BI-hoz: bemutató"
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
ms.date: 10/28/2017
ms.author: mihart
ms.openlocfilehash: 576ddfbbf52a2738dd32597479ffd03d554a5256
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="procurement-analysis-sample-for-power-bi-take-a-tour"></a>Beszerzéselemzési minta a Power BI-hoz: bemutató
Ez az iparági mintaként szolgáló irányítópult és a mögöttes jelentés egy gyártással foglalkozó cég beszállítói költségeit elemzi kategória és hely szerint. A mintában az alábbi területek ismerhetők meg:

* Kik a fő beszállítók?
* Mely kategóriák költségei a legmagasabbak?
* Mely beszállítók biztosítják a legnagyobb kedvezményeket, és mikor?

Ez a minta egy olyan sorozat részét képezi, amely bemutatja, hogyan használhatja a Power BI-t üzleti adatokkal, jelentésekkel és irányítópultokkal. Az adatok az obviEnce-től ([www.obvience.com](http://www.obvience.com/)) származó valós, de anonimizált adatok.

![](media/sample-procurement/procurement1.png)

Szeretné követni a leírást? A [Power BI szolgáltatásban](https://powerbi.com) keresse meg az **Adatok beolvasása > Minták > Beszerzéselemzési minta > Kapcsolódás** elemet a minta saját példányának beszerzéséhez.

[Letöltheti kizárólag a minta adatkészletét (Excel-munkafüzetét) is](http://go.microsoft.com/fwlink/?LinkId=529784).

## <a name="spending-trends"></a>Költési trendek
Először nézzük meg a költési trendeket kategória és hely szerint.  

1. A munkaterületen nyissa meg az **Irányítópultok** lapot, és válassza a Beszerzéselemzés nevű irányítópultot.
2. Válassza ki a **Teljes számla ország/régió szerint** nevű csempét az irányítópulton. Megjelenik a Beszerzéselemzési minta című jelentés Költések áttekintése nevű lapja.
   
    ![](media/sample-procurement/procurement2.png)

Az alábbiak figyelhetők meg:

* A **Teljes számla hónap és kategória szerint** nevű vonaldiagramon: a **Közvetlen** kategória következetes költéssel rendelkezik, a **Logisztika** kategória csúcsértéke decemberben van, míg az **Egyéb** nevű kategóriáé februárban.
* A **Teljes számla ország/régió** szerint nevű térképen:
a költések többsége az Egyesült Államokban történik.
* A **Teljes számla alkategória szerint** nevű oszlopdiagramon:
a **Hardver**, valamint a **Közvetett termékek és szolgáltatások** képviselik a legnagyobb költési kategóriát.
* A Teljes számla szint szerint nevű sávdiagramon: az ügyfelek többsége 1. szintű (első 10-be tartozó) beszállítónak minősül. Ez segít a beszállítói kapcsolatok jobb kezelésében.

## <a name="spending-in-mexico"></a>Mexikói költések
Nézzük meg a mexikói költési területeket.

1. A tortadiagramon válassza ki a **Mexikó** nevű térképbuborékot. Látható, hogy a Teljes számla alkategória szerint nevű oszlopdiagramon a legtöbb kategóriát a **Közvetett termékek és szolgáltatások** alkategória képviseli.
   
   ![](media/sample-procurement/pbi_procsample_spendmexico.png)
2. Részletezheti a **Közvetett termékek és szolgáltatások** nevű oszlopot:
   
   * Válassza ki a lehatolási nyilat ![](media/sample-procurement/pbi_drilldown_icon.png) a diagram jobb felső sarkában.
   * Válassza ki a **Közvetett termékek és szolgáltatások** nevű oszlopot.
     
      Ebben a kategóriában a legnagyobb költést az értékesítés és a marketing képviseli.
   * Válassza ki újra **Mexikót** a térképen.
     
      A legnagyobb mexikói költés ebben a kategóriában a karbantartás és a javítás.
     
      ![](media/sample-procurement/pbi_procsample_drill_mexico.png)
3. Válassza ki a felfelé mutató nyilat a diagram bal felső sarkában a felhatoláshoz.
4. Válassza ki a nyilat újra a lehatolás kikapcsolásához.  
5. A **Power BI** elem felső navigációs sávon való kiválasztásával térhet vissza a munkaterületre.

## <a name="evaluate-different-cities"></a>Különböző városok értékelése
A kiemelések használatával értékelheti a különböző városokat.

1. Válassza ki a **Teljes számla és kedvezményszázalék hónap szerint** nevű csempét az irányítópulton. A jelentésben megnyílik a Kedvezmény elemzése lap.
2. A **Teljes számla város szerint** fatérképen az egyes városok kiválasztásával hasonlíthatja össze őket. A Miamihoz tartozó szinte összes számla 1. szintű beszállítóktól származik.
   
   ![](media/sample-procurement/pbi_procsample_miamitreemap2.png)

## <a name="vendor-discounts"></a>Beszállítói kedvezmények
Most tekintsük át a beszállítóktól származó kedvezményeket, valamint azokat az időszakokat, amikor a legtöbb kedvezményt kapjuk. 

![](media/sample-procurement/procurement4.png)

Pontosabban az alábbi kérdéseket tehetjük fel:

* A kedvezmények eltérnek-e havonként, vagy megegyeznek minden egyes hónapban?
* Egyes városok több kedvezményt kapnak-e más városokhoz képest?

### <a name="discount-by-month"></a>Kedvezmény havonta
A **Teljes számla és kedvezményszázalék hónap szerint** nevű kombinált diagramon látható, hogy **február** a leginkább, és **szeptember** a legkevésbé forgalmas hónap. Most nézzük meg az ezekhez a hónapokhoz tartozó kedvezményszázalékot.
Látható, hogy a mennyiség növekedésével a kedvezmény mértéke csökken, valamint ha a mennyiség alacsony, a kedvezmény megnő. Minél több kedvezményre van szükség, annál kedvezőtlenebb ajánlatot kapunk.

![](media/sample-procurement/procurement5.png)

### <a name="discount-by-city"></a>Kedvezmény városonként
Egy másik feltárható terület a városonként kapott kedvezmény. Válassza ki az egyes városokat a fatérképen, és láthatja, hogyan változik a többi diagram. 

* St. Louis-ban (Missouri) csúcsértéket ért el februárban a teljes számlaérték, valamint áprilisban esett a legalacsonyabb szintre a kedvezményekkel elérhető megtakarítás.
* A mexikói Mexikóvárosban a legmagasabb a kedvezményszázalék értéke (11,05%), míg Atlantában (Georgia) a legkisebb (0,08%).

![](media/sample-procurement/procurement6.png)

### <a name="edit-the-report"></a>A jelentés szerkesztése
Válassza ki a **Jelentés szerkesztése** elemet a bal felső sarokban, és nyissa meg a szerkesztési nézetet.

* Áttekintheti a lapok felépítését
* Lapokat és diagramokat vehet fel ugyanazon adatok alapján
* Módosíthatja a diagram vizualizációs típusát – például fatérképről gyűrűdiagramra
* Rögzítheti azokat az irányítópulton

Ebben a környezetben nyugodtan kísérletezhet. Nem kötelező menteni a módosításokat. De ha mégis mentené őket, bármikor lekérheti a minta új másolatát az **Adatok lekérése** lehetőséggel.

## <a name="next-steps-connect-to-your-data"></a>Következő lépések: Kapcsolódás saját adatokhoz
Reméljük, ez a bemutató segített megérteni a Power BI-beli irányítópultok és jelentések segítségével történő beszerzési adatelemzést. Most Önön a sor &#151; kapcsolódjon a saját adataihoz. A Power BI-jal számos adatforráshoz kapcsolódhat. Tudjon meg többet a [Power BI használatának első lépéseiről](service-get-started.md).

