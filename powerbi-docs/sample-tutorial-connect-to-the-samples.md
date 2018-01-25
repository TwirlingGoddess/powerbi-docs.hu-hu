---
title: "Power BI-példák használata, oktatóanyag."
description: "Oktatóanyag: Power BI-példák használata"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: monitoring
qualitydate: 03/08/2017
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/27/2017
ms.author: mihart
ms.openlocfilehash: d92edce9ae1332c4a0c73be5db93201c9b87dc86
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/19/2018
---
# <a name="the-power-bi-samples-a-tutorial"></a>Power BI-példák, oktatóanyag
<!-- Shared newnav Include -->
[!INCLUDE [newnavbydefault](./includes/newnavbydefault.md)]

Javasoljuk, hogy először [A Power BI mintaként használható adatkészletei](sample-datasets.md) cikket olvassa el. Ebben a cikkben megismerkedhet a mintákkal, azok beszerzésével, mentési helyével, használatával, valamint az egyes mintákhoz kapcsolódó történetekkel. Ha pedig már tisztában van az alapokkal, akkor térjen vissza ehhez az oktatóanyaghoz.   

## <a name="about-this-tutorial"></a>Az oktatóanyag ismertetése
Ez az oktatóanyag megismerteti a mintaként használható tartalomcsomagok importálásának, a csomagoknak a Power BI szolgáltatáshoz történő hozzáadásának, valamint a tartalmak megnyitásának módjával. A *tartalomcsomagok* olyan típusú minták, ahol az adatkészlethez irányítópult és jelentés is mellékelve van. A mintaként használható tartalomcsomagok a Power BI-ban az **Adatok lekérése** funkció használatával érhetőek el.

> [!NOTE]
> Ez az oktatóanyag a Power BI szolgáltatásra és a Power BI Desktopra egyaránt vonatkozik.
> 
> 

Az ebben az oktatóanyagban használt *Kiskereskedelmi elemzési* minta tartalomcsomag irányítópultot, jelentést és adatkészletet is tartalmaz.
Ahhoz, hogy megismerkedjen az adott tartalomcsomaggal és az ahhoz tartozó forgatókönyvvel, lehetséges, hogy először érdemes megtekintenie [a Kiskereskedelmi elemzési minta bemutatóját](sample-retail-analysis.md).

## <a name="get-data-in-this-case-get-a-sample-content-pack"></a>Adatok lekérése (ebben az esetben egy minta tartalomcsomag lekérése)
1. Nyissa meg a Power BI szolgáltatást, és jelentkezzen be (app.powerbi.com).
2. Válasszon ki egy munkaterületet, és hozzon létre egy új irányítópultot.  
   
    ![](media/sample-tutorial-connect-to-the-samples/power-bi-create-dashboard2.png)
3. Nevezze el a következőképpen: **Kiskereskedelmi elemzési minta**.
   
   ![](media/sample-tutorial-connect-to-the-samples/power-bi-name-dashboard.png)
4. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre. Ha nem látja az **Adatok lekérése** elemet, a ![](media/sample-tutorial-connect-to-the-samples/expand-nav.png) lehetőség kiválasztásával bővítse ki a navigációs panelt.
   
   ![](media/sample-tutorial-connect-to-the-samples/pbi_getdata.png)
5. Válassza a **Minták** lehetőséget.  
   
   ![](media/sample-tutorial-connect-to-the-samples/pbi_samplesdownload.png)
6. Válassza a *Kiskereskedelmi elemzési minta* elemet, majd a **Kapcsolódás** lehetőséget.   
   
   ![](media/sample-tutorial-connect-to-the-samples/pbi_retailanalysissampleconnect.png)

## <a name="what-exactly-was-imported"></a>Pontosan mit is importáltunk?
A mintaként használható tartalomcsomagok esetében a **Kapcsolódás** lehetőség kiválasztásakor a Power BI tulajdonképpen az adott tartalomcsomag másolatát tölti be és tárolja az Ön számára a felhőben. Mivel a tartalomcsomagot létrehozó személy adatkészletet, jelentést és irányítópultot is foglalt a csomagba – a **Kapcsolódás** lehetőségre történő kattintáskor mindezek lekérése megtörténik.

1. A Power BI létrehozza az új irányítópultot, és felveszi azt az **Irányítópultok** lapon található listára. Sárga csillag jelzi, hogy új elemről van szó.
   
   ![](media/sample-tutorial-connect-to-the-samples/power-bi-new-dashboard.png)
2. Nyissa meg a **Jelentések** lapot.  Itt egy új, *Retail Analysis Sample* (Kiskereskedelmi elemzési minta) nevű jelentést fog látni.
   
   ![](media/sample-tutorial-connect-to-the-samples/power-bi-new-report.png)
   
   Ezt követően tekintse meg az **Adatkészletek** lapot.  Található itt egy új adatkészlet is.
   
   ![](media/sample-tutorial-connect-to-the-samples/power-bi-new-dataset.png)

## <a name="explore-your-new-content"></a>Az új tartalmak vizsgálata
Most vizsgálja meg saját maga is az irányítópultot, az adatkészletet és a jelentést. Számos lehetséges módja van az irányítópultok, jelentések és adatkészletek közötti navigációnak, az alábbiakban ezek közül csupán egyet mutatunk be.  

> [!TIP]
> Szeretne egy kis kezdeti segítséget?  [A Kiskereskedelmi elemzési minta bemutatója](sample-retail-analysis.md) részletes útmutatóval szolgál ehhez a mintához.
> 
> 

1. Lépjen vissza az **Irányítópultok** lapra, és válassza a *Retail Analysis Sample* (Kiskereskedelmi elemzési minta) irányítópultot annak megnyitásához.    
   
   ![](media/sample-tutorial-connect-to-the-samples/power-bi-dashboards.png)
2. Ekkor megnyílik az irányítópult.  Az irányítópulton számos vizualizáció-csempe található.
   
   ![](media/sample-tutorial-connect-to-the-samples/power-bi-dashboards2new.png)
3. Válassza ki az egyik csempét az alapul szolgáló jelentés megnyitásához.  Ebben a példában a területdiagramot (rózsaszín kerettel jelöltük az előző képen) választjuk ki. A jelentés a területdiagramot tartalmazó oldalnál nyílik meg.
   
    ![](media/sample-tutorial-connect-to-the-samples/power-bi-report.png)
   
   > [!NOTE]
   > Ha az adott csempe a [Power BI Q&A](power-bi-q-and-a.md) szolgáltatásával lett létrehozva, akkor a Q&A oldalnak kellett volna megnyílnia.
   > 
   > 
4. Lépjen vissza az **Adatkészletek** lapra, ahol az adatkészlet átvizsgálását illetően számos lehetőség közül választhat.  Nem tudja megnyitni és megtekinteni az összes sort és oszlopot (ahogy a Power BI Desktop vagy az Excel esetében meg tudná tenni).  Ha valaki megoszt egy tartalomcsomagot a kollégáival, akkor jellemzően az elemzéseket kívánja megosztani, nem pedig közvetlen hozzáférést adni a kollégáinak az adatokhoz. Ez azonban nem jelenti azt, hogy ne tudná elvégezni az adatkészlet átvizsgálását.  
   
   ![](media/sample-tutorial-connect-to-the-samples/power-bi-chart-icon2.png)
   
   * Az adatkészlet átvizsgálásának egyik módja, ha az alapoktól kezdve létrehozza saját vizualizációit és jelentéseit.  Kattintson a diagram ikonra ![](media/sample-tutorial-connect-to-the-samples/power-bi-chart-icon4.png) az adatkészlet jelentésszerkesztési módban történő megnyitásához.
     
       ![](media/sample-tutorial-connect-to-the-samples/power-bi-report-editing.png)
   * Az adatkészlet átvizsgálásának másik módja a [Gyors elemzések](service-insights.md) szolgáltatás futtatása. Kattintson a három pontra (...), és válassza az **Elemzések lekérése** lehetőséget. Ha az elemzések elkészültek, válassza az **Elemzések megtekintése** lehetőséget.
     
       ![](media/sample-tutorial-connect-to-the-samples/power-bi-insights.png)

## <a name="next-steps"></a>Következő lépések
[Power BI – Alapfogalmak](service-basic-concepts.md)

[Minták a Power BI szolgáltatáshoz](sample-datasets.md)

[Power BI-adatforrások](service-get-data.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

