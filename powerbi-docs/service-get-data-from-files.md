---
title: "Adatok lekérdezése fájlból"
description: "Megtudhatja, hogyan olvashat be adatokat Excel-, Power BI Desktop- és CSV-fájlokból a Power BI-ba."
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: complete
qualitydate: 04/01/2016
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: efce7d59df544a067a57db2402c6441c296b569f
ms.sourcegitcommit: d91436de68a0e833ecff18d976de9d9431bc4121
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/06/2017
---
# <a name="get-data-from-files"></a>Adatok lekérdezése fájlból
![](media/service-get-data-from-files/file_icons.png)

A Power BI-ban akkor kapcsolódhat adatokhoz vagy jelentésekhez, és akkor importálhatja őket, ha az alábbi három fájltípusból származnak.

* Microsoft Excel (.xlsx vagy .xlsm)
* Power BI Desktop (.pbix)
* Vesszővel tagolt adatfájl (.csv)

## <a name="what-does-get-data-from-a-file-really-mean"></a>Mit jelent pontosan az adatok fájlból történő beolvasása?
A Power BI-ban az adatok adatkészletekből származnak. Az adatkészleteket azonban meg kell tölteni adatokkal. Ebben a cikkben azzal foglalkozunk, hogy miképpen szerezhet adatokat fájlokból.

Az adatkészletek és az adatokkal történő feltöltésük megértéséhez vegyünk alapul egy autót. Üljön be az autóba, és nézzen a műszerfalra. Ez nagyjából olyan, mintha a számítógép előtt ülne, és egy Power BI-irányítópultot nézne. A műszerfal az autó működésének minden mutatóját megjeleníti: a motor fordulatszámát, a hőmérsékletet, a sebességi fokozatot, a sebességet stb.

A Power BI-ban az adatkészletek jelentik az autó motorját. Az adatkészletekből származnak az adatok, a metrikák és minden, ami megjelenik a Power BI-irányítópulton. A motornak, azaz az adatkészletnek, természetesen üzemanyagra van szüksége, és a Power BI-ban ez nem más, mint az adat. Az autó üzemanyagtartályban tárolja a szükséges üzemanyagot. Ugyanígy a Power BI-ban is szükség van egy üzemanyagtartályra, amelyben az adatkészlethez szükséges adatok vannak. Az üzemanyagtartály ebben az esetben egy Power BI Desktop-fájl, egy Excel-munkafüzet vagy egy .CSV-fájl.

És még nincs vége. Az autó üzemanyagtartályát meg kell tölteni üzemanyaggal. A Power BI Desktop-, Excel- vagy .CSV-fájlban tárolt üzemanyagot egy másik adatforrás adatai jelentik. A másik adatforrás adatait helyezzük el egy Excel-, Power BI Desktop- vagy .CSV-fájlban. Excel-munkafüzet vagy .CSV-fájl esetében magunk írhatjuk be az adatsorokat. De csatlakozhatunk külső adatforráshoz is, amelyből lekérdezhetjük és betölthetjük az adatokat a fájlba. Amint rendelkezésünkre áll egy-két, adatot tartalmazó fájl, beolvashatjuk őket adatkészletként a Power BI-ba.

> [!NOTE]
> Az Excel-munkafüzetekből származó adatok csak akkor importálhatók a Power BI-ba, ha táblázatban vagy az adatmodellben szerepelnek.
> 
> 

## <a name="where-your-file-is-saved-makes-a-difference"></a>Nem mindegy, hogy hová menti a fájlokat
**Helyi meghajtó** – Ha a fájlt a saját számítógépére vagy a cég valamilyen más helyére mentette, a Power BI-ból *importálhatja* a fájlt Power BI-ba. Mivel a fájl ténylegesen a helyi meghajtón marad, a rendszer valójában nem importálja a teljes fájlt a Power BI-ba. Valójában az történik, hogy létrejön egy új adatkészlet az Ön Power BI-webhelyén, a rendszer pedig betölti abba az adatokat és – olykor – az adatmodellt. Ha a fájlban jelentések is találhatók, azok a Power BI-webhelyen, a Jelentések között fognak megjelenni.

**OneDrive – vállalati verzió** – Ha OneDrive Vállalati verzióval rendelkezik, és a Power BI-hoz is használt fiókkal jelentkezik be oda, akkor a leghatékonyabb megoldást választja ahhoz, hogy a Power BI Desktop- vagy a .CSV-fájl, az adatbázis, a jelentések és az irányítópultok szinkronban maradjanak a Power BI-ban. Mivel a Power BI és a OneDrive egyaránt a felhőben található, a Power BI nagyjából óránként kapcsolódik a OneDrive-on található fájlhoz. Ha bármilyen változást érzékel, az adatkészlet, a jelentések és az irányítópultok automatikusan frissülnek a Power BI-ban.

**OneDrive – Személyes verzió** – A OneDrive Vállalati verzió számos előnyét akkor is élvezheti, ha fájljait a saját OneDrive-fiókjába menti. A legnagyobb különbség az, hogy amikor a fájlt először csatlakoztatja (az Adatok lekérése > Fájlok > OneDrive személyes verzió paranccsal), akkor a Microsoft-fiókjával kell a OneDrive-ba jelentkeznie, és ez általában eltér attól a fióktól, amelyet a Power BI-ba való belépéshez használ. Amikor a Microsoft-fiókjával jelentkezik be a OneDrive-ba, mindenképpen válassza a Maradjak bejelentkezve lehetőséget. Így a Power BI képes lesz nagyjából óránként kapcsolódni a fájlhoz, és gondoskodni róla, hogy a Power BI-ban lévő adatkészlet szinkronban legyen.

**SharePoint-csoportwebhelyek** – A Power BI Desktopban lévő fájloknak a SharePoint-csoportwebhelyekre történő mentése nagyjából ugyanúgy zajlik, mint a OneDrive Vállalati verzió esetében. A legnagyobb különbség a Power BI és a fájl csatlakoztatásának módja. Megadhat egy URL-címet, vagy csatlakozhat a gyökérmappához.

## <a name="ready-to-get-started"></a>Készen áll?
Ezekben a cikkekben további tájékoztatást talál a fájlok Power BI-ba történő beolvasásáról.

* [Adatok lekérdezése Excel-munkafüzetből](service-excel-workbook-files.md)
* [Adatok lekérdezése Power BI Desktop-fájlból](service-desktop-files.md)
* [Adatok lekérdezése vesszővel tagolt fájlból](service-comma-separated-value-files.md)

