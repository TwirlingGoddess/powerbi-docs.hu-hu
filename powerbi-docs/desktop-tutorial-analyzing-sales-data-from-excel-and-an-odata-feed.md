---
title: 'Oktatóanyag: Excelből és OData-csatornáról származó értékesítési adatok elemzése a Power BI Desktopban'
description: 'Oktatóanyag: Excelből és OData-csatornáról származó értékesítési adatok elemzése'
services: powerbi
documentationcenter: ''
author: davidiseminger
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/24/2018
ms.author: davidi
LocalizationGroup: Learn more
ms.openlocfilehash: aad93a6c636fb0d75ad89f9e3d9eb70ec203cc88
ms.sourcegitcommit: afa10c016433cf72d6d366c024b862187a8692fd
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/04/2018
---
# <a name="tutorial-analyzing-sales-data-from-excel-and-an-odata-feed"></a>Oktatóanyag: Excelből és OData-csatornáról származó értékesítési adatok elemzése
A **Power BI Desktop** használatával különféle adatforrásokhoz kapcsolódhat, majd az ezekből származó adatokat úgy kombinálhatja és alakíthatja, hogy érdekes és magukkal ragadó elemzéseket és vizualizációkat eredményezzenek. Ebben az oktatóanyagban megtanulhatja, hogyan kombinálja két adatforrás adatait. 

Igen gyakori, hogy az adatok több különböző adatforrásban találhatók, például a termékinformációk egy adatbázisban, az értékesítési adatok egy másikban. Az ebben a dokumentumban bemutatott példákban egy Excel-munkafüzetet és egy OData-csatornát alkalmazunk, azonban a technikák ugyanúgy alkalmazhatók más adatforrásokra, például SQL Server lekérdezésekre, CSV-fájlokra vagy bármely egyéb adatforrásra a Power BI Desktopban.

Ebben az oktatóanyagban az adatokat az Excelből (a termékinformációkat) és egy OData-csatornáról (a megrendelések adatait) importáljuk. Átalakítási és összesítési műveleteket hajtunk végre, és a két forrásból származó adatokat kombinálva létrehozunk egy interaktív vizualizációkat is tartalmazó **Összes értékesítés termék és év szerint** jelentést. 

A végleges jelentés így fog kinézni:

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/18.png)

Az oktatóanyagban szereplő lépések végrehajtásához szükség lesz a Termékek munkafüzetre, amelyet letölthet: **[Kattintson ide a Products.xlsx fájl letöltéséhez](http://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Products.xlsx)**

A **Mentés másként** párbeszédablakban nevezze el a fájlt **Products.xlsx** néven.

## <a name="task-1-get-product-data-from-an-excel-workbook"></a>1. feladat: Termékadatok betöltése Excel-munkafüzetből
Ebben a feladatban a Products.xlsx fájlból a Power BI Desktopba importáljuk a termékeket.

### <a name="step-1-connect-to-an-excel-workbook"></a>1. lépés: Kapcsolódás az Excel-munkafüzethez
1. Indítsa el a Power BI Desktopot.
2. A Kezdőlap menüszalagon válassza az **Adatok lekérése** lehetőséget. Az Excel egyike a **Leggyakoribb** adatkapcsolatoknak, így közvetlenül kiválasztható az **Adatok lekérése** menüből.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_1.png)
3. Ha közvetlenül az Adatok lekérése gombra kattint, itt választhatja a **Fájl \> Excel**, majd a **Kapcsolódás** lehetőséget.
4. A **Fájl megnyitása** párbeszédablakban válassza ki a **Products.xlsx** fájlt.
5. A **Kezelő** ablaktáblán válassza a **Termékek** táblát, majd a **Szerkesztés** lehetőséget.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_2.png)

### <a name="step-2-remove-other-columns-to-only-display-columns-of-interest"></a>2. lépés: Az egyéb oszlopok eltávolítása, hogy csak a lényeges oszlopok jelenjenek meg
Ebben a lépésben a **ProductID** (Termékazonosító), **ProductName** (Terméknév), **UnitsInStock** (Készletmennyiség) és **QuantityPerUnit** (MennyiségEgységenként) oszlopokon kívül az összes többi oszlopot eltávolítja. A Power BI Desktopban gyakori, hogy egy adott feladatot többféleképpen is el lehet végezni. Például a menüszalag számos gombja az oszlopok vagy cellák helyi menüjéből (jobb kattintás) is elérhető.

A Power BI Desktop Lekérdezésszerkesztő eszközével formázhatja és alakíthatja az adatkapcsolatokat. A **Kezelőben** a **Szerkesztés** gombra kattintva a Lekérdezésszerkesztő automatikusan megnyílik. Emellett megnyitható a Power BI Desktop **Kezdőlap** menüszalagján a **Lekérdezések szerkesztése** lehetőséget választva is. A következő lépéseket a Lekérdezésszerkesztőben kell végrehajtania.

1. A Lekérdezésszerkesztőben jelölje ki a **ProductID**, a **ProductName**, a **QuantityPerUnit** és a **UnitsInStock** oszlopokat (több külön oszlop kijelöléséhez használja a **Ctrl+kattintás**, több egymás mellett állóhoz a **Shift+kattintás** kombinációt).
2. Válassza az **Oszlopok eltávolítása** \> **További oszlopok eltávolítása** parancsot a menüszalagon, vagy kattintson jobb gombbal az oszlopfejlécre, majd kattintson **További oszlopok eltávolítása** elemre.

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/anlayzingsalesdata_removeothercolumns.png)

### <a name="step-3-change-the-data-type-of-the-unitsinstock-column"></a>3. lépés: A UnitsInStock oszlop adattípusának módosítása
Miután a Lekérdezésszerkesztő kapcsolódott az adatokhoz, megvizsgálja az egyes mezőket, és meghatározza azok optimális adattípusát. Az Excel-munkafüzetben a készleten lévő termékek mennyisége mindig egész számként lesz megadva, így ebben a lépésben jóváhagyhatjuk, hogy a **UnitsInStock** oszlop adattípusa Egész szám.

1. Jelölje ki a **UnitsInStock** oszlopot.
2. Kattintson az **Adattípus** legördülő menü gombjára a **Kezdőlap** menüszalagon.
3. Ha nem Egész szám van beállítva, az adattípusnak válassza ki az **Egész szám** lehetőséget a legördülő menüből (az **Adattípus:** gomb az aktuális kijelölés adattípusát is megjeleníti).
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/anlayzingsalesdata_wholenumber.png)      

### <a name="power-bi-desktop-steps-created"></a>A Power BI Desktopban létrehozott lépések
Ahogy egymás után hajtja végre a különféle lekérdezési műveleteket a Lekérdezésszerkesztőben, a lekérdezés lépéseit azok létrehozását követően a **Lekérdezési beállítások** ablaktábla sorolja fel az **Alkalmazott lépések** listában. A lekérdezés mindegyik lépése rendelkezik egy megfelelő, az úgynevezett „M” nyelven íródott képlettel. További információk az „M” képletnyelvről: [A Power BI képletek bemutatása](https://support.office.com/Article/Learn-about-Power-Query-formulas-6bc50988-022b-4799-a709-f8aafdee2b2f).

| Feladat | Lekérdezési lépés | Képlet |
| --- | --- | --- |
| Kapcsolódás az Excel-munkafüzethez |Forrás |Source{[Name="Products"]}[Data] |
| Az első sor előléptetése a tábla oszlopfejléceivé |FirstRowAsHeader |[Table.PromoteHeaders](https://support.office.com/Article/TablePromoteHeaders-b8eaeb95-042a-42e1-9164-6d3c646acadc "Table.PromoteHeaders") <br /> (Products) |
| Az egyéb oszlopok eltávolítása, hogy csak a lényeges oszlopok jelenjenek meg |RemovedOtherColumns |[Table.SelectColumns](https://support.office.com/Article/TableSelectColumns-20bb9e28-9fd3-4cd2-a21b-97972c82ec22 "Table.SelectColumns")  <br />(FirstRowAsHeader,{"ProductID", "ProductName", "QuantityPerUnit", "UnitsInStock"}) |
| Adattípus módosítása |Típus módosítva |Table.TransformColumnTypes(\#"A többi oszlop eltávolítva",{{"UnitsInStock", Int64.Type}}) |

## <a name="task-2-import-order-data-from-an-odata-feed"></a>2. feladat: Megrendelésadatok importálása az OData-csatornáról
Ebben a feladatban megrendelésadatokat olvashat be. Ez a lépés az értékesítési rendszerekkel való kapcsolódást mutatja be. Az adatokat a Power BI Desktopba arról a minta Northwind OData-csatornáról importálhatja a következő URL-címen, amelyet az alábbi lépések során másolhat (és illeszthet be): <http://services.odata.org/V3/Northwind/Northwind.svc/> 

### <a name="step-1-connect-to-an-odata-feed"></a>1. lépés: Kapcsolódás az OData-csatornához
1. A Lekérdezésszerkesztőben a **Kezdőlap** menüszalagon válassza az **Adatok lekérése** lehetőséget.
2. Tallózással keresse meg az **OData-csatorna** adatforrást.
3. Az **OData-csatorna** párbeszédablakban illessze be a Northwind OData-csatorna **URL-címét**.
4. Kattintson az **OK** gombra.
5. A **Kezelő** ablaktáblán válassza az **Orders** (Megrendelések) táblát, majd a **Szerkesztés** lehetőséget.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/anlayzingsalesdata_odatafeed.png)

>[!NOTE]
>Ha valamelyik tábla nevére kattint, de nem jelöli be a jelölőnégyzetet, megtekintheti a tábla előnézetét.

### <a name="step-2-expand-the-orderdetails-table"></a>2. lépés: Az Order\_Details (Megrendelések részletei) tábla kibontása
Az **Orders** (Megrendelések) tábla egy hivatkozást tartalmaz a **Details** (Részletek) táblára, amely az egyes megrendelésekben érintett egyedi termékeket tartalmazza. Amikor olyan adatforráshoz kapcsolódik, amely több táblát is tartalmaz (például egy relációs adatbázishoz), az ilyen hivatkozások segítségével állíthatja össze a lekérdezést. 

Ebben a lépésben kibontjuk az **Orders** (Megrendelések) táblához kapcsolódó **Order\_Details** (Megrendelések részletei) táblát, és így kombináljuk az **Order\_Details** (Megrendelések részletei) tábla **ProductID** (Termékazonosító), **UnitPrice** (Egységár) és **Quantity** (Mennyiség) oszlopait az **Orders** (Megrendelések) táblán. Az alábbi ábra a táblákon lévő adatok sémáját mutatja:

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/orderdetails.png)

A **Kibontás** művelettel egy kapcsolódó tábla adatai kombinálhatóak egy érintett táblán. A lekérdezés futtatásakor a kapcsolódó tábla (**Order\_Details**) sorai az érintett tábla (**Orders**) soraivá lesznek kombinálva.

Miután kibontotta az **Order\_Details** táblát, az **Orders** tábla három új oszloppal és további sorokkal bővül, a beágyazott vagy kapcsolódó tábla minden sora után eggyel.

1. A **Lekérdezés nézetében** görgessen az **Order\_Details** (Megrendelés részletei) oszlopra.
2. Az **Order\_Details** (Megrendelés részletei) oszlopban kattintson a Kibontás ikonra (![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/expand.png)).
3. A **Kibontás** legördülő menüben:
   1. Válassza **(Az összes oszlop kijelölése)** lehetőséget az összes oszlop törléséhez.
   2. Jelölje ki a **ProductID**, a **UnitPrice** és a **Quantity** oszlopokat.
   3. Kattintson az **OK** gombra.
      ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/7.png)

### <a name="step-3-remove-other-columns-to-only-display-columns-of-interest"></a>3. lépés: Az egyéb oszlopok eltávolítása, hogy csak a lényeges oszlopok jelenjenek meg
Ebben a lépésben az **OrderDate (Megrendelés dátuma), ShipCity** (Szállítási cím városa), **ShipCountry** (Szállítási cím országa), **Order\_Details.ProductID** (Megrendelés_részletei.Termékazonosító), **Order\_Details.UnitPrice** (Megrendelés_részletei.Egységár) és **Order\_Details.Quantity** (Megrendelés_részletei.Mennyiség) oszlopokon kívül az összes többi oszlopot eltávolítja. Az előző feladatban a **További oszlopok eltávolítása** parancsot használtuk. Ebben a feladatban a kijelölt oszlopokat fogjuk eltávolítani.

1. A **Lekérdezés nézetében** az a. és a b. pontok végrehajtásával jelölje ki az összes oszlopot:
   1. Kattintson az első oszlopra (**OrderID**).
   2. A Shift billentyűt lenyomva tartva kattintson az utolsó oszlopra (**Shipper**).
   3. Most, hogy az összes oszlop ki van jelölve, a Ctrl billentyűt lenyomva tartva kattintson a következő oszlopokra azok kijelölésének visszavonásához: **OrderDate**, **ShipCity**, **ShipCountry**, **Order\_Details.ProductID**, **Order\_Details.UnitPrice** és **Order\_Details.Quantity**.
2. Most, hogy csak az eltávolítani kívánt oszlopok vannak kijelölve, kattintson a jobb gombbal bármelyik kijelölt oszlop fejlécére, majd kattintson az **Oszlopok eltávolítása** lehetőségre.

### <a name="step-4-calculate-the-line-total-for-each-orderdetails-row"></a>Lépés 4: Az egyes Order\_Details (Megrendelés részletei) sorok végösszegének kiszámítása
A Power BI Desktop segítségével számításokat végezhet az importált oszlopok alapján, így bővítheti a betöltött adatokat. Ebben a lépésben egy **Egyéni oszlopot** hozunk létre az egyes **Order\_Details** (Megrendelés részletei) sorok végösszegének kiszámítására.

Az egyes **Order\_Details** (Megrendelés részletei) sorok végösszegének kiszámítása:

1. Az **Oszlop hozzáadása** szalagfülön kattintson a **Hozzáadás** **Egyéni oszlop** lehetőségre.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_4.png)
2. Az **Egyéni oszlop hozzáadása** párbeszédablak **Egyéni oszlopképlet** szövegmezőjébe írja be az **[Order\_Details.UnitPrice]**  \* **[Order\_Details.Quantity]** képletet.
3. Az **Új oszlop neve** szövegmezőbe írja be a **LineTotal** (Sor összege) nevet.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/8.png)
4. Kattintson az **OK** gombra.

### <a name="step-5-set-the-datatype-of-the-linetotal-field"></a>5. lépés: A LineTotal mező adattípusának beállítása
1. Kattintson a jobb gombbal a **LineTotal** oszlopra.
2. Válassza a **Típus módosítása** lehetőséget, majd a **Tizedes tört szám** értéket.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/9.png)

### <a name="step-6-rename-and-reorder-columns-in-the-query"></a>6. lépés: A lekérdezés oszlopainak átnevezése és átrendezése
Ebben a lépésben átnevezzük és átrendezzük a modell végső oszlopait, hogy könnyebb legyen azt használni a jelentések létrehozása során.

1. A **Lekérdezésszerkesztőben** húzza a **LineTotal** oszlopot balra, a **ShipCountry** oszlop mögé.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/10.png)
2. Törölje az *Order\_Details.* előtagot az **Order\_Details.ProductID**, az **Order\_Details.UnitPrice** és az **Order\_Details.Quantity** oszlopok nevében. Ehhez kattintson duplán az adott oszlopok fejlécére, majd törölje az adott szövegrészletet az oszlop nevéből.

### <a name="power-bi-desktop-steps-created"></a>A Power BI Desktopban létrehozott lépések
Ahogy egymás után hajtja végre a különféle lekérdezési műveleteket a Lekérdezésszerkesztőben, a lekérdezés lépéseit azok létrehozását követően a **Lekérdezési beállítások** ablaktábla sorolja fel az **Alkalmazott lépések** listában. A lekérdezés mindegyik lépése rendelkezik egy megfelelő egy úgynevezett „M” nyelven íródott Power Query képlettel. További információk erről a képletnyelvről: [A Power BI képletek bemutatása](https://support.office.com/Article/Learn-about-Power-Query-formulas-6bc50988-022b-4799-a709-f8aafdee2b2f "A Power Query képletek bemutatása").

| Feladat | Lekérdezési lépés | Képlet |
| --- | --- | --- |
| Kapcsolódás OData-csatornához |Forrás |Source{[Name="Orders"]}[Data] |
| Az Order\_Details tábla kibontása |Az Order\_Details kibontása |[Table.ExpandTableColumn](https://support.office.com/Article/TableExpandTableColumn-54903f25-75a2-4a44-a9a3-52a9d895ee98 "Table.ExpandTableColumn") <br /> (Orders, "Order\_Details", {"ProductID", "UnitPrice", "Quantity"}, {"Order\_Details.ProductID", "Order\_Details.UnitPrice", "Order\_Details.Quantity"}) |
| Az egyéb oszlopok eltávolítása, hogy csak a lényeges oszlopok jelenjenek meg |RemovedColumns |[Table.RemoveColumns](https://support.office.com/Article/TableRemoveColumns-6265190e-2f58-4300-85b8-df88fc1a67d3 "Table.RemoveColumns") <br />(\#"Expand Order\_Details",{"OrderID", "CustomerID", "EmployeeID", "RequiredDate", "ShippedDate", "ShipVia", "Freight", "ShipName", "ShipAddress", "ShipCity", "ShipRegion", "ShipPostalCode", "ShipCountry", "Customer", "Employee", "Shipper"}) |
| Az egyes Order\_Details sorok végösszegének kiszámítása |InsertedColumn |[Table.AddColumn](https://support.office.com/Article/TableAddColumn-6c64d0a5-9654-4d15-bfb6-9cc380aaf3c0 "Table.AddColumn") <br /> (RemovedColumns, "Custom", each [Order\_Details.UnitPrice] \* [Order\_Details.Quantity]) |

## <a name="task-3-combine-the-products-and-total-sales-queries"></a>3. feladat: A Products (Termékek) és a Total Sales (Összes értékesítés) lekérdezés kombinálása
A Power BI Desktopban nem szükséges kombinálni a lekérdezéseket ahhoz, hogy jelentéseket készíthessen belőlük. Ehelyett létrehozhat **Kapcsolatokat** az adatkészletek között. Ezek a kapcsolatok bármely olyan oszlopra létrehozhatóak, amely mindegyik érintett adatkészletben megtalálható. További információ: [Kapcsolatok létrehozása és kezelése](desktop-create-and-manage-relationships.md).

Ebben az oktatóanyagban az Orders (Megrendelések) és a Products (Termékek) adatai is tartalmaznak „ProductID” (Termékazonosító) mezőt, ezért gondoskodnunk kell róla, hogy a Power BI Desktopban használt modellben létezzen ezek között kapcsolat. Egyszerűen adja meg a Power BI Desktopban, hogy a két táblában ezek az oszlopok kapcsolatban vannak (azaz ugyanazokat az értékeket veszik fel). A Power BI Desktop automatikusan beállítja a kapcsolat irányát és számosságát. Egyes esetekben képes automatikusan észlelni is a kapcsolatokat.

Ebben a feladatban ellenőrizni fogjuk, hogy létrejött-e a kapcsolat a Power BI Desktopban a **Products** és a **Total Sales** lekérdezések közt.

### <a name="step-1-confirm-the-relationship-between-products-and-total-sales"></a>1. lépés: A Products és a Total Sales közötti kapcsolat ellenőrzése
1. Először be kell töltenünk a Lekérdezésszerkesztőben létrehozott modellt a Power BI Desktopba. A Lekérdezésszerkesztő **Kezdőlap** menüszalagján válassza a **Bezárás és betöltés** lehetőséget.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_4.png)
2. A Power BI Desktop betölti az adatokat a két lekérdezésből.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/11.png)      
3. Az adatok betöltését követően kattintson a **Kapcsolatok kezelése** gombra a **Kezdőlap** menüszalagon.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_5.png)
4. Kattintson az **Új...** gombra
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_6.png)
5. Amikor megpróbáljuk létrehozni a kapcsolatot, láthatjuk, hogy az már létezik! Amint azt a **Kapcsolat létrehozása** párbeszédablak mutatja (az árnyékolt oszlopokkal), a két lekérdezés **ProductsID** mezői között már létre lett hozva a kapcsolat.
   
    ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/12.png)
6. Kattintson a **Mégse** gombra, majd válassza a **Kapcsolat** nézetet a Power BI Desktopban.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_7.png)
7. A lekérdezések közötti kapcsolatot ábrázoló alábbi séma jelenik meg.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_8.png)
8. A két lekérdezést összekötő vonalon lévő nyílra duplán kattintva a **Kapcsolat szerkesztése** párbeszédablak jelenik meg.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_9.png)
9. Itt nem kell módosításokat végrehajtanunk, ezért a **Mégse** gombra kattintva egyszerűen bezárjuk a **Kapcsolat szerkesztése** párbeszédablakot.

## <a name="task-4-build-visuals-using-your-data"></a>4. feladat: Vizualizáció létrehozása az adatok alapján
A Power BI Desktop segítségével különféle vizualizációkat hozhat létre, amelyek segítségével elemezheti az adatokat. Többoldalas jelentéseket is létrehozhat, és mindegyik oldalon több vizualizáció is szerepelhet. A vizualizációk kezelésével az adatok még részletesebben elemezhetőek és értelmezhetőek. További információk a jelentések szerkesztésérről: [Jelentések szerkesztése](service-interact-with-a-report-in-editing-view.md).

Ebben a feladatban a korábban betöltött adatok alapján hozhat létre jelentést. A Mezők panelen választhatja ki azokat az oszlopokat, amelyekből a vizualizációkat létre szeretné hozni.

### <a name="step-1-create-charts-showing-units-in-stock-by-product-and-total-sales-by-year"></a>1. lépés: A Stock by Product (Készleten lévő mennyiségek termékenként) és a Total Sales by Year (Teljes értékesítés évenként) diagramok létrehozása
Húzza a **UnitsInStock** (Készletmennyiség) mezőt a Mezők panelről (ez a képernyő jobb oldalán található) a vászon egy üres területére. Ezzel létrehoz egy Tábla vizualizációt. Ezután húzza a ProductName (Terméknév) mezőt a Tengely dobozba a Megjelenítések panel alsó felében. Ezután válassza a **Rendezés szempontja: \> UnitsInStock** lehetőséget a vizualizáció jobb felső sarkában lévő ikonra kattintva.

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/14.png)

Húzza az **OrderDate** (Megrendelés dátuma) mezőt a vászonra a az első diagram alá, majd (ugyanígy a Mezők panelről) a LineTotal (Sor összege) mezőt a vizualizációra, és válassza a Vonaldiagram lehetőséget. Ezzel az alábbi vizualizáció jön létre.

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/15.png)

 Ezután húzza a **ShipCountry** (Szállítási cím országa) mezőt a vászon jobb felső részére. Mivel egy földrajzi adatokat tartalmazó mezőt választott, a rendszer automatikusan létrehoz egy térképet. Most húzza a **LineTotal** mezőt az **Értékek** mezőbe, így a térképen a körök mérete az egyes országokon az adott országból feladott megrendelések **LineTotal** értékével arányosan változik.

![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/17.png)

### <a name="step-2-interact-with-your-report-visuals-to-analyze-further"></a>2. lépés: A jelentés vizualizációinak kezelése az adatok részletesebb elemzéséhez
A Power BI Desktopban a vizualizációk egymás közötti keresztkiemelések és szűrések segítségével további trendeket képesek mutatni. További információk: [Szűrők és kiemelések a jelentésekben](power-bi-reports-filters-and-highlighting.md)

1. Kattintson a **Kanadán lévő** világoskék körre. Láthatja, hogy a vizualizációk szűrve lettek, és csak a Kanadára vonatkozó Stock (**ShipCountry**) és Total Orders (**LineTotal**) adatokat mutatják.
   
   ![](media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/18.png)

## <a name="complete-sales-analysis-report"></a>Teljes értékesítéselemzési jelentés
Miután végrehajtotta a fenti lépéseket, az így eredményül kapott értékesítési jelentés a Products.xlsx fájl és a Northwind OData-csatorna adatait kombinálja. A jelentés vizualizációival kielemezhetőek az egyes országokra vonatkozó értékesítési adatok. Az oktatóanyag kész Power BI Desktop-fájlját [innen](http://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Analyzing_Sales_Data.pbix) töltheti le.

## <a name="next-steps"></a>Következő lépések
* [Olvassa el a többi Power BI Desktop-oktatóanyagot](http://go.microsoft.com/fwlink/?LinkID=521937)
* [Tekintse meg a Power BI Desktop videóit](http://go.microsoft.com/fwlink/?LinkID=519322)
* [Látogasson el a Power BI fórumára](http://go.microsoft.com/fwlink/?LinkID=519326)
* [Látogasson el a Power BI blogra](http://go.microsoft.com/fwlink/?LinkID=519327)


