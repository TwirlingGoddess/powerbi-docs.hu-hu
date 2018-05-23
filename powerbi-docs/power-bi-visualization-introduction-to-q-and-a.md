---
title: Első lépések a Power BI Q&A-ben
description: Első lépések a Q&A kiskereskedelmi elemzési mintákon való használatában a Power BI szolgáltatásban
author: mihart
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 01/16/2018
ms.author: mihart
LocalizationGroup: Ask questions of your data
ms.openlocfilehash: c567921b765f03fbaa11f2b98724cea1a1ce1905
ms.sourcegitcommit: 998b79c0dd46d0e5439888b83999945ed1809c94
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
---
# <a name="get-started-with-power-bi-qa"></a>Első lépések a Power BI Q&A-ben
## <a name="use-power-bi-qa-with-the-retail-analysis-sample"></a>A Power BI Q&A használata a kiskereskedelmi elemzési mintával
Ha válaszokat keres az adatokban, néha az a leggyorsabb megoldás, ha természetes nyelven kérdez.  Ebben az útmutatóban két különböző módszert is megtekintünk ugyanannak a vizualizációnak a létrehozására: először felépítjük egy jelentésben, majd kérdést teszünk fel a Q&A-val. Noha a Power BI szolgáltatást fogjuk használni, a folyamat csaknem teljesen azonosan néz ki a Power BI Desktop használatával is.

A bemutatott megoldások elvégzéséhez rendelkeznie kell egy Ön által szerkeszthető jelentéssel, ezért a Power BI-ban elérhető egyik mintát fogjuk használni.

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
[Q&A a Power BI-ban](power-bi-q-and-a.md)

[Megfelelő adatműködés biztosítása a Q&A és a Power BI használatánál](service-prepare-data-for-q-and-a.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

