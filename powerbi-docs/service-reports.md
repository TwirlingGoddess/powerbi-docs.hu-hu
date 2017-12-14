---
title: "Jelentések a Power BI-ban"
description: "Jelentések a Power BI-ban"
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
ms.date: 10/27/2017
ms.author: mihart
ms.openlocfilehash: d974fbac281fc8f1d74553d1342f7056fa8d7b03
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="reports-in-power-bi"></a>Jelentések a Power BI-ban
## <a name="what-is-a-power-bi-report"></a>Mi a Power BI-jelentés?
A Power BI-***jelentés*** többféle nézőpontból jeleníti meg az adathalmazokat, különböző, az adott adathalmazból származó eredményeket és meglátásokat bemutató vizualizációkkal.  Egy jelentés állhat egyetlen vizualizációból vagy vizualizációkkal megtöltött lapokból. Feladatkörétől függően Ön lehet a jelentések *létrehozója* és/vagy egy azokat *feldolgozó* vagy felhasználó személy.

![](media/service-reports/reportview.png)

Ez a jelentés 3 lapot tartalmaz, és jelenleg az „Üzleti értékesítések áttekintése” lapot látjuk. Ez a lap 6 különböző vizualizációt és egy lapcímet tartalmaz. A vizualizációk *rögzíthetők* az irányítópultokra, és a rögzített vizualizációk választásakor megnyílik a jelentés, amelyből a vizualizáció származik.

Ha először használja a Power BI-t, sok mindent megtudhat, ha elolvassa a [Power BI alapvető fogalmai](service-basic-concepts.md) című témakört.

A jelentések a Power BI szolgáltatásban és a Power BI Desktop alkalmazásban érhetők el. A jelentések használatának élménye a két környezet esetében csaknem azonos. Mobileszközről azonban nem tud jelentést létrehozni, hanem csak [megtekintheti, megoszthatja és jegyzetekkel láthatja el](mobile-reports-in-the-mobile-apps.md) őket.

## <a name="advantages-of-reports"></a>A jelentések előnyei
A jelentések egyetlen adathalmazon alapulnak. A jelentésben lévő vizualizációk egy-egy információmorzsát képviselnek. A vizualizációk nem statikusak: hozzáadhat és eltávolíthat adatokat, módosíthatja a vizualizációtípusokat, és az elemzésekhez és a válaszok kereséséhez az adatok mélyebb szintjére lehatolva szűrőket és szeletelőket alkalmazhat. A jelentések rendkívül interaktívak és nagymértékben testre szabhatók (éppen úgy, ahogyan az irányítópultok – sőt, még inkább), a vizualizációk pedig frissülnek az alapjukul szolgáló adatok változásakor.

## <a name="dashboards-versus-reports"></a>Az irányítópultok és a jelentések különbségei
Az [irányítópultokat](service-dashboards.md) sokan összetévesztik a jelentésekkel, mert ezek is vizualizációkat tartalmazó vásznak. Vannak azonban lényeges különbségek a két elem között.  

| **Képesség** | **Irányítópultok** | **Jelentések** |
| --- | --- | --- |
| Lapok |Egy lap |Egy vagy több lap |
| Adatforrások |Egy vagy több jelentés és egy vagy több adatkészlet irányítópultonként |Egyetlen adatkészlet jelentésenként |
| Elérhető a Power BI Desktop alkalmazásban |Nem |Igen, hozhat létre és tekinthet meg jelentéseket a Desktop alkalmazásban |
| Rögzítés |Rögzítheti a már létező vizualizációkat (csempéket), de csak az aktuális irányítópultról a többi irányítópultra |Rögzíthet vizualizációkat (csempékként) bármelyik irányítópultra. Rögzíthet teljes jelentéslapokat bármelyik irányítópultra. |
| Feliratkozás |Nem lehet feliratkozni irányítópultra |Fel lehet iratkozni jelentéslapokra |
| Szűrés |Nem lehet szűrni és szeletelni |Számos szűrési, kiemelési és szeletelési lehetőség elérhető |
| Riasztás beállítása |Hozhat létre riasztásokat, melyeket e-mailben küld ki a rendszer bizonyos feltételek teljesülésekor |Nem |
| Kiemelés |Beállíthatja az egyik irányítópultot „kiemelt” irányítópultként |Nem hozható létre kiemelt jelentés |
| Természetes nyelvi kérdések |Elérhető az irányítópultokról |Nem érhető el a jelentésekből |
| Vizualizáció típusának módosítása |Nem. Sőt, ha a jelentéstulajdonos módosítja a jelentésben egy vizualizáció típusát, az irányítópultra rögzített vizualizáció nem frissül. |Igen |
| Mögöttes adatkészlettáblák és -mezők megtekintése |Nem. Exportálhatja az adatokat, de nem láthatja a táblákat és a mezőket közvetlenül az irányítópulton. |Igen. Megtekintheti a mögöttes adatkészlettáblákat és -mezőket. |
| Vizualizációk létrehozása |Korlátozott. Csak widgetet tud hozzáadni az irányítópultokhoz a „Csempe hozzáadása” lehetőséggel |Hozhat létre számos típusú vizualizációt, adhat hozzá egyéni vizualizációkat, szerkesztheti a vizualizációkat, és más műveleteket is végezhet szerkesztési jogosultság esetén |
| Testreszabás |Végezhet műveleteket a vizualizációkkal (csempékkel), ideértve például a következőket: áthelyezés, átrendezés, átméretezés, hivatkozások hozzáadása, átnevezés, törlés és teljes képernyős megjelenítés. De maguk az adatok és a vizualizációk csak olvashatók. |Olvasó nézetben többek között a következő műveletek érhetők el: közzététel, beágyazás, szűrés, exportálás, letöltés .pbix-fájlként, kapcsolódó tartalom megtekintése, QR-kódok generálása és elemzés Excelben.  Szerkesztő nézetben ugyanezek mellett rengeteg más művelet is elérhető. |

## <a name="report-creators-and-report-consumers"></a>Jelentések ***létrehozói*** és ***felhasználói***
A szerepkörétől függően Ön lehet olyan személy, aki jelentéseket hoz létre saját használatra vagy a munkatársakkal való megosztáshoz. Ez esetben a jelentések létrehozásáról és megosztásáról kell ismereteket szereznie. Vagy lehet olyan személy is, aki jelentéseket kap másoktól. Ez esetben azt kell tudnia, hogy hogyan értelmezheti és használhatja a jelentéseket.

A szerepkörének megfelelő alábbi témakörök kiváló kiindulási pontot nyújtanak.

### <a name="if-you-will-be-creating-and-sharing-reports"></a>Jelentések létrehozásához és megosztásához
* Kezdje a [Power BI szolgáltatás áttekintésével](service-basic-concepts.md), melyből megtudhatja, hol találhatja meg a jelentéseket és a jelentéseszközöket.
* Ismerkedjen meg a [jelentésszerkesztővel](service-the-report-editor-take-a-tour.md).
* Tudja meg, [hogyan hozhat létre jelentést egy adatkészletből](service-report-create-new.md).
* Ismerkedjen meg a [vizualizációk, lapok és jelentésszintű szűrők használatával](power-bi-how-to-report-filter.md).
* Fedezze fel, milyen különféle módokon [oszthatja meg a jelentéseket a munkatársaival](service-share-dashboards.md).

### <a name="if-you-will-be-receiving-and-consuming-reports"></a>Jelentések fogadásához és felhasználásához
* Kezdje a [Power BI szolgáltatás áttekintésével](service-basic-concepts.md), melyből megtudhatja, hol találhatja meg a jelentéseket és a jelentéseszközöket.
* Ismerje meg, hogyan tud [megnyitni egy jelentést](service-report-open-in-reading-view.md), és fedezze fel az [Olvasó nézetben](service-dashboard-tiles.md) elérhető műveleteket.
* Gyakorolja a jelentések használatát az egyik [mintánk](sample-tutorial-connect-to-the-samples.md) segítségével.  
* Nincs már szüksége egy jelentésre? Akkor [törölheti a jelentést](service-delete.md).
* Ha szeretné megtudni, milyen adatkészletet használ egy jelentés, és mely irányítópultok tartalmaznak rögzített csempéket a jelentésből, [tekintse meg a kapcsolódó tartalmat](service-related-content.md).

> [!TIP]
> Ha nem találta meg itt, amit keres, a bal oldali tartalomjegyzékben elérheti a *jelentések* témaköreinek teljes listáját.
> 
> 

## <a name="next-steps"></a>Következő lépések
[Első lépések a Power BI használatával](service-get-started.md) 

[Power BI – alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

