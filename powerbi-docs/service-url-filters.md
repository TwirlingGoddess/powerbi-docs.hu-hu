---
title: Power BI-jelentés paramétereinek megadása az URL-cím használatával
description: A jelentések szűrhetők az URL-cím lekérdezési sztringjének paramétereivel, akár egynél több mezőre is.
author: mihart
manager: kfile
ms.reviewer: ''
featuredvideoid: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 05/18/2018
ms.author: mihart
LocalizationGroup: Reports
ms.openlocfilehash: aeaea6d14cf8f4fd62fbbf5098e68429fe40b96a
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34471939"
---
# <a name="filter-a-report-using-query-string-parameters-in-the-url"></a>Jelentés szűrése lekérdezésisztring-paraméterek URL-címben való használatával
A Power BI szolgáltatásban megnyitott jelentések minden egyes oldalának saját egyedi URL-címe van. Az adott jelentésoldal a jelentésvászon Szűrők paneljének használatával szűrhető.  A jelentés úgy is szűrhető, hogy lekérdezésisztring-paramétereket ad hozzá a jelentés URL-címéhez. Tegyük fel, hogy egy jelentést meg szeretne mutatni a munkatársainak, és előre szűrni szeretné azt a számukra. Ennek egyik módja, hogy a jelentés alapértelmezett URL-címéből kiindulva hozzáfűzi ahhoz a szűrési paramétereket, majd elküldi nekik a teljes URL-címet.

![Power BI-jelentés a szolgáltatásban](media/service-url-filters/power-bi-report2.png)

<iframe width="640" height="360" src="https://www.youtube.com/embed/WQFtN8nvM4A?list=PLv2BtOtLblH3YE_Ycas5B1GtcoFfJXavO&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="query-string-parameter-syntax-for-filtering"></a>Lekérdezésisztring-paraméterek szintaxisa szűréshez
A szintaxis nagyon egyszerű – kezdje a jelentés URL-címével, adjon hozzá egy kérdőjelet, majd a szűrési szintaxist.

URL-cím?filter=***Tábla***/***Mező*** eq '***érték***'

![URL-cím szűrővel](media/service-url-filters/power-bi-filter-urls7b.png)

* A **Tábla** és a **Mező** név megkülönbözteti a kis- és nagybetűket, az **érték** viszont nem.
* A jelentésnézetben rejtett mezők is szűrhetők.
* Az **értéket** aposztrófok között kell megadni.
* A fájltípusnak szám vagy sztring típusúnak kell lennie
* A tábla és a mező neve nem tartalmazhat szóközöket.

Ha egyelőre nem minden világos, akkor olvasson tovább, és bővebb kifejtést is találhat.  

## <a name="filter-on-a-field"></a>Szűrés egy mező alapján
Tegyük fel például, hogy a jelentés URL-címe a következő.

![URL indítása](media/service-url-filters/power-bi-filter-urls6.png)

A térkép-vizualizáción (fent) látható, hogy üzleteink vannak Észak-Karolinában.

>[!NOTE]
>Ez a példa a [Kiskereskedelmi elemzési mintán](sample-datasets.md) alapszik.
> 

Ha úgy szeretné szűrni a jelentést, hogy csak az Észak-Karolinában („NC”) található üzletek adatait jelenítse meg, akkor fűzze hozzá az URL-címhez a következőt;

?filter=Store/Territory eq 'NC'

![URL-cím szűrővel](media/service-url-filters/power-bi-filter-urls7.png)

>[!NOTE]
>Az *NC* (North Carolina, Észak-Karolina) érték a **Store** (Üzlet) tábla **Territory** (Terület) mezőjében található meg.
> 
> 

A jelentés szűrve lett Észak-Karolinára, és a jelentés oldalán található összes vizualizáció csak Észak-Karolina adatait jeleníti meg.

![](media/service-url-filters/power-bi-report4.png)

## <a name="filter-on-multiple-fields"></a>Szűrés több mező alapján
Ha további paramétereket fűz az URL-címhez, több mező alapján is végezhet szűrést. Térjünk vissza az eredeti szűrési paraméterhez.

```
?filter=Store/Territory eq 'NC'
```

További mezők alapján úgy szűrhet, hogy az `and` kulcsszót és egy újabb mezőt ad meg a fentinek megfelelő formátumban. Íme egy példa.

```
?filter=Store/Territory eq 'NC' and Store/Chain eq 'Fashions Direct'
```

<iframe width="640" height="360" src="https://www.youtube.com/embed/0sDGKxOaC8w?showinfo=0" frameborder="0" allowfullscreen></iframe>


### <a name="using-dax-to-filter-on-multiple-values"></a>Szűrés több értékre a DAX használatával
A szűrés egy másik módja, ha létrehoz egy számított oszlopot, amely két mezőt egyetlen értékké fűz össze. Ezt követően már szűrhet erre az értékre.

Legyen a két mező például a Territory (Terület) és a Chain (Üzletlánc). [Hozzon létre egy új számított oszlopot](desktop-tutorial-create-calculated-columns.md) (Mezőt) a Power BI Desktopban, TerritoryChain (TerületÜzletlánc) néven. Ne feledje, hogy a **Mező** neve nem tartalmazhat szóközöket. Az oszlop DAX-képlete a következő.

TerritoryChain = [Territory] & " - " & [Chain]

Tegye közzé a jelentést a Power BI szolgáltatásban, majd az URL-cím lekérdezési sztringjével szűrje azt úgy, hogy csak az Észak-Karolinában található Lindseys üzletek adatait jelenítse meg.

    https://app.powerbi.com/groups/me/reports/8d6e300b-696f-498e-b611-41ae03366851/ReportSection3?filter=Store/TerritoryChain eq 'NC–Lindseys'

## <a name="pin-a-tile-from-a-filtered-report"></a>Szűrt jelentésből származó csempe rögzítése
Miután lekérdezésisztring-paraméterek használatával szűrte a jelentést, abból származó vizualizációkat rögzíthet az irányítópulton. Az irányítópulton lévő csempe a szűrt adatokat jeleníti meg, a csempe kiválasztásakor pedig megnyílik a létrehozásához használt jelentés.  Az URL-címmel alkalmazott szűrés azonban nem lesz a jelentéssel együtt mentve, és az irányítópult csempéjének kiválasztása után a jelentés szűretlen állapotban nyílik meg.  Ez azzal jár, hogy az irányítópult csempéjén látható adatok nem egyeznek meg azokkal, amelyek a jelentésben lévő vizualizáción megjelennek.

Bizonyos esetekben ez hasznos is lehet, ha különböző eredményeket szeretne látni: szűrve az irányítópulton és szűrés nélkül a jelentésben.

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
Lekérdezésisztring-paraméterek használatakor néhány szemponttal érdemes tisztában lenni.

* A Power BI jelentéskészítő kiszolgálón [adhat át jelentésparamétereket](https://docs.microsoft.com/sql/reporting-services/pass-a-report-parameter-within-a-url?view=sql-server-2017.md) úgy, hogy belefoglalja őket a jelentés URL-címébe. Ezek az URL-paraméterek nincsenek előtaggal ellátva, mert a rendszer közvetlenül átadja őket a jelentésfeldolgozó motornak. 
* A lekérdezési sztringgel végzett szűrés [webes közzététellel](service-publish-to-web.md) és Power BI Embedded használatával nem működik.   
* A fájltípusnak szám vagy sztring típusúnak kell lennie.
* A tábla és a mező neve nem tartalmazhat szóközöket.

## <a name="next-steps"></a>Következő lépések
[Vizualizáció rögzítése az irányítópulton](service-dashboard-pin-tile-from-report.md)  
[Próbálja ki – ingyenes!](https://powerbi.com/)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

