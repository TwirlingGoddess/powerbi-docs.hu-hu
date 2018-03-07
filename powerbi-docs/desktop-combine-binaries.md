---
title: "Bináris fájlok egyesítése a Power BI Desktopban"
description: "A bináris adatforrások egyszerűen egyesíthetők a Power BI Desktopban."
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
ms.date: 12/06/2017
ms.author: davidi
LocalizationGroup: Transform and shape data
ms.openlocfilehash: 395562dfecba4657ffa906494f81532febb6a11f
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="combine-binaries-in-power-bi-desktop"></a>Bináris fájlok egyesítése a Power BI Desktopban
Az adatok a **Power BI Desktopba** való importálásának egy igen hatékony módja, ha az azonos sémájú fájlokat egyetlen logikai táblában egyesíti. A **Power BI Desktop** 2016 novemberi (és azt követő) kiadásaiban ez a kényelmes és népszerű megközelítés még kényelmesebbé és szélesebb körben alkalmazhatóvá vált, amint azt ez a cikk is ismerteti.

Az egyazon mappában lévő bináris fájlok ötvözéséhez válassza az **Adatok lekérése > Fájl > Mappa** lehetőséget.

![](media/desktop-combine-binaries/combine-binaries_1.png)

## <a name="previous-combine-binaries-behavior"></a>A bináris fájlok egyesítésének korábbi működése
A **Power BI Desktop** 2016 novemberi kiadását megelőzően a különböző fájltípusok egyesíthetők voltak a **bináris fájlok egyesítése** átalakítással, azonban volt néhány korlát:

* A rendszer az egyes fájlokat az egyetlen táblába való egyesítésüket megelőzően nem alakította át. Így sokszor a fájlok egyesítését követően a szerkesztési folyamat keretében, a sorok szűrésével ki kellett szűrni a *fejlécértékeket*.
* A **Bináris fájlok egyesítése** átalakítás kizárólag *szöveges* vagy *CSV*-fájlokon volt használható, más támogatott fájlformátumokkal, például Excel-munkafüzetekkel, JSON-fájlokkal és egyéb fájlokkal nem működött.

Az ügyfelek kérésére a **bináris fájlok egyesítése** műveletet továbbfejlesztettük, így az átalakítás most intuitívabb módon működik.

## <a name="current-combine-binaries-behavior"></a>A bináris fájlok egyesítésének jelenlegi működése
A **Power BI Desktop** mostantól hatékonyabban végzi a **bináris fájlok egyesítését**. A **bináris fájlok egyesítése** a **Lekérdezésszerkesztő** menüszalagján a **Kezdőlapról** vagy magából az oszlopból indítható.

![](media/desktop-combine-binaries/combine-binaries_2a.png)

A **bináris fájlok egyesítése** átalakítás mostantól az alábbiak szerint működik:

* A **bináris fájlok egyesítése** átalakítás kielemzi az egyes bemeneti fájlokat, és meghatározza a megfelelő fájlformátumot (például: *szövegfájl*, *Excel-munkafüzet* vagy *JSON*-fájl).
* Az átalakítással kiválaszthat egy adott objektumot az első fájlból, például egy *Excel-munkafüzetből*, amelyet ki szeretne nyerni.
  
  ![](media/desktop-combine-binaries/combine-binaries_3.png)
* A **bináris fájlok egyesítése** ezután automatikusan végrehajtja a következőket:
  
  * Létrehoz egy példalekérdezést, amely végrehajtja a kinyeréshez szükséges lépéseket egyetlen fájlban.
  * Létrehoz egy *függvénylekérdezést*, amely felparaméterezi a fájl/bináris fájl bemenetet a *példalekérdezéshez*. A példalekérdezés és a függvénylekérdezés össze van kapcsolva, így a példalekérdezésen végrehajtott módosítások a függvénylekérdezésben is megjelennek.
  * Alkalmazza a *függvénylekérdezést* az eredeti lekérdezésre a bemeneti bináris fájlokkal (például a *Mappa* lekérdezést), azaz a bináris fájlbemenetek függvénylekérdezéseit mindegyik soron alkalmazza, majd az így kinyert adatokat felsőszintű oszlopokká bontja ki.
    
    ![](media/desktop-combine-binaries/combine-binaries_4.png)

A **bináris fájlok egyesítésének** új működése révén könnyedén egyesítheti az egy adott mappában lévő összes bináris fájlt, amennyiben egyazon fájltípussal és szerkezettel (azaz ugyanazokkal az oszlopokkal) rendelkeznek.

Emellett további átalakítási és kinyerési műveleteket is könnyen alkalmazhat az automatikusan létrehozott *példalekérdezés* módosításával anélkül, hogy módosítania kellene a *függvénylekérdezés* lépéseit, vagy újakat kellene létrehoznia, a *példalekérdezés* változásai ugyanis automatikusan megjelennek a csatolt *függvénylekérdezésben*.

## <a name="next-steps"></a>Következő lépések
A Power BI Desktop használatával számos adatforráshoz csatlakozhat. Az adatforrásokkal kapcsolatos információkért lásd az alábbi forrásanyagokat:

* [Első lépések a Power BI Desktopban](desktop-getting-started.md)
* [Adatforrások a Power BI Desktopban](desktop-data-sources.md)
* [Adatok formázása és kombinálása a Power BI Desktoppal](desktop-shape-and-combine-data.md)
* [Csatlakozás CSV-fájlokhoz a Power BI Desktopban](desktop-connect-csv.md)   
* [Adatok közvetlen bevitele a Power BI Desktopba](desktop-enter-data-directly-into-desktop.md)   

