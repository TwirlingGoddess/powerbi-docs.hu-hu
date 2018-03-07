---
title: "Oktatóanyag: Weboldalakról származó adatok importálása és elemzése a Power BI Desktop használatával"
description: "Oktatóanyag: Weboldalakról származó adatok importálása és elemzése a Power BI Desktop használatával"
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
ms.openlocfilehash: 9650f0be6ca795fdea3395721c0eb02e80464821
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="analyzing-web-page-data-using-power-bi-desktop-tutorial"></a>Weboldalakról származó adatok elemzése a Power BI Desktop használatával (oktatóanyag)
Ez az oktatóanyag bemutatja, hogyan importálhat egy adatokból álló táblázatot egy weboldalról, majd hogyan hozhat létre egy jelentést az adatok vizualizációjához. A folyamat részeként a weboldalon elérhető táblázatok között kell navigálnia, és át kell alakítania az adatokat egy új formátumba.

 A cikk tartalma:

* **1. feladat:** Kapcsolódás egy webes adatforráshoz
* **2. feladat:** Adatok formázása a Lekérdezés nézetben
  * 1. lépés: Az egyéb oszlopok eltávolítása, hogy csak a lényeges oszlopok jelenjenek meg
  * 2. lépés: A kijelölt oszlop értékeinek megtisztítása az értékek cseréjével
  * 3. lépés: Oszlop értékeinek szűrése
  * 4. lépés: Oszlop átnevezése
  * 5. lépés: Nullértékek kiszűrése az oszlopból
  * 6. lépés: Lekérdezés átnevezése
  * A lekérdezéshez létrehozott lépések
* **3. feladat:** Vizualizáció létrehozása a Jelentés nézettel
  * 1. lépés: Lekérdezés betöltése a jelentésbe
  * 2. lépés: Térkép vizualizáció létrehozása

## <a name="task-1-connect-to-a-web-data-source"></a>1. feladat: Kapcsolódás egy webes adatforráshoz
 Az 1. feladat keretében a Bajnoksági összefoglaló táblázatot importálja az UEFA labdarúgó Európa-bajnokság Wikipédia-oldaláról, a következő címről: https://hu.wikipedia.org/wiki/\_Labdarúgó-\_Európa-\_bajnokság

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage1.png)

### <a name="add-a-wikipedia-page-data-source"></a>Wikipédia-oldal adatforrásként történő hozzáadása
1. Az **Első lépések** párbeszédpanelen vagy a **Kezdőlap** szalagfülön válassza az **Adatok lekérése** lehetőséget.
2. Ezzel megnyitja az **Adatok lekérése** párbeszédpanelt, ahol számos adatforrás közül választhat, amelyekből adatokat importálhat a Power BI Desktopba. Ezúttal a **Web** lehetőséget választjuk, amely az **Összes** vagy az **Egyéb** csoportban található meg.
3. A **Webes tartalom** párbeszédpanel **URL** szövegmezőjébe illessze be a Wikipédia-oldal URL-címét (https://hu.wikipedia.org/wiki/\_Labdarúgó-\_Európa-\_bajnokság).
4. Kattintson az **OK** gombra.

Miután sikerült kapcsolatot létesíteni a weboldallal, a **Kezelő** párbeszédpanelen tekintse meg a Wikipédia-oldalon elérhető táblázatok listáját. Az egyes táblázatokra kattintva megtekintheti azok előnézetét.

A **Kezelő** bal oldali ablaktábláján válassza az **Eredmények[szerkesztés]** táblázatot a bajnoksági összefoglaló eredményeinek megjelenítéséhez, vagy válassza az **Eredmények[szerkesztés]** táblázatot, majd a **Szerkesztés** parancsot. Ez lehetővé teszi a táblázatban található adatok átalakítását a jelentésbe történő importálás előtt, mivel az adatok nem az elemzéshez szükséges formátumban vannak.

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/tutorialimanaly_navigator.png)

Ezzel megjeleníti a táblázat előnézetét a Lekérdezés nézetben, ahol a megfelelő átalakítási lépésekkel megtisztíthatjuk az adatokat.

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage3.png)

## <a name="task-2-shape-data-in-the-subject-table"></a>2. feladat: Adatok formázása az érintett táblázatban
Most, hogy kijelölte az érintett táblázatot az adatlekérdezésben, bemutatjuk, hogyan hajthat végre különböző adatátalakítási és adattisztítási műveleteket.

**1. lépés:** Az egyéb oszlopok eltávolítása, hogy csak a lényeges oszlopok jelenjenek meg

Ebben a lépésben eltávolítunk minden oszlopot, az **Év** és a **Döntő győztesei** kivételével.

1. A **Lekérdezés előnézete** rácson válassza ki az **Év** és a **Döntő győztesei** oszlopot (**CTRL** + **kattintással**).
2. Kattintson a jobb gombbal egy oszlopfejlécre a **Lekérdezés előnézete** rácson, majd kattintson a **További oszlopok eltávolítása** parancsra a ki nem jelölt oszlopok eltávolításához. Ez a művelet elérhető a **Kezdőlap** szalagfülről is, az **Oszlopok kezelése** csoportban.

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage4.png)

**2. lépés:** A kijelölt oszlop értékeinek megtisztítása az értékek cseréjével

Ebben a lépésben az **Év** oszlop Részletek utótagját cseréli le. Figyelje meg, hogy ez az utótag egy új sorban található, ezért nem jelenik meg a táblázat előnézetében. Ugyanakkor, ha az Év oszlop egyik numerikus értéket tartalmazó cellájára kattint, a részletes nézetben a teljes érték látható lesz.

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage5.png)

1. Jelölje ki az **Év** oszlopot.
2. A **Lekérdezés nézet** szalagon kattintson a **Kezdőlap** fül **Értékek lecserélése** elemére, majd kattintson a jobb gombbal az **Év** oszlopra, és kattintson az **Értékek lecserélése** parancsra, hogy a Részletek helyére üres szöveg kerüljön.
3. Az **Értékek lecserélése** párbeszédpanelen írja be a Részletek szöveget a **Keresendő érték** szövegmezőbe, és hagyja üresen a **Csere a következőre** szövegmezőt üresen.
4. Kattintson az **OK** gombra.

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage6.png)

 **3. lépés:** Oszlop értékeinek szűrése

Ebben a lépésben szűrni fogjuk az **Év** oszlop értékeit, hogy ne jelenjenek meg az „Év” szöveget tartalmazó sorok.

1. Kattintson a szűrő listanyílra az **Év** oszlopban.
2. A **Szűrés** legördülő listában törölje az **Év** elem jelölését.
3. Kattintson az **OK** gombra.

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage7.png)

**4. lépés:** Oszlop átnevezése

Most, hogy sikerült megtisztítani az **Év** oszlop adatait, rátérhetünk a **Döntő győztesei** oszlopra.

Mivel kizárólag a győztesek listáját szeretnénk megkapni, átnevezhetjük az oszlopot „**Ország**”-ra.

1. Válassza ki a **Döntő győztesei** oszlopot a Lekérdezés előnézetben.
2. A **Lekérdezés nézet** szalag **Átalakítás** fülének **Minden oszlop** csoportjában kattintson az **Átnevezés** parancsra.
3. Ezzel szerkeszthetővé teszi az oszlop nevét. Nevezzük át az oszlopot az **Ország** névre.

**5. lépés:** Nullértékek kiszűrése az oszlopból

Ezután ki kell szűrnünk a nullértékeket az **Ország** oszlopból. Ezt megtehetjük a Szűrés menün keresztül a 3. lépésben látott módon, de elérhető egy másik megoldás is:

1. Kattintson a jobb gombbal az **Ország** oszlop valamelyik cellájára, amely nullértéket tartalmaz.
2. A helyi menüben jelölje be a **Szövegszűrők –\> nem egyenlő** elemet.
3. Ezzel egy új szűrési lépést hoz létre, amellyel eltávolítja a nullértéket tartalmazó sorokat az **Ország** oszlopból.

**6. lépés:** Lekérdezés elnevezése

Ebben a lépésben a végső lekérdezésnek az **Európa-kupa győztesei** nevet adjuk.

1. A **Lekérdezési beállítások** ablaktábla **Név** szövegmezőjébe írja be az **Európa-kupa győztesei** szöveget.
   
   ![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage8.png)

## <a name="task-3-create-visualizations-using-the-report-view"></a>3. feladat: Vizualizáció létrehozása a Jelentés nézettel
Most, miután sikerült az adatokat az elemzéshez szükséges formába átalakítani, az eredményül kapott táblázatot betölthetjük a jelentésünkbe, és vizualizációkat hozhatunk létre.

**1. lépés:** A lekérdezés betöltése a jelentésbe

Ahhoz, hogy betölthessük a lekérdezés eredményeit a Power BI Desktopba, és létrehozhassunk egy jelentést, a **Kezdőlap** szalagon kattintson a **Bezárás és betöltés** elemre.

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage9.png)

Ezzel elindítja a lekérdezés értékelését, és betölti a táblázatos kimenetet a jelentésbe. A Power BI Desktopban válassza ki a **Jelentés** ikont, hogy a Power BI Desktop látható legyen a Jelentés nézetben.

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage10.png)

Az így kapott táblázatmezők a **Jelentés nézet** jobb oldalán, a **Mezők ablaktáblán** jelennek meg.

![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage11.png)

**2. lépés:** Térkép vizualizáció létrehozása

Vizualizációk létrehozásához áthúzhatjuk a mezőket a **Mező listából** a **Jelentés vászonra**.

1. Húzza az **Ország** mezőt a **Jelentés vászonra**. Ezzel létrehozza a vizualizációt a **Jelentés vásznon**. Ebben az esetben, mivel országok listájáról van szó, egy **Térkép vizualizációt** kapunk.
   
   ![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage12.png)
2. A **Vizualizáció** panel egy másik ikonjára kattintva bármikor módosítható a vizualizáció típusa.
   
   ![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage13.png)
3. Mi maradunk a **Térkép** vizualizációs típusnál. A vizualizációt ezenkívül az egyik sarkánál húzva át lehet méretezni a kívánt méretre.
   
   ![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage14.png)
4. Figyelje meg, hogy jelenleg a térképen minden pont ugyanolyan méretű. Azt szeretnénk, hogy ha minél több Európa-kupát nyert az ország, annál nagyobb pont jelenítené meg a térképen. Ehhez húzza át a **Mezők lista** **Év** mezőjét a **Mezők ablaktábla** alsó felében található **Értékek** mezőbe.
   
   ![](media/desktop-tutorial-importing-and-analyzing-data-from-a-web-page/webpage15.png)

Amint láthatja, a jelentésekhez könnyen készíthetők vizualizációk, így tetszőleges módon lehet bemutatni az adatokat. A Power BI Desktop teljes körű szolgáltatást nyújt, lehetővé téve az adatok számos különféle adatforrásból való beszerzését, az elemzési igényeknek megfelelő átalakítását, valamint a látványos és interaktív módon történő megjelenítését. Miután elkészült a jelentés, [felöltheti azt a Power BI-ba](desktop-upload-desktop-files.md), és létrehozhat azon alapuló irányítópultokat, amelyeket más Power BI-felhasználókkal meg is oszthat.

Ezzel az **adatok webes forrásból történő importálását** ismertető oktatóanyag végéhez is ért. Az elkészült Power BI Desktop-fájlt [innen](http://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Analyzing_Data_From_The_Web.pbix) töltheti le.

## <a name="where-else-can-i-get-more-information"></a>Hol olvashatok további információkat?
* [Olvassa el a többi Power BI Desktop-oktatóanyagot](http://go.microsoft.com/fwlink/?LinkID=521937)
* [Tekintse meg a Power BI Desktop videóit](http://go.microsoft.com/fwlink/?LinkID=519322)
* [Látogasson el a Power BI fórumára](http://go.microsoft.com/fwlink/?LinkID=519326)
* [Látogasson el a Power BI blogra](http://go.microsoft.com/fwlink/?LinkID=519327)

