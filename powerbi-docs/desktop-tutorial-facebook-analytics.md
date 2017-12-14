---
title: "Oktatóanyag: Facebook-elemzések a Power BI Desktop használatával"
description: "Oktatóanyag: Facebook-elemzések a Power BI Desktop használatával"
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: 3642a252467d504b61eb81f82d0b96f64a24f22b
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="tutorial-facebook-analytics-using-power-bi-desktop"></a>Oktatóanyag: Facebook-elemzések a Power BI Desktop használatával
Ez az oktatóanyag bemutatja, hogyan importálhatja és vizualizálhatja a **Facebookról** származó adatokat. Ebben az oktatóanyagban elsajátíthatja, hogyan csatlakozhat egy adott Facebook-oldalhoz (a Power BI oldalhoz), hogyan alkalmazhatja az adatátalakítási lépéseket, és hozhat létre egyes vizualizációkat.

A végrehajtandó lépések a következők:

* **1. feladat**: Kapcsolódás egy Facebook-oldalhoz
* **2. feladat**: Vizualizáció létrehozása a Jelentés nézettel
  
  * **1. lépés**: Fatérkép vizualizáció létrehozása
* **3. feladat**: Adatok formázása a Lekérdezés nézetben
  
  * **1. lépés**: A dátum-idő oszlop ketté bontása
  * **2. lépés**: Összesített érték hozzáadása egy kapcsolódó táblából
* **4. feladat**: További vizualizációk létrehozása a Jelentés nézettel
  
  * **1. lépés**: A lekérdezés betöltése a jelentésbe
  * **2. lépés**: Vonaldiagram és sávdiagram létrehozása

## <a name="task-1-connect-to-a-facebook-page"></a>**1. feladat: Kapcsolódás egy Facebook-oldalhoz**
Ebben a feladatban adatokat importálunk a [Microsoft Power BI Facebook](https://www.facebook.com/microsoftbi)-helyről (íme az URL-cím: *https://www.facebook.com/microsoftbi )*.

Ehhez az oldalhoz bárki kapcsolódhat, és végrehajthatja ezeket a lépéseket – nincs szükség speciális hitelesítő adatokra (a jelen lépésben használt saját Facebook-fiókjától eltekintve).

![](media/desktop-tutorial-facebook-analytics/1.png)

1. Az **Első lépések** párbeszédpanelen vagy a **Kezdőlap szalagfülön** válassza az **Adatok lekérése** lehetőséget.
2. Megjelenik az **Adatok lekérése** párbeszédpanel, amelyen számos különféle adatforrás közül választhat. Válassza a **Facebook** lehetőséget az **Egyéb** csoportban.
   
   ![](media/desktop-tutorial-facebook-analytics/t_fb_getdataother.png)
   
   A **Kapcsolódás** gombra kattintva egy párbeszédpanel jelenik meg, amely a külső szolgáltatások használatának kockázataira figyelmezteti.
   
   ![](media/desktop-tutorial-facebook-analytics/t_fb_connectingtotps.png)
3. A Folytatás gombra kattintva megjelenik a **Facebook** párbeszédpanel, ahol beillesztheti az oldal nevét (**microsoftbi**) a **Felhasználónév** mezőbe. Válassza a **Bejegyzések** lehetőséget a **Kapcsolat** legördülő menüből.
   
   ![](media/desktop-tutorial-facebook-analytics/2.png)
4. Kattintson az **OK** gombra.
5. Amikor a rendszer a hitelesítő adatokat kéri, jelentkezzen be a saját Facebook-fiókjával, és engedélyezze a Power BI-hozzáférést a fiókján keresztül.
   
   ![](media/desktop-tutorial-facebook-analytics/facebookcredentials.png)

Miután felépült a kapcsolat az oldallal, láthatja, ahogy az adatok a modellbe töltődnek. 

![](media/desktop-tutorial-facebook-analytics/t_fb_1-loadpreview.png)

Innen a **Lekérdezésszerkesztő** jeleníti meg az adatokat. A **Lekérdezésszerkesztő** a Power BI Desktop részét képezi, de egy külön ablakban töltődik be, ahol az adatkapcsolatokra vonatkozó összes átalakítást végrehajthatja.

![](media/desktop-tutorial-facebook-analytics/t_fb_1-intoqueryeditor.png)

Mikor elérte az adatok kívánt formáját, betöltheti azokat a Power BI Desktopba. Válassza a **Bezárás és betöltés** lehetőséget a **Kezdőlap** menüszalaglapról.

![](media/desktop-tutorial-facebook-analytics/t_fb_1-loadandclose.png)

Egy párbeszédpanel jelenik meg, amelyen az adatok a Power BI Desktop adatmodellbe való betöltése követhető nyomon.

![](media/desktop-tutorial-facebook-analytics/t_fb_1-loading.png)

Az adatok betöltését követően a **Jelentés** nézet nyílik meg, ahol a tábla oszlopai a jobb oldalon a **Mező** listában láthatóak.

![](media/desktop-tutorial-facebook-analytics/fbdesigner1.png)

## <a name="task-2-create-visualizations-using-the-report-view"></a>**2. feladat: Vizualizáció létrehozása a Jelentés nézettel**
Most, miután betöltötte az adatokat az oldalról, vizualizációk használatával gyorsan és egyszerűen elemezheti azokat.

**1. lépés:** Fatérkép vizualizáció létrehozása

A vizualizációk létrehozása egyszerű, csak áthúzzuk a mezőket a **Mező listából** a **Jelentés vászonra**.

Húzza a **type** (típus) mezőt a **Jelentés** vászonra. A Power BI Desktop létrehoz egy új vizualizációt a **Jelentés vásznon**. Ezután húzza a **type** (típus) mezőt a **Mezők** listából (ugyanazt a mezőt, amelyet az imént a **Jelentés** vászonra is) az **Érték** területre egy **Sáv** vizualizáció létrehozásához.

![](media/desktop-tutorial-facebook-analytics/fbdesigner2.png)

A vizualizáció típusa a **Vizualizáció** ablaktáblán egy másik ikonra kattintva bármikor módosítható. Módosítsuk a típust egy **Fatérképre** a megfelelő ikon kiválasztásával a **Vizualizációk** ablaktáblán, amint az a következő képen látható.

![](media/desktop-tutorial-facebook-analytics/fbdesigner3.png)

Most adjunk hozzá egy jelmagyarázatot, és módosítsuk egy adatpont színét. Kattintson a **Formátum** ikonra a **Vizualizációk** ablaktáblán – a **Formátum** ikon egy ecsetet ábrázol.

![](media/desktop-tutorial-facebook-analytics/fbdesigner3a.png)

A **Jelmagyarázat** melletti lefelé mutató nyílra kattintva a szakasz kibomlik, és megjelennek a kijelölt vizualizáció jelmagyarázatának formázási lehetőségei. Ebben az esetben a következő változtatásokat végeztük el:

* a **Jelmagyarázat** kapcsolót **Be** állásba toltuk, hogy a jelmagyarázat megjelenjen
* a **Jelmagyarázat pozíciója** legördülő listában a **Jobbra** lehetőséget választottuk
* a **Cím** kapcsolót szintén **Be** állapotba toltuk, hogy a jelmagyarázat címe is látható legyen
* beírtuk a **Típus** címet a jelmagyarázat címeként

A következő ábrán ezek a változtatások már el vannak végezve, és láthatóak a vizualizáción.

![](media/desktop-tutorial-facebook-analytics/fbdesigner3b.png)

Ezután módosítsuk az egyik adatpont színét. A hivatkozás adatpontját érdemes kék színre venni, hogy jobban hasonlítson a hiperhivatkozásokhoz általában használt színéhez.

Az **Adatszínek** melletti nyílra kattintva bontsa ki az adott szakaszt. Megjelennek az adatpontok, minden szín mellett egy-egy választónyíllal, amelyek segítségével adatpontonként külön szín állítható be.

![](media/desktop-tutorial-facebook-analytics/fbdesigner3c.png)

Ha az egyes adatpontok mellett a színmező lefelé mutató nyíl ikonjára kattint, megjelenik egy színválasztó panel, amelyen kiválaszthatja a kívánt színt. Ebben az esetben most a világoskék színt választjuk.

![](media/desktop-tutorial-facebook-analytics/fbdesigner3d.png)

Mindjárt jobb is. A következő ábrán láthatja, ahogy a szín alkalmazva lett a vizualizációban az adatpontra, és a jelmagyarázat is frissül, valamint annak színe megváltozik is az **Adatszínek** szakaszban.

![](media/desktop-tutorial-facebook-analytics/fbdesigner3e.png)

## <a name="task-3-shape-data-in-the-table"></a>**3. feladat: Adatok formázása a táblában**
Most, miután importálta a kijelölt táblát, és megkezdte a vizualizáció létrehozását, láthatja, hogy a lehető legjobb eredmények érdekében érdemes különféle adatformázási és -tisztítási lépéseket végrehajtania.

**1. lépés**: A dátum-idő oszlop ketté bontása

Ebben a lépésben kettéosztjuk a **created\_time** (létrehozás időpontja) oszlopot, hogy a dátum és az idő értékét külön kapjuk meg. Ha a Power BI Desktopot használja, és módosítani szeretne egy meglévő lekérdezést, ehhez el kell indítania a **Lekérdezésszerkesztőt**. Ehhez válassza a **Lekérdezések szerkesztése** lehetőséget a **Kezdőlapon**.

![](media/desktop-tutorial-facebook-analytics/t_fb_editquery.png)

1. A **Lekérdezésszerkesztő** táblázatában görgessen jobbra, amíg meg nem találja a **created\_time** oszlopot
2. Kattintson jobb gombbal egy oszlopfejlécre a **Lekérdezés előnézete** táblázatban, majd kattintson az **Oszlop felosztása \> Elválasztó alapján** lehetőségre az oszlopok felosztásához. Válassza az **Egyéni** lehetőséget az elválasztó karakterek legördülő listájában, és írja be a **„T”** karaktert. Ez a művelet a **Kezdőlap** szalagfül **Oszlopok kezelése** csoportjában is elérhető.
   
   ![](media/desktop-tutorial-facebook-analytics/9.png)
   
   ![](media/desktop-tutorial-facebook-analytics/10.png)
3. Nevezze át az újonnan létrehozott oszlopokat **created\_date** és **created\_time** névre.
4. Jelölje ki az új **created\_time** oszlopot, **** majd a **Lekérdezésnézet** szalagon lépjen az **Oszlop hozzáadása** lapra, és válassza az **Idő\>Óra** lehetőséget a **Dátumból és időből** csoportban. Ez hozzáad egy új oszlopot, amely az időnek csak az óra összetevőjét tartalmazza.
   
   ![](media/desktop-tutorial-facebook-analytics/11.png)
5. Módosítsa az új **Hour** oszlop típusát **Egész szám** értékre a **Kezdőlap** **Adattípus** menüjét lenyitva vagy jobb gombbal az oszlopra kattintva és az **Átalakítás\>Egész szám** lehetőséget választva.
   
   ![](media/desktop-tutorial-facebook-analytics/12.png)

**2. lépés**: Összesített érték hozzáadása egy kapcsolódó táblából

Ebben a lépésben hozzáadjuk a megosztások számát a beágyazott értékből, hogy felhasználhassuk azt a vizualizációkban.

1. Görgessen tovább jobbra, amíg el nem éri a **shares** (megosztások) oszlopot. A beágyazott érték azt jelenti, hogy még egy átalakítást el kell végeznünk, hogy megkapjuk a tényleges értékeket.
2. Az oszlopfejléc jobb felső részén válassza a ![](media/desktop-tutorial-facebook-analytics/14.png) ikont a **Kibontás/összesítés** szerkesztő megnyitásához. Válassza a **count** (darabszám) lehetőséget, majd kattintson az **OK** gombra. Ez hozzáadja a megosztások számát a tábla mindegyik sorához.
   
   ![](media/desktop-tutorial-facebook-analytics/15.png)
   
   Miután az adatok betöltődtek, nevezze át az oszlopot **shares** (megosztások) névre. Ehhez kattintson duplán az oszlop nevére vagy jobb gombbal magára az oszlopra, vagy válassza a **Lekérdezésnézet** szalagon az **Átnevezés** lehetőséget az **Átalakítás** lap **Minden oszlop** csoportjában.
3. Végül pedig módosítsa az új **shares** oszlop típusát **Egész szám** értékre. Ha az oszlop ki van jelölve, a típus módosításához kattintson jobb gombbal az oszlopra, és válassza az **Átalakítás\>Egész szám** lehetőséget, vagy **** lépjen a **Kezdőlapra**, és válassza az **Adattípus** legördülő menüt.

### <a name="query-steps-created"></a>A lekérdezéshez létrehozott lépések
Ahogy egymás után hajtja végre a különféle átalakításokat a Lekérdezés nézetben, a lekérdezés lépéseit azok létrehozását követően a **Lekérdezési beállítások** ablaktábla sorolja fel az **ALKALMAZOTT LÉPÉSEK** listában. A lekérdezés mindegyik lépése rendelkezik egy megfelelő egy úgynevezett „M” nyelven íródott lekérdezési képlettel.

![](media/desktop-tutorial-facebook-analytics/16.png)

| Feladat | Lekérdezési lépés | Képlet |
| --- | --- | --- |
| Kapcsolódás Facebook-forráshoz |Forrás |Facebook.Graph  (&quot;https://graph.facebook.com/microsoftbi/posts&quot;) |
| **Oszlopok felosztása** a szükséges értékek megkapása érdekében |Oszlop felosztása elválasztó alapján |Table.SplitColumn  (Source,&quot;created_time&quot;,Splitter.SplitTextByDelimiter(&quot;T&quot;),{&quot;created_time.1&quot;, &quot;created_time.2&quot;}) |
| Az új oszlopok **típusának módosítása** (automatikus lépés) |Típus módosítva |Table.TransformColumnTypes  (#&quot;Oszlop felosztása elválasztó alapján&quot;,{{&quot;created_time.1&quot;, type date}, {&quot;created_time.2&quot;, type time}}) |
| **Oszlop **átnevezése**** |Oszlopok átnevezve |Table.RenameColumns  (#&quot;Típus módosítva&quot;,{{&quot;created_time.1&quot;, &quot;created_date&quot;}, {&quot;created_time.2&quot;, &quot;created_time&quot;}}) |
| **Oszlop **beszúrása**** |Óra beszúrva |Table.AddColumn  (#&quot;Oszlopok átnevezve&quot;, &quot;Hour&quot;, each Time.Hour([created_time]), type number) |
| **Típus módosítása ** |Típus módosítva1 |Table.TransformColumnTypes  (#&quot;Óra beszúrva&quot;,{{&quot;Hour&quot;, type text}}) |
| **Értékek **kibontása beágyazott táblában**** |shares kibontása |Table.ExpandRecordColumn  (#&quot;Típus módosítva1&quot;, &quot;shares&quot;, {&quot;darabszám&quot;}, {&quot;shares.count&quot;}) |
| **Az oszlop **átnevezése**** |Oszlopok átnevezve1 |Table.RenameColumns  (#&quot; shares kibontása&quot;,{{&quot;shares.count&quot;, &quot;shares&quot;}}) |
| **Típus módosítása** |Típus módosítva2 |Table.TransformColumnTypes  (#&quot;Oszlopok átnevezve1&quot;,{{&quot;shares&quot;, Int64.Type}}) |

## <a name="task-4-create-additional-visualizations-using-the-report-view"></a>**4. feladat: További vizualizációk létrehozása a Jelentés nézettel**
Most, miután sikerült az adatokat az elemzés további részéhez szükséges formába átalakítani, az eredményül kapott táblát betölthetjük a jelentésünkbe, és további vizualizációkat hozhatunk létre.

**1. lépés:** A lekérdezés betöltése a jelentésbe

A lekérdezés eredményeinek a jelentésbe való betöltéséhez a **Bezárás és betöltés** lehetőséget kell választanunk a **Lekérdezésszerkesztőben**. Ez betölti a módosított adatokat a Power BI Desktopba, és bezárja a **Lekérdezésszerkesztőt**.

![](media/desktop-tutorial-facebook-analytics/t_fb_1-loadandclose.png)

A Power BI Desktopban mindenképp a **Jelentések** nézetben kell lennünk. Kattintson a legfelső ikonra a Power BI Desktop bal oldali menüsávján.

![](media/desktop-tutorial-facebook-analytics/17.png)

**2. lépés:** Vonaldiagram és sávdiagram létrehozása

Vizualizációk létrehozásához áthúzhatjuk a mezőket a **Mező listából** a **Jelentés vászonra**.

1. Húzza a **shares** mezőt a **Jelentés** vászonra – ez létrehoz egy sávdiagramot. Ezután húzza a created\_date mezőt a diagramra, és a Power BI Desktop **Vonaldiagramra** módosítja a vizualizációt.
   
   ![](media/desktop-tutorial-facebook-analytics/19.png)
2. A következő lépésben húzza a **shares** mezőt a **Jelentés vászonra**. Most pedig húzza a **Hour** mezőt a **Tengely** szakaszba a **Mező lista** területen.
   
   ![](media/desktop-tutorial-facebook-analytics/20.png)
3. A vizualizáció típusa a **Vizualizáció** ablaktáblán egy másik ikonra kattintva bármikor módosítható. Az alábbi ábrán a nyíl a **Sávdiagram** ikonra mutat.
   
   ![](media/desktop-tutorial-facebook-analytics/21.png)
4. Módosítsa a vizualizáció típusát **Sávdiagramra**.
5. Létrejön a **Sávdiagram**, a tengely azonban nem az, amit szeretnénk – mi a másik irányban szeretnénk sorba rendezni (a magasabb értékektől az alacsonyabbakig). Az **Y tengely** melletti lefelé mutató nyílra kattintva bontsa ki az adott szakaszt. A tengely típusát módosítanunk kell **Folytonos** típusról **Kategorikus** típusra, hogy úgy lehessen rendezni, ahogy szeretnénk (az alábbi képen a tengely még a beállítás előtt látható – az azt követő kép mutatja a kívánt állapotot).

![](media/desktop-tutorial-facebook-analytics/22.png)

Mindjárt jobb is. És most már három vizualizációval rendelkezünk ezen az oldalon, amelyeket igény szerint átméretezhetünk a jelentésoldal kitöltése érdekében.

![](media/desktop-tutorial-facebook-analytics/23.png)

Amint láthatja, a jelentésekhez könnyen készíthetőek vizualizációk, így tetszőleges módon lehet bemutatni az adatokat. A Power BI Desktop teljes körű szolgáltatást nyújt, lehetővé téve az adatok számos különféle adatforrásból való beszerzését, az elemzési igényeknek megfelelő átalakítását, valamint a látványos és interaktív módon történő megjelenítését. Miután elkészült a jelentés, [felöltheti azt a Power BI-ba](desktop-upload-desktop-files.md), és létrehozhat azon alapuló irányítópultokat, amelyeket más Power BI-felhasználókkal meg is oszthat.

Az oktatóanyag végeredményét [innen](http://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/FacebookAnalytics.pbix) töltheti le

### <a name="where-else-can-i-get-more-information"></a>Hol olvashatok további információkat?
* [Olvassa el a többi Power BI Desktop oktatóanyagot](http://go.microsoft.com/fwlink/?LinkID=521937)
* [Tekintse meg a Power BI Desktop videóit](http://go.microsoft.com/fwlink/?LinkID=519322)
* [Látogasson el a Power BI fórumára](http://go.microsoft.com/fwlink/?LinkID=519326)
* [Látogasson el a Power BI blogra](http://go.microsoft.com/fwlink/?LinkID=519327)



