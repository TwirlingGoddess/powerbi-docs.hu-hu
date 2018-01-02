---
title: "Szűrők és kiemelés a Power BI-jelentésekben"
description: "Szűrők és kiemelés a Power BI-jelentésekben"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/29/2017
ms.author: mihart
ms.openlocfilehash: 57960c3ca46e48f399e0492192c10cba2cfa7ea9
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="about-filters-and-highlighting-in-power-bi-reports"></a>Szűrők és kiemelés a Power BI-jelentésekben
A ***szűrők*** használatával minden olyan adatot eltávolíthat, amelyek az Ön szempontjából lényegtelenek.  A ***kiemelés*** nem egyenlő a szűréssel, mert nem távolítja el az adatokat, hanem kiemeli a látható adatok egy részét; a ki nem emelt adatok halványítva láthatóak maradnak.

A Power BI-ban sokféleképpen szűrheti és kiemelheti a jelentések adatait. Ha az összes erre vonatkozó információt egyetlen cikkbe sűrítenénk, az nehezen áttekinthető lenne, ezért az információt a következőképpen bontottuk fel:

* Bevezetés a szűrők és a kiemelés használatába (a cikk, amelyet most olvas)
* A [szűrők és a kiemelés létrehozásának módjai a saját tulajdonú Szerkesztés nézetben/jelentésekben](power-bi-report-add-filter.md). Ha szerkesztési engedélye van egy jelentéshez, akkor létrehozhatja, módosíthatja és törölheti a szűrőket és a kiemeléseket a jelentésekben.
* A [szűrők és kiemelések használatának módjai az Önnel megosztott jelentésekben vagy a jelentés Olvasó nézetében](service-interact-with-a-report-in-reading-view.md). Korlátozottabb számú dolgot tehet meg, de a Power BI még így is a szűrési és kiemelési lehetőségek széles skáláját kínálja.  
* [A Szerkesztés nézetben rendelkezésre álló szűrési és kiemelési vezérlők részletes bemutatása](power-bi-how-to-report-filter.md) többek között a szűrőtípusok részletes ismertetése (pl. dátum és idő, szám, szöveg), valamint az alapszintű és a speciális beállítások közötti különbségek.
* Most, hogy már tudja, alapértelmezés szerint hogyan működnek a szűrők és a kiemelés, [ismerje, meg hogyan lehet megváltoztatni azt a módot, ahogy az oldal vizualizációi egymást szűrik és kiemelik](service-reports-visual-interactions.md)

> [!TIP]
> Honnan tudja a Power BI, hogyan kapcsolódnak egymáshoz az adatok?  Az alapul szolgáló [adatmodell](https://support.office.com/article/Create-a-Data-Model-in-Excel-87e7a54c-87dc-488e-9410-5c75dbcb0f7b?ui=en-US&rs=en-US&ad=US) különböző táblái és mezői közötti kapcsolatokat használja a jelentésoldal elemei közötti interakció kialakítására.
> 
> 

## <a name="introduction-to-filters-and-highlighting-in-reports-using-the-filters-pane"></a>Bevezetés a jelentésekben a Szűrő ablaktábla használatával történő szűrésbe és kiemelésbe
![](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-reading-view.png)

A szűrés és kiemelés alkalmazható a **Szűrők** ablaktáblán vagy a kiválasztásoknak közvetlenül a jelentésben való elvégzésével (alkalmi, lásd a lap alján). A Szűrők ablaktáblán láthatók a jelentésben használt táblák és mezők és az alkalmazott szűrők, ha vannak. A szűrők **oldalszintű szűrőkre**, **jelentésszintű szűrőkre** és **vizuális szintű szűrőkre** oszthatók.  Vizuális szintű szűrőket csak akkor láthat, ha kiválasztott egy vizualizációt a jelentés vásznán.

> [!TIP]
> Ha a szűrő mellett szerepel az **All** (összes), az azt jelenti, hogy ez a teljes mező szerepel szűrőként.  Például a **Chain(All)** (Lánc(összes)) az alábbi képernyőképen azt jelenti, hogy ez a jelentésoldal az összes áruházláncra vonatkozó adatokat tartalmaz.  Míg a **FiscalYear is 2013 or 2014** jelentésszintű arra utal, hogy a jelentés csak a 2013-as és 2014-es pénzügyi év adatait tartalmazza.
> 
> 

## <a name="filters-in-reading-view-versus-editing-view"></a>Szűrők az Olvasó nézetben és a Szerkesztés nézetben
A jelentéseket kétféle üzemmódban lehet kezelni: [Olvasó nézet](service-interact-with-a-report-in-reading-view.md) és [Szerkesztés nézet](service-interact-with-a-report-in-editing-view.md) használatával.  Az elérhető szűrési funkciók attól függnek, hogy melyik üzemmódban van.

* A Szerkesztés nézetben felvehet jelentés-, oldal- és vizuális szűrőket. Amikor menti a jelentést, a szűrőket is menti vele együtt. A jelentést az Olvasó nézetben szemlélő személyek kezelhetik az Ön által felvett szűrőket, de nem tudják menteni a módosításaikat.
* Olvasó nézetben kezelheti a már a jelentésben lévő oldal- és vizuális szűrőket, de a szűrők módosításait nem tudja menteni.

### <a name="the-filters-pane-in-reading-view"></a>A Szűrők ablaktábla Olvasó nézetben
Ha csak Olvasó nézetben van hozzáférése a jelentéshez, a Szűrők ablaktábla ehhez hasonló:

![](media/power-bi-reports-filters-and-highlighting/power-bi-filter-reading-view.png)

Tehát a jelentés ezen oldalának 6 oldalszintű szűrője és 1 jelentésszintű szűrője van.

Ha tudni szeretné, vannak-e vizuális szintű szűrők, jelöljön ki egy vizualizációt. Az alábbi képen szereplő buborék diagramra 6 szűrőt alkalmaztak.

![](media/power-bi-reports-filters-and-highlighting/power-bi-filter-visual-level.png)

Olvasó nézetben a meglévő szűrők módosításával tárhatja fel az adatokat. Ennek módjáról a [Szűrők kezelése Olvasó nézetben](service-interact-with-a-report-in-reading-view.md) című szakaszban tájékozódhat.

### <a name="the-filters-pane-in-editing-view"></a>Szűrők ablaktábla Szerkesztés nézetben
Ha tulajdonosi engedélye van a jelentéshez, és Szerkesztés nézetben nyitja meg, akkor azt látja, hogy a **Szűrők** csak egyike a rendelkezésre álló szerkesztési ablaktábláknak.

![](media/power-bi-reports-filters-and-highlighting/power-bi-add-filter-editing-view.png)

Mint a fenti Olvasó nézetben, láthatjuk, hogy a jelentésnek ezen az oldalán 6 oldalszintű szűrő és 1 jelentésszintű szűrő van. A buborék diagram kijelölésekor láthatjuk, hogy arra 6 vizuális szintű szűrőt alkalmaztak.

Szerkesztés nézetben azonban sokkal több mindent tehetünk szűrőkkel és kiemeléssel. A fő különbség, hogy felvehetünk új szűrőket. Ennek módjáról és sok egyébről a [Szűrő hozzáadása jelentéshez](power-bi-report-add-filter.md) című cikkben olvashat.

## <a name="ad-hoc-filterting-and-highlighting"></a>Alkalmi szűrők és kiemelés
Jelöljön ki egy mezőt a jelentés vásznon az oldal többi részének szűréséhez és kiemeléséhez. Jelöljön ki egy üres helyet ugyanabban a vizualizációban az eltávolításához. A szűrésnek és kiemelésnek ez a módja nem lesz mentve a jelentéssel, de szórakoztató módja az adathatások feltárásának. Az ilyen típusú keresztszűrés és keresztkiemelés finombeállításához lásd: [Vizuális interakciók](service-reports-visual-interactions.md)

![](media/power-bi-reports-filters-and-highlighting/power-bi-adhoc-filter.gif)

## <a name="next-steps"></a>További lépések
[Interakció a szűrőkkel és kiemeléssel (Olvasó nézetben)](service-interact-with-a-report-in-reading-view.md)

[Szűrő hozzáadása jelentéshez (Szerkesztés nézetben)](power-bi-report-add-filter.md)

[Ismerkedés a jelentésszűrőkkel](power-bi-how-to-report-filter.md)

[A jelentésvizualizációk keresztszűrésének és -kiemelésének módosítása](service-reports-visual-interactions.md)

További információ a [Power BI-jelentésekről](service-reports.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

