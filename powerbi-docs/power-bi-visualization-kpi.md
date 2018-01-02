---
title: "KPI-vizualizációk (Oktatóanyag)"
description: "KPI létrehozása a Power BI-ban"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: xmja6EpqaO0
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/09/2017
ms.author: mihart
ms.openlocfilehash: 23b322c9fbc4c203a5b20aa45bb41c2cb6cb7f0f
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="kpi-visuals-tutorial"></a>KPI-vizualizációk (Oktatóanyag)
A fő teljesítménymutató (KPI) olyan vizuális jel, amely egy mérhető cél terén elért előrehaladás mértékét jelzi. A KPI-kal kapcsolatos további információkért lásd: [Microsoft Developer Network](https://msdn.microsoft.com/library/hh272050).

## <a name="when-to-use-a-kpi"></a>Mikor érdemes KPI-t használni?
A KPI remek választás:

* az előrehaladás mérésére (miben járok előrébb vagy miben maradtam le?)
* egy céltól való távolság mérésére (mennyivel járok előrébb vagy milyen messze vagyok tőle?)   

## <a name="kpi-visual-requirements"></a>KPI-vizualizációk követelményei
A fő teljesítménymutató (KPI) specifikus mérésen alapul, és úgy van kialakítva, hogy segítsen egy mutatószám jelenlegi értékének és állapotának egy meghatározott célhoz viszonyított értékelésében. Ezért a KPI-vizualizációhoz szükség van egy *alapmértékre*, amely egy értéket és egy *célmértéket* vagy -értéket ad eredményként, valamint egy küszöbértékre vagy célra.

> [!NOTE]
> Jelenleg a KPI-adatkészletnek tartalmaznia kell egy KPI célértékeit. Ha az adatkészlet nem tartalmaz ilyet, létrehozhat célokat, ha hozzáad egy célokat tartalmazó Excel-munkalapot az adatmodellhez vagy egy PBIX-fájlt.
> 
> 

## <a name="how-to-create-a-kpi"></a>KPI létrehozása
A lépések elvégzése érdekében jelentkezzen be a Power BI szolgáltatásba, és válassza az **Adatok lekérése > Minták > Kiskereskedelmi elemzési minta** lehetőséget. Létrehozunk egy KPI-t, amely egy értékesítési cél irányába tett előrehaladást méri.

Másik lehetőségként tekintse meg a videót, amelyben bemutatjuk, hogyan hozhat létre egyetlen mutatószámos vizualizációkat: mérőműszereket, kártyákat és KPI-ket.

<iframe width="560" height="315" src="https://www.youtube.com/embed/xmja6EpqaO0?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

1. Válassza a **Sales > Total Units This Year** (Értékesítés > Idei összes egység) mezőt.  Ez lesz a mutató.
2. Adjon hozzá **Time > Month** (Időpont > Hónap) értékeket.  Ez jelzi a trendet.
3. FONTOS: A **Month** mező szerint rendezze a diagramot. Miután átalakítja a vizualizációt KPI-vé, nincs lehetőség rendezésre.
4. Alakítsa át a vizualizációt KPI-vé a KPI ikon kiválasztásával a Vizualizációk panelen.
   
    ![](media/power-bi-visualization-kpi/power-bi-kpi-icon.png)
5. Adjon meg egy célt. Adja meg a múlt évi értékesítést célként. Húzza a **Total Units Last Year** (Tavalyi összes egység) mezőt a **Célkitűzések** mezőbe.
   
    ![](media/power-bi-visualization-kpi/power-bi-kpi.png)
6. Ha szeretné, formázza a KPI-t a festőhenger ikon kiválasztásával, amely megnyitja Formátum panelt.
   
   * **Mutató** – szabályozza a mutatószám megjelenítési egységeit és tizedesjegyeit.
   * **Trendtengely** – amikor **Be** értékre van állítva, a trendtengely a KPI-vizualizáció háttereként jelenik meg.  
   * **Célok** – amikor **Be** értékre van állítva, a vizualizáció megjeleníti a célt és a távolságot a céltól százalékban.
   * **Állapot** – néhány KPI magasabb érték esetén *jobb*, néhány pedig alacsonyabb érték esetén *jobb*. Például ilyen a bevétel, illetve a várakozási idő. Általában a bevételek magasabb értékét jobbnak, míg a várakozási idő magasabb értékét többnyire rosszabbnak tartjuk. Ezzel a kapcsolóval meghatározhatja a KPI viselkedését. Az állapot kiválasztásának alapértelmezett értéke **a magasabb jobb**.
7. Ha már olyan a KPI, amilyennek szeretné, [rögzítse az irányítópultra](service-dashboard-pin-tile-from-report.md).

A KPI-k a mobileszközein is elérhetők, így mindig összhangban lehet vállalata szívverésével

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
* Amennyiben a KPI-je nem hasonlít a fentire, lehetséges, hogy hónapok szerint sorba kell rendeznie. Mivel a KPI-knél nem érhető el a rendezés lehetősége, a hónapok szerinti rendezést még *azelőtt* kell elvégeznie, hogy átalakítja a vizualizációt KPI-vé.

## <a name="next-steps"></a>Következő lépések
[Power BI-jelentések](service-reports.md)

[Vizualizációk a Power BI-jelentésekben](power-bi-report-visualizations.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Forduljon a Power BI közösségéhez](http://community.powerbi.com/)

