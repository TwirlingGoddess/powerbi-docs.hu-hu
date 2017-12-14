---
title: "Első lépések a Power BI Q&A használatában (oktatóanyag)"
description: "Oktatóanyag: első lépések a Q&A kiskereskedelmi elemzési mintákon való használatában a Power BI szolgáltatásban"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: 
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/25/2017
ms.author: mihart
ms.openlocfilehash: 2038fb5bd4a21235c3026c8506ae30b8c3e287e4
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="get-started-with-power-bi-qa-tutorial"></a>Első lépések a Power BI Q&A használatában (oktatóanyag)
## <a name="tutorial-use-power-bi-qa-with-the-retail-analysis-sample"></a>Oktatóanyag: a Power BI Q&A használata a kiskereskedelmi elemzési mintával
Néha a leggyorsabb módja, hogy válaszokat kapjon az adatokból, ha a természetes nyelvet használja kérdezésre.  Ebben az oktatóanyagban két különböző módszert is megtekintünk ugyanannak a vizualizációnak a létrehozására: felépítjük egy jelentésben, és kérdést teszünk fel a Q&A-val.  

## <a name="method-1-using-the-report-editor"></a>1. módszer: a jelentésszerkesztő használatával
1. Válassza a Power BI munkaterületén az **Adatok beolvasása** \> **Minták** \> **Kiskereskedelmi elemzési minta** > **Csatlakozás** menüpontot.
   
    ![](media/power-bi-visualization-introduction-to-q-and-a/power-bi-dashboard.png)
2. Az irányítópult tartalmaz egy területdiagram-csempét „Last Year Sales and This Year Sales.” (Elmúlt évi értékesítések és idei értékesítések) címmel.  Jelölje ki ezt a csempét. 
   
   * Ha ezt a csempét a Q&A-val hozták létre, a csempe kijelölésekor megnyílik a Q&A. 
   * Ezt a csempét azonban egy jelentésben hozták létre, ezért a jelentés megnyílik a vizualizációt tartalmazó oldalon.
3. Nyissa meg a jelentést szerkesztési nézetben a **Jelentés szerkesztése** lehetőséget választva.  Ha nem tulajdonosa a jelentésnek, akkor nem lesz lehetősége azt szerkesztési nézetben megnyitni.
   
    ![](media/power-bi-visualization-introduction-to-q-and-a/power-bi-edit-report.png)
4. Jelölje ki a területdiagramot, és tekintse át a beállításokat a **Mezők** ablaktáblán.  A jelentés létrehozója ennek a 3 értéknek a kiválasztásával építette fel a jelentést: (**Idő > FiscalMonth**, **Értékesítések > This Year Sales (Idei értékesítések)**, **Értékesítések > Last Year Sales (Múlt évi értékesítések) > Érték**), és ezeket a **Tengely** és az **Értékek** mezőterületen rendezte el.
   
    ![](media/power-bi-visualization-introduction-to-q-and-a/gnatutorial_3-new.png)

## <a name="method-2-using-qa"></a>2. módszer: a Q&A használatával
Hogyan lehet létrehozni ugyanezt a vonaldiagramot a Q&A-val?

![](media/power-bi-visualization-introduction-to-q-and-a/power-bi-qna.png)

1. Térjen vissza a Kiskereskedelmi elemzési minta irányítópulthoz.
2. A természetes nyelvet használva írjon be valami ehhez hasonlót a kérdezési mezőbe:
   
   **hogyan alakult az idei és a múlt évi értékesítés havi bontásban, területdiagramon ábrázolva**
   
   A kérdés beírása közben a Q&A kiválasztja a legjobb vizualizációt a válasz megjelenítéséhez; a kérdés módosítása közben a vizualizáció dinamikusan változik. A Q&A segít a kérdés megfogalmazásában is javaslatokkal, automatikus kiegészítéssel és helyesírási javításokkal.
   
   Amikor befejezi a kérdés beírását, az eredmény pontosan ugyanaz a diagram lesz, amelyet a jelentésben láttunk.  De így sokkal gyorsabban létre lehet hozni!
   
   ![](media/power-bi-visualization-introduction-to-q-and-a/powerbi-qna-areachart.png)
3. A jelentésekkel való munkavégzéshez hasonlóan a Q&A-ban hozzáférhet a Megjelenítések, a Szűrők és a Mezők ablaktáblához.  Nyissa meg ezeket az ablaktáblákat a vizualizáció további felfedezéséhez és módosításához.
4. A diagram irányítópultra való kitűzéséhez válassza a gombostű ikont ![](media/power-bi-visualization-introduction-to-q-and-a/pinnooutline.png).

## <a name="next-steps"></a>Következő lépések
[Milyen típusú kérdéseket tehetek fel a Q&A-nak?](service-q-and-a.md)

[Q&A a Power BI-ban](service-q-and-a.md)

[Megfelelő adatműködés biztosítása a Q&A és a Power BI használatánál](service-prepare-data-for-q-and-a.md)

[munkafüzet előkészítése a Q&A-hoz](service-prepare-data-for-q-and-a.md)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

