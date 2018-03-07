---
title: "Oktatóanyag: Saját mértékek létrehozása a Power BI Desktopban"
description: "Oktatóanyag: Saját mértékek létrehozása a Power BI Desktopban"
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
LocalizationGroup: Learn more
ms.openlocfilehash: 96295ced577ddb18b8c56031278bf9a81cddf981
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="tutorial-create-your-own-measures-in-power-bi-desktop"></a>Oktatóanyag: Saját mértékek létrehozása a Power BI Desktopban
A Power BI Desktop leghatékonyabb adatelemzési megoldásai mértékek segítségével alakíthatóak ki. A mértékek segítségével számítások hajthatóak végre az adatokon a jelentések használata közben. Ez az oktatóanyag bemutatja, hogyan hozhat létre saját alapszintű mértékeket a Power BI Desktopban.

A cikk olyan Power BI-felhasználóknak szól, akik már jól ismerik a speciálisabb modellek létrehozásának eljárásait. Ehhez ismernie kell, hogyan importálhat adatokat az Adatok lekérése és a Lekérdezésszerkesztő segítségével, hogyan dolgozhat több kapcsolódó táblával, és hogyan adhat mezőket a jelentésvászonhoz. Ha még csak most ismerkedik a Power BI Desktoppal, mindenképp tekintse át az [Első lépések a Power BI Desktopban](desktop-getting-started.md) című szakaszt.

Az oktatóanyag lépéseinek végrehajtásához töltse le a [Power BI Desktophoz készült Contoso értékesítési mintafájlt](http://download.microsoft.com/download/4/6/A/46AB5E74-50F6-4761-8EDB-5AE077FD603C/Contoso%20Sales%20Sample%20for%20Power%20BI%20Desktop.zip). Ez már eleve tartalmazza a fiktív Contoso, Inc. vállalat online értékesítési adatait. Mivel a fájlban lévő adatok egy adatbázisból lettek importálva, nem tud majd az adatforráshoz kapcsolódni, illetve megtekinteni azt a Lekérdezésszerkesztőben. Miután letöltötte a fájlt a számítógépére, azonnal nyissa is meg azt a Power BI Desktopban.

## <a name="what-are-these-measures-all-about"></a>Mik is ezek a mértékek lényegében?
A mértékeket leggyakrabban automatikusan hozza létre a rendszer, például amikor bejelöli a **Sales** **SalesAmount** mezője melletti négyzetet a mezők listájában, vagy amikor áthúzza a **SalesAmount** mezőt a jelentésvászonra.

![](media/desktop-tutorial-create-measures/measurestut_salesamountinfieldlist.png)

Megjelenik egy új, a következőhöz hasonló diagramvizualizáció:

![](media/desktop-tutorial-create-measures/meastut_salesamountchart.png)

Egy oszlopdiagramot kapunk, amely a SalesAmount mezőben található értékesítések értékének összegét mutatja.  A SalesAmount mező lényegében nem más, mint az importált Sales tábla SalesAmount elnevezésű oszlopa.

A SalesAmount oszlop több mint kétmillió sornyi értékesítési összeget tartalmaz. Talán érdekli, hogy miért nem jelenik meg egy tábla mindezekkel az értéksorokkal. Nos, a Power BI Desktop tudja, hogy a SalesAmount összes értéke numerikus típusú adat, és hogy ezeket valószínűleg valahogy szeretné majd összesíteni, például összeadni, átlagolni, megszámlálni stb.

Ha a Mezők listájában egy mezőnél a szigma ikon ![](media/desktop-tutorial-create-measures/meastut_sigma.png) látható, ez azt jelzi, hogy a mező numerikus, és az értékei összesíthetők. Ebben az esetben a SalesAmount kiválasztásakor a Power BI Desktop létrehoz egy saját mértéket, kiszámítja és a diagramon megjeleníti az értékesítés összegét.

Az összegzés a numerikus típusú az alapértelmezett összesítés, de egyszerűen lehet más típusú összesítésre is váltani.

Az **Érték** területen a **SalesAmount** melletti lefelé mutató nyílra kattintva kiválaszthatja az **Átlag** lehetőséget.

![](media/desktop-tutorial-create-measures/meastut_salesamountaverage.png)

A vizualizáció módosul, és a SalesAmount mező értékeinek átlagát mutatja.

![](media/desktop-tutorial-create-measures/meastut_salesamountaveragechart.png)

Az összesítés típusa a kívánt eredménytől függően módosítható, azonban nem minden típusú összesítés alkalmazható minden numerikus adattípusra. Például a SalesAmount mező esetében az Összeg és az Átlag típusnak van értelme. A Minimum és a Maximum is alkalmazható. A Számnak azonban nem igazán lenne értelme, mert bár ugyan a SalesAmount mező numerikus értékeket tartalmaz, azok valójában pénznemben kifejezett összegeket tartalmaznak.

A mértékek megértéséhez elengedhetetlen az összesítések megértése, mivel minden mérték valamilyen típusú összesítést hajt végre. Az Összeg összesítésre nemsokára bemutatunk még néhány példát, amikor majd saját mértékeket fogunk létrehozni.

A mértékekből számított értékek a jelentésben végrehajtott beállításoktól függően mindig változnak. Ha például áthúzzuk a **RegionCountryName** (Régió/országnév) mezőt a **Geography** (Földrajzi hely) tábláról a diagramra, a jelentés országokra bontva átlagolja és jeleníti meg az értékesítési összeget.

![](media/desktop-tutorial-create-measures/meastut_salesamountavchartbyrcn.png)

Amikor egy mérték eredménye a jelentés használata közben módosul, lényegében a mérték *környezetét* módosítjuk. Azaz minden alkalommal, amikor módosítja a jelentés beállításait, azt a környezetet módosítja, amelynek alapján a mérték az eredményeit kiszámítja és megjeleníti.

A legtöbb esetben a Power BI teszi a dolgát, és az értékeket a hozzáadott mezőknek és a kiválasztott összesítéseknek megfelelően kiszámítja és megjeleníti. Más esetekben azonban az összetettebb, egyedi számításokhoz saját mértékeket kell létrehoznia.

A Power BI Desktopban az egyéni mértékek a Data Analysis Expressions (Adatelemzési kifejezések, DAX) képletnyelv használatával hozhatóak létre. A DAX-képletek az Excel-képletekhez rendkívül hasonlók. Valójában a DAX számos függvénye, operátora és szintaxisa megegyezik az Excelben található képletekkel. A DAX-függvények azonban relációs adatbázisokhoz lettek kialakítva, és a jelentések kezelése során dinamikusabb számításokat hajtanak végre.

Összesen több mint 200 DAX-függvény létezik az egyszerű összesítő függvényektől, mint az Összeg és az Átlag, az összetettebb statisztikai és szűrőfüggvényekig. Itt most nem megyünk bele részletesen a DAX nyelv ismertetésébe, azonban számos forrásanyag létezik, amelyből megismerheti azt. Miután végzett ezzel az oktatóanyaggal, mindenképp tekintse át a következő forrásanyagot: [A DAX alapszintű használata a Power BI Desktopban](desktop-quickstart-learn-dax-basics.md).

Amikor saját mértékeket hoz létre, azok felkerülnek a kívánt tábla Mezők listájára. Ezeket *modellmértékeknek* nevezzük, és mezőként használhatóak a táblában. A modellmértékek egyik nagy előnye, hogy tetszés szerint elnevezhetjük azokat, így könnyebb azonosítani őket. Emellett argumentumként használhatóak más DAX-kifejezésekben, és olyan mértékek is létrehozhatóak, amelyek igen gyorsan végeznek el összetett számításokat.

## <a name="lets-create-our-own-measure"></a>Hozzunk létre saját mértékeket
Tegyük fel, hogy a nettó értékesítést szeretnénk elemezni. Ha megtekintjük a Sales táblát a Mezők listájában, láthatjuk, hogy nincs NetSales nevű mező. Rendelkezünk azonban azokkal az elemekkel, amelyekből létrehozhatunk egy saját mértéket a nettó értékesítés számításához.

Egy olyan mértékre van szükségünk, amely levonja a kedvezményeket és a visszafizetéseket az értékesítés összegéből. Mivel azt szeretnénk, ha a mérték a vizualizációban lévő bármilyen környezetben számítana eredményt, lényegében le kell vonnunk a DiscountAmount (Kedvezmény összege) és a ReturnAmount (Visszatérítés összege) értékeket a SalesAmount összegéből. Ez most így talán egy kissé zagyvának hat, de nemsokára kitisztul.

### <a name="net-sales"></a>Nettó értékesítés
1.  A mezők listájában kattintson jobb gombbal a **Sales** táblára vagy bal gombbal a mellette lévő lefelé mutató nyílra, majd kattintson az **Új mérték** gombra. Ez menti az új mértéket a Sales táblába, ahol majd könnyebben megtaláljuk.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure.png)
    
    > [!TIP]
    > Új mértékek létrehozásához használhatja az Új mérték gombot is a Power BI Desktop menüszalagjának Kezdőlapján.
    > 
    > ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasureribbon.png)
    > 
    > Amikor a menüszalagról hoz létre mértéket, az bármelyik táblában létrehozható. Bár a mértékeknek nem kell adott táblához tartozniuk, könnyebben megtalálja őket, ha az Ön számára leginkább logikus táblában hozza létre őket. Ha egy adott táblában szeretné a mértéket létrehozni, előbb a táblára kattintva tegye azt aktívvá. Ezután kattintson az Új mérték gombra. Esetünkben az első mértéket a Sales táblában hozzuk létre.
    > 
    > 
    
    A szerkesztőléc a jelentésvászon felső részén található. Itt nevezhetjük át a mértéket, és itt adhatunk hozzá DAX-képletet.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formulabar.png)
    
    Adjunk egy nevet az új mértéknek. Alapértelmezés szerint az új mértékek neve egyszerűen Mérték lesz. Ha ezt nem nevezzük át, a következő létrehozott mérték a Mérték 2, Mérték 3 stb. nevet kapja majd. Mi most azonban szeretnénk, ha a mértékek könnyen azonosíthatóak lennének, ezért nevezzük át az új mértéket Net Sales (Nettó értékesítés) névre.
    
2. Jelölje ki a **Mérték** nevet a szerkesztőlécen, majd írja be a **Net Sales** nevet.
    
    Most pedig lássunk hozzá a képlet megadásához.
    
3.  Az egyenlőségjel után írja be az **S** betűt. Egy lenyíló lista jelenik meg, amely felkínálja az összes S betűvel kezdődő DAX-képletet. minél több karaktert ad meg, a lista annál jobban leszűkül a kívánt függvényre. Görgessen le, és válassza a **SUM** képletet, majd nyomja le az ENTER billentyűt.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_s.png)
    
    Az Enter billentyűt lenyomva egy nyitó zárójel jelenik meg, valamint a SUM függvénybe beadható oszlopokat tartalmazó javaslati lista.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_sum.png)
    
    A kifejezéseket mindig egy nyitó és egy záró zárójel fogja közre. Esetünkben a kifejezés egyetlen argumentumot tartalmaz, amelyet beadunk a SUM függvénybe: az összegezni kívánt oszlopot. Az oszlopok listáját az első betűk beírásával szűkíthetjük. Esetünkben most a SalesAmount oszlopot szeretnénk megadni, tehát ahogy elkezdjük beírni a salesam betűket, a lista egyre szűkül, és végül két elem közül választhatunk. Valójában mindkettő ugyanazt az oszlopot jelöli. Az egyik egyszerűen [SalesAmount] néven jelenik meg, mivel a mértéket ugyanabban a táblában hozzuk létre, amelyikben a SalesAmount oszlop is van. A másik elemben a tábla neve is szerepel az oszlop neve előtt.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_salesam.png)
    
    Általában érdemes az oszlopok teljes nevét megadni. Így a képletek könnyebben olvashatóak.
    
4. Válassza a **Sales[SalesAmount]** elemet, majd írjon be egy záró zárójelet.
    
    > [!TIP]
    > A szintaxishibákat leggyakrabban a hiányzó vagy rossz helyre beírt záró zárójelek okozzák.
    > 
    > 
    
    Most pedig ki szeretnénk vonni a másik két oszlopot.
    
5.  Az első kifejezés záró zárójele után írjon be egy szóközt, majd egy mínusz operátort (**-**) és végül még egy szóközt. Ezután írja be megint a SUM függvényt, argumentumként ezúttal a **Sales[DiscountAmount]** oszloppal.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_discamount.png)
    
    Kezd elfogyni a helye a szerkesztőlécben. Semmi gond.
    
6.  Kattintson a lefelé mutató nyílra a szerkesztőléc jobb oldalán.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_chevron.png)
    
    Mindjárt több lett a hely. Az Alt+Enter billentyűkombinációt lenyomva egy új sor nyílik meg, ahol újabb részekkel egészíthetjük ki a képletet. Az egyes elemeket feljebb is mozgathatjuk a Tab billentyű lenyomásával.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_formula_expanded.png)
    
    Most már beírhatjuk a képlet utolsó részét is.
    
7.  Adjon hozzá még egy mínusz operátort, majd még egy SUM függvényt, argumentumként a **Sales[ReturnAmount]** oszloppal.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_newmeasure_complete.png)
    
    A képlet most késznek tűnik.

8.  A véglegesítéséhez nyomja le az Enter billentyűt vagy kattintson a pipa jelre a szerkesztőlécen. A rendszer ellenőrzi a képletet, és hozzáadja azt a mezők listájához a Sales táblában.

### <a name="lets-add-our-new-measure-to-a-report"></a>Adjuk hozzá az új mértéket egy jelentéshez
Most a Net Sales mértéket felvehetjük a jelentésvászonra, és a rendszer a jelentéshez hozzáadott összes mezőre számolni fogja a nettó értékesítést. Lássuk a nettó értékesítést országonként.

1.  Húzza a **Net Sales** mértéket a **Sales** tábláról a jelentésvászonra.
    
2. Most húzza a **RegionCountryName** (Régió/országnév) mezőt a **Geography** (Földrajzi hely) táblából a diagramra.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_byrcn.png)
    
    Adjunk hozzá további adatokat.
    
3.  Húzza a **SalesAmount** mezőt a diagramra, hogy a nettó értékesítés és az értékesítés összege közti különbség is látható legyen.
    
    Most lényegében két mérték jelenik meg a diagramon. az automatikusan összegzett SalesAmount, valamint az imént létrehozott Net Sales mérték. Mindkettő esetében az eredmények egy, a diagramon megjelenő másik mező, a RegionCountryName (Régió/országnév) országai alapján számolódnak.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_byrcnandsalesamount.png)
    
    Adjunk hozzá egy szeletelőt, hogy tovább bonthassuk a nettó értékesítés és az értékesítés összegét naptári évek szerint.
    
4.  Kattintson a diagram egy üres területére, majd a **Vizualizációk** menüben a Tábla vizualizációra.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_blanktablevisbutton.png)
    
    Ez létrehoz egy üres táblavizualizációt a jelentésvásznon.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_blanktable.png)
    
5.  Húzza a **Year** (Év) mezőt a **Calendar** (Naptár) táblából erre az új üres táblára.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_yearaggtable.png)
    
    Mivel a Year egy numerikus mező, a Power BI Desktop összegezte a benne lévő értékeket, és megjelenített egy diagramot. Ez azonban szeletelőként így nem igazán használható.
    
6. Az **Értékek** menüben kattintson a **Year** mező mellett a lefelé mutató nyílra, majd kattintson az **Összegzés mellőzése** lehetőségre.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_year_donotsummarize.png)
    
    Most már átalakíthatjuk a Year mezőt szeletelővé a táblavizualizációban.

    7.  A **Vizualizációk** menüben kattintson a **Szeletelő** vizualizációra.

    ![](media/desktop-tutorial-create-measures/meastut_netsales_year_changetoslicer.png)
    
    Így most hozzáadtuk a Year mezőt szeletelőként. Ha most bármelyik évet vagy évek csoportját kiválasztjuk, a jelentés vizualizációi annak megfelelően lesznek szeletelve.
    
8. Próbálja ki, és kattintson a **2013** évre. Láthatja, ahogy a diagram változik. A rendszer újraszámítja a Net Sales és a SalesAmount mértékeket, és azokban most csak a 2013-ra vonatkozó új eredmények láthatóak. Így tehát most újra módosítottuk a környezetet, amelyben a rendszer a mértékeket számítja és az eredményeket megjeleníti.
    
    ![](media/desktop-tutorial-create-measures/meastut_netsales_chartslicedbyyear.png)

## <a name="lets-create-another-measure"></a>Hozunk létre egy újabb mértéket
Most hogy már tudja, hogyan hozhat létre mértékeket, hozzunk létre egy újabbat.

### <a name="net-sales-per-unit"></a>Nettó értékesítés egységenként
Mit tegyünk, ha azt szeretnénk megtudni, hogy melyik az eladott egységenként legnagyobb értékesítést produkáló termékünk?

Nos, létrehozhatunk egy újabb mértéket. Ebben az esetben a nettó értékesítést el kell osztanunk az értékesített egységek mennyiségével. Lényegében a Net Sales mérték eredményét a Sales[SalesQuantity] összegével szeretnénk osztani.

1.  Hozzon létre egy új mértéket **Net Sales per Unit** (Nettó értékesítés egységenként) néven a Sales (Értékesítés) vagy a Products (Termékek) táblában.
    
    Ebben a mértékben a korábban létrehozott Net Sales mértéket fogjuk használni. A DAX-képletekben hivatkozhatunk más mértékekre is.
    
2.  Kezdje el beírni a **Net Sales** nevét. A javaslati listában jelennek meg a lehetőségek, amelyek közül választhatunk. Válassza a **[Net Sales]** mértéket.
    
    ![](media/desktop-tutorial-create-measures/meastut_nspu_formulastep2a.png)
    
    Ha mértékre szeretne hivatkozni, elég csak beírnia egy nyitó szögletes zárójelet (**[**). A javaslati listában ekkor csak a képlethez hozzáadható mértékek jelennek meg.
    
    ![](media/desktop-tutorial-create-measures/meastut_nspu_formulastep2b.png)
    
3.  Közvetlenül a **[Net Sales]** után írjon be egy szóközt, majd egy osztás operátort (**/**), majd adjon meg egy SUM függvényt, és írja be a **Quantity** (Mennyiség) nevet. A javaslati lista ekkor az összes olyan oszlopot tartalmazza, amelyeknek szerepel a Quantity kifejezés a nevében. Válassza a **Sales[SalesQuantity]** elemet. A képletnek most így kell kinéznie:
    
    > **Net Sales per Unit = [Net Sales] / SUM(Sales[SalesQuantity])**
    > 
    > 
    
    Szép, nem? A DAX-képletek beírása igazából meglehetősen egyszerű a DAX-szerkesztő keresési és javaslati funkcióinak használatával. Most lássuk, milyen eredményeket kapunk az új Net Sales per Unit mértékkel.
    
4. Húzza a **Net Sales per Unit** mértéket a jelentésvászon egy üres területére.
    
    ![](media/desktop-tutorial-create-measures/meastut_nspu_chart.png)
    
    Hát nem valami érdekes, nemde? Ne aggódjon.
    
5.  Módosítsa a diagramvizualizáció típusát **Faszerkezetes térképre**.
    
    ![](media/desktop-tutorial-create-measures/meastut_nspu_changetotreemap.png)
    
6. Most húzza a **ProductCategory** (Termékkategória) mezőt a **ProductCategory** tábláról a **Csoport** területre.
    
    ![](media/desktop-tutorial-create-measures/meastut_nspu_byproductcat.png)
    
    Ezek értékes információk, de mit csináljunk, ha a termékenkénti nettó értékesítés érdekel bennünket?
    
7. Távolítsa el a **ProductCategory** mezőt, majd húzza helyette a **ProductName** (Terméknév) mezőt a **Product** tábláról a **Csoport** területre. 
    
    ![](media/desktop-tutorial-create-measures/meastut_nspu_byproductname.png)
    
    Rendben, ez itt most csak játszadozás, de azért elég menő, ezt be kell ismernie! Természetesen ezt a faszerkezetes térképet számos különböző módon szűrhetjük, ez azonban a jelen oktatóanyagnak nem témája.

## <a name="what-weve-learned"></a>A megismert témák
A mértékek rengeteg lehetőséget kínálnak az adatokból kinyerhető információk elemzéséhez. Megtanultuk, hogyan hozhatunk létre mértékeket a szerkesztőléc segítségével. A mértékeknek, ha értelmét látjuk, nevet is adhatunk, a javaslati listákkal pedig könnyedén megtalálhatjuk és kiválaszthatjuk a képletekbe beilleszteni kívánt megfelelő elemeket. Megismertük a környezeteket is, amelyekben a mértékek számítási eredményei más mezőknek vagy a mértékképletben foglalt egyéb kifejezéseknek megfelelően módosulnak.

## <a name="next-steps"></a>Következő lépések
Ha szeretné a DAX-képleteket részletesebben megismerni, és speciálisabb mértékeket létrehozni olvassa el [A DAX alapszintű használata a Power BI Desktopban](desktop-quickstart-learn-dax-basics.md) című cikket. Ez a cikk a DAX alapvető fogalmaira, a szintaxisra, a függvényekre és a környezet alaposabb megértésére összpontosít.

Mindenképp vegye fel a [Data Analysis Expressions (DAX) referenciát](https://msdn.microsoft.com/library/gg413422.aspx) a kedvencei közé. Ebben találja részletesen leírva a DAX-szintaxist, az operátorokat, valamint a több mint 200 DAX-függvényt.

