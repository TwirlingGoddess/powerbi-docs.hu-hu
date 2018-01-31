---
title: DirectQuery az SAP HANA-hoz a Power BI Desktopban
description: "Megfontolandó szempontok a DirectQuery SAP HANA-val való használatakor"
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 01/24/2018
ms.author: davidi
ms.openlocfilehash: 2b2e59371c96928a2b7c6b23bd393a80ecc3041a
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/25/2018
---
# <a name="directquery-and-sap-hana"></a>DirectQuery és SAP HANA
Az **SAP HANA**-adatforrásokhoz közvetlenül kapcsolódhat a **DirectQuery** használatával.

Az **SAP HANA** használata esetén fontos, hogy tisztában legyen a kapcsolatok kezelésének bizonyos szempontjaival, hogy biztosíthassa a következőket:

* A várt eredmények jelennek meg, amikor az SAP HANA-nézet nem additív mértékeket tartalmaz (például különböző számadatokat, vagy átlagértékeket egyszerű összegek helyett)
* A kapott lekérdezések hatékonyak

Érdemes rászánni egy kis időt a relációs forrás, például az **SQL Server** működésének tisztázására, amikor az **Adatok lekérése** utasításban vagy a **Lekérdezésszerkesztőben** meghatározott lekérdezés összesítést végez. A következő példában egy **Lekérdezésszerkesztőben** meghatározott lekérdezés **termékazonosító** szerint rendezve adja vissza az átlagárat.

![](media/desktop-directquery-sap-hana/directquery-sap-hana_01.png)

Ha a Power BI-ba importálja az adatokat (a DirectQuery helyett), az az alábbiakat eredményezi:

* Az adatok importálása a **Lekérdezésszerkesztőben** létrehozott lekérdezés által meghatározott összesítési szinten történik. Például átlagár termékek szerint rendezve. Ennek eredményeként egy *ProductID* (termékazonosító) és egy *AveragePrice* (átlagár) oszlopokat tartalmazó tábla jön létre, amely vizualizációkban használható.
* Egy vizualizáción belül minden további összesítés (pl. *Sum*, *Average*, *Min* stb.) az importált adatok felhasználásával történik.  Ha például belefoglalja az *AveragePrice* (átlagár) értéket egy vizualizációba, akkor a rendszer alapértelmezés szerint a *Sum* (összeg) összesítést fogja használni, és az *AveragePrice* összegét fogja visszaadni minden *ProductID*-hez (termékazonosítóhoz) – amely ebben az esetben 13,67. Ugyanez vonatkozik a vizualizációban használt minden alternatív összegzési függvényre (pl. *Min*, *Average* stb.). Az *Average* (átlag) függvény például az *AveragePrice* esetében a 6,66, a 4 és a 3 átlagát fogja visszaadni, ami 4,56, *nem* pedig az alapul szolgáló tábla 6 rekordjában szereplő *Price* (ár) értékek átlagát, ami 5.17.

Ha importálás helyett a **DirectQueryt** használja, akkor is ugyanaz a szemantika, és az eredmények is pontosan ugyanazok lesznek:

* Ugyanazon lekérdezés esetén logikusan ugyanazok az adatok kerülnek a jelentéskészítési rétegbe, még ha az adatok nem is lettek importálva.
* Egy vizualizáción belül minden további összesítés (*Sum*, *Average*, *Min* stb.) a lekérdezésből származó logikai tábla felhasználásával történik. Az *Average* függvény az *AveragePrice* esetében ekkor is ugyanazt az értéket (4,56) adja vissza.

Most pedig vegyük az **SAP HANA** példáját. A Power BI az SAP HANA *Analitikus nézetével* és *Számítási nézetével* is működik, és mindkettő tartalmazhat mértékeket. Az SAP HANA jelenlegi módszere viszont szintén az előzőleg bemutatott alapelveket használja: az **Adatok lekérése** utasításban vagy a **Lekérdezésszerkesztőben** meghatározott lekérdezés határozza meg az elérhető adatokat, és a vizualizáción belüli minden további összesítéshez azokat az adatokat használja fel. Ez az importálás és a DirectQuery használata esetén is igaz.

Azonban a HANA természetéből adódóan a kezdeti **Adatok lekérése** párbeszédablakban vagy a **Lekérdezésszerkesztőben** meghatározott lekérdezés mindig összesítő lekérdezés, és általában olyan mértékeket is tartalmaz, amelyekben a tényleges lekérdezést a HANA-nézet határozza meg.

Az SQL Serverből vett fenti példa megfelelője, hogy adott egy **ID** (azonosító), **ProductID** (termékazonosító) és **DepotID** (raktár-azonosító) adatokból álló HANA-nézet, amely többek között az **AveragePrice** (átlagérték) mértéket is tartalmazza (a nézetben **Average of Price** (ár átlaga) néven van meghatározva).

![](media/desktop-directquery-sap-hana/directquery-sap-hana_02.png)

Ha az **Adatok lekérése** utasítás használatakor kiválasztotta a **ProductID** és az **AveragePrice** mértékeket, akkor az határozza meg a lekérdezést a nézetben, és ezeket az összesített adatokat kéri le (a fenti példában az egyszerűség kedvéért egy ál-SQL szerepel, amely nem felel meg tökéletesen a HANA SQL szintaxisának). Ekkor a vizualizáción belül meghatározott minden további összesítés tovább összesíti az ilyen lekérdezések eredményét. Az **SQL Server** esetében fentebb leírtakhoz hasonlóan ez szintén érvényes az importálásra és a DirectQuery használatára is. Vegye figyelembe, hogy a DirectQuery esetében a rendszer az **Adatok lekérése** utasításból vagy a **Lekérdezésszerkesztőből** származó lekérdezést a HANA-hoz küldött egyetlen lekérdezés részkiválasztásaként használja, így valójában nem történik meg az összes adat beolvasása a további összesítés előtt.

Ez pedig a következő megfontolandó szempontokat veti fel a DirectQuery HANA-val való használatakor:

* A vizualizációkban elvégzett minden további összesítésre oda kell figyelni, amikor a HANA-beli mérték nem additív (például nem egyszerű *Sum*, *Min* vagy *Max*).
* Az **Adatok lekérése** utasításban vagy a **Lekérdezésszerkesztőben** csak a szükséges oszlopokat kell kiválasztani a szükséges adatok lekéréséhez, hiszen az eredmény lekérdezés lesz, amelynek a HANA-hoz továbbítható ésszerű lekérdezésnek kell lennie. Például ha több tucat oszlopot választott ki azzal az elgondolással, hogy későbbi vizualizációkban még szüksége lehet rájuk, akkor még egy DirectQuery használatával indított egyszerű lekérdezés esetén is a részkiválasztásban használt összesítő lekérdezés tartalmazni fogja azt a több tucat oszlopot, így az általános teljesítmény igen gyenge lesz.

Lássunk erre egy példát. Az alábbi példában öt oszlop van kiválasztva (a CalendarQuarter, a Color, a LastName, a ProductLine és a SalesOrderNumber) az **Adatok lekérése** párbeszédablakban, illetve az OrderQuantity mérték, ez pedig azt jelenti, hogy később egy a Min OrderQuantity (Minimális rendelési mennyiség) mértéket tartalmazó egyszerű vizualizációt kiválasztva az eredmény a következő SQL-lekérdezést küldi a HANA-hoz. Az árnyékolt szakasz a részkiválasztást jelöli, amely az **Adatok lekérése** utasításból /  a **Lekérdezésszerkesztőből** származó lekérdezést tartalmazza. Ha ez a részkiválasztás nagyon magas számosságú eredményt ad, az valószínűleg gyenge HANA-teljesítményt is eredményez.

![](media/desktop-directquery-sap-hana/directquery-sap-hana_03.png)

Ennek következtében ajánlott az **Adatok lekérése** utasításban vagy a **Lekérdezésszerkesztőben** kiválasztott elemeket csak a szükséges elemekre korlátozni úgy, hogy közben továbbra is ésszerű HANA-lekérdezést eredményezzenek.

### <a name="next-steps"></a>Következő lépések
Ha többet szeretne megtudni a DirectQueryről, tekintse át a következő forrásanyagokat:

* [A DirectQuery használata a Power BI-ban](desktop-directquery-about.md)
* [A DirectQuery által támogatott adatforrások](desktop-directquery-data-sources.md)
* [A DirectQuery és az SAP BW](desktop-directquery-sap-bw.md)
* [Helyszíni adatátjáró](service-gateway-onprem.md)

