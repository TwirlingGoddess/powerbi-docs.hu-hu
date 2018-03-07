---
title: "Adatok formázása és összevonása a Power BI Desktopban"
description: "Adatok formázása és összevonása a Power BI Desktopban"
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
ms.date: 01/30/2018
ms.author: davidi
LocalizationGroup: Transform and shape data
ms.openlocfilehash: c8f2419ae2898a59907763392eb86b4877b4fd75
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="shape-and-combine-data-in-power-bi-desktop"></a>Adatok formázása és összevonása a Power BI Desktopban
A **Power BI Desktoppal** számos különféle típusú adatforráshoz csatlakozhat, és igény szerint formázhatja az adatokat. A *formázás* az adatok átalakítását jelenti, például oszlopok vagy táblázatok átnevezését, szöveg számokká alakítását, sorok eltávolítását, az első sorok fejléccé alakítását stb. Az adatok *összevonásakor* két vagy több adatforráshoz csatlakozik, amelyeket igény szerint formázhat, majd egyetlen, hasznos lekérdezéssé vonhat össze.

Ez a dokumentum bemutatja, hogyan lehet lekérdezéseket formázni a Power BI Desktoppal, kiemelve a leggyakoribb feladatokat. Az itt használt lekérdezés részletesebb leírását – például teljesen új lekérdezés létrehozásának lépéseit – az [Első lépések a Power BI Desktopban](desktop-getting-started.md) című témakörben találja.

Érdemes tudni, hogy a Power BI Desktop **Lekérdezésszerkesztőjében** a funkciók a menüszalagon és helyi menükben is elérhetőek. Az **Átalakítás** menüszalag elemeinek nagy része egy adott elemre (például oszlopra) a jobb gombbal kattintva megjelenő menüből is elérhető.

## <a name="shape-data"></a>Adatok formázása
Amikor a Lekérdezésszerkesztőben formázza az adatokat, részletes utasításokat ad meg a Lekérdezésszerkesztő számára, hogy az milyen módosításokat végezzen az adatok betöltésekor és megjelenítésekor. Az eredeti adatforrást nem érintik a változtatások, csak az adatok adott nézete lesz módosítva vagy *formázva*.

A megadott lépéseket (például tábla átnevezése, adattípus átalakítása vagy oszlopok törlése) a Lekérdezésszerkesztő rögzíti, és minden alkalommal végrehajtja, amikor a lekérdezés csatlakozik az adatforráshoz, hogy az adatok mindig a meghatározott formázással jelenjenek meg. Ez a folyamat minden alkalommal végbemegy, amikor a Power BI Desktop Lekérdezésszerkesztő funkcióját használja, valamint akkor is, ha egy másik felhasználó elindít egy megosztott lekérdezést, például a **Power BI** szolgáltatásban. A lépések a megadott sorrendben rögzítve lesznek a **Lekérdezés beállításai** panel **Alkalmazott lépések** területén.

Az alábbi képen egy formázott lekérdezés **Lekérdezés beállításai** panelje látható – az egyes lépések részletes leírását a következő bekezdésekben találhatja meg.

![](media/desktop-shape-and-combine-data/shapecombine_querysettingsfinished.png)

Használjuk az [Első lépések a Power BI Desktopban](https://powerbi.uservoice.com/knowledgebase/articles/471664) témakörben található, nyugdíjba vonulással kapcsolatos adatokat, amelyeket egy webes adatforráshoz csatlakozva találtunk meg. Formáljuk ezeket az adatokat az igényeink szerint.

Először is láthatjuk, hogy amikor a Lekérdezésszerkesztő betöltötte a táblázatot, egy oszlop értékei nem lettek automatikusan átalakítva szövegből számmá. Márpedig nekünk számokra van szükségünk. Ez nem jelent problémát. Csak kattintson a jobb gombbal az oszlop fejlécére, és válassza a **Típus módosítása \> Egész szám** lehetőséget a módosításukhoz. Ha egynél több oszlopot szeretne kijelölni, először jelöljön ki egy oszlopot, majd a **SHIFT** billentyűt lenyomva tartva jelölje ki a szomszédos oszlopokat, és kattintson a jobb gombbal az összes kijelölt oszlop módosításához. A **CTRL** billentyűvel nem szomszédos oszlopokat is kijelölhet.

![](media/desktop-shape-and-combine-data/shapecombine_changetype.png)

Az oszlopokat szövegből fejléccé is *átalakíthatja* az **Átalakítás** menüszalagon. A képen az **Átalakítás** menüszalag látható. A nyíl az **Adattípus** gombra mutat, amellyel az adott adattípust egy másikká alakíthatja.

![](media/desktop-shape-and-combine-data/queryoverview_transformribbonarrow.png)

Vegye figyelembe, hogy a **Lekérdezés beállításai** panel **Alkalmazott lépések** területén minden végrehajtott adatformázási lépés megjelenik. Ha el szeretne távolítani egy lépést a formázási folyamatból, egyszerűen csak kattintson az adott lépés bal oldalán található **X** jelre. Az alábbi képen az **Alkalmazott lépések** listában láthatók az eddigi lépések: csatlakozás a webhelyhez (**Forrás**), tábla kiválasztása (**Navigálás**). Emellett a Lekérdezésszerkesztő a táblázat betöltésekor automatikusan megváltoztatta a szövegalapú számoszlopok adattípusát *Szövegről* *Egész számra* (**Típus módosítva**). Egy rangsorolást tartalmazó oszlopnál nem módosult a típus automatikusan számalapúra. Ennek oka a következő néhány bekezdésben kiderül.

![](media/desktop-shape-and-combine-data/shapecombine_appliedstepsearly.png)

Mielőtt használhatnánk a lekérdezést, végre kell hajtanunk néhány változtatást, hogy az adatok az igényeink szerint a helyükre kerülhessenek:

* *Az első oszlop eltávolítása*: nincs rá szükségünk, mivel csak redundáns sorokból áll, amelyekben a „Check out how your state ranks for retirement” szöveg olvasható. Ennek az az oka, hogy az adatforrás egy webes táblázat.
* *Néhány hiba javítása*: a **Health care quality** nevű oszlop egyező értéket is tartalmaz az államok rangsorolására vonatkozóan. Ezek az egyező értékek a webhelyen a számértéket követő *(tie)* szöveggel voltak jelölve. Ez a webhelyen jól működik, viszont emiatt manuálisan kell átalakítanunk az oszlop típusát szövegből adat típusúvá. A Power BI Desktop könnyű megoldást kínál erre, a folyamat során pedig megismerkedhetünk a lekérdezésben az **Alkalmazott lépések** egy hasznos funkciójával.
* *Táblázatnév megváltoztatása*: a **Table 0** nem túl hasznos leíró név, de könnyű megváltoztatni.

Az első oszlop eltávolításához egyszerűen jelölje ki az adott oszlopot, és válassza a menüszalagon a **Kezdőlap** fület, majd az **Oszlopok eltávolítása** lehetőséget, ahogyan az az alábbi képen látható.

![](media/desktop-shape-and-combine-data/shapecombine_removecolumnsretirement.png)

Következő lépésként a szöveges oszlopot kell számokká alakítanunk. Első ránézésre egyszerűnek tűnik, hiszen csak módosítanunk kell a **Health care quality** oszlop típusát számra (például *Egész szám* vagy *Tizedes tört*). Azonban ha átállítjuk a típust **Szöveg** értékről **Egész szám** értékre, és áttekintjük az oszlopban szereplő értékeket, láthatjuk, hogy a Lekérdezésszerkesztő néhány hibát jelentett.

![](media/desktop-shape-and-combine-data/shapecombine_error.png)

Íme néhány módszer, amellyel további információt tudhatunk meg az egyes hibákról. Kijelölheti az adott cellát (anélkül, hogy a **Hiba** szóra kattintana), vagy közvetlenül a **Hiba** szóra is kattinthat. Ha úgy jelöli ki a cellát, hogy *nem* kattint közvetlenül a **Hiba** szóra, a Lekérdezésszerkesztő az ablak alsó részében megjeleníti a hibával kapcsolatos információkat.

![](media/desktop-shape-and-combine-data/shapecombine_errorinfo.png)

Ha közvetlenül a *Hiba* szóra kattint, a lekérdezés egy **alkalmazott lépést** hoz létre a **Lekérdezés beállításai** panelen, és megjeleníti a hibával kapcsolatos információkat.

![](media/desktop-shape-and-combine-data/shapecombine_errorselect.png)

A Lekérdezésszerkesztőbe való visszatéréshez el kell távolítania ezt a lépést a mellette lévő **X** jelre kattintva.

Ha kiválasztjuk a legutolsó **alkalmazott lépést**, csak a hiba leírása jelenik meg, ahogyan az az alábbi képen látható.

![](media/desktop-shape-and-combine-data/shapecombine_querystep1.png)

Mivel a Lekérdezésszerkesztő sorrendben rögzíti a lépéseket, az **Alkalmazott lépések** területen kiválaszthatjuk a típusmódosítás előtti lépést, hogy megtudjuk, mi volt a cella átalakítás előtti értéke, ahogyan az az alábbi képen látható.

![](media/desktop-shape-and-combine-data/shapecombine_querystep2.png)

Így már kijavíthatjuk az értékeket, *ezután* pedig módosíthatjuk a típust. Mivel a Lekérdezésszerkesztő sorrendben, de egymástól függetlenül rögzíti a lépéseket, lehetősége van minden **alkalmazott lépést** feljebb vagy lejjebb mozgatni a sorrendben. Kattintson a jobb gombbal bármelyik lépésre. Ekkor a Lekérdezésszerkesztő megjelenít egy menüt, amelyben a következő lehetőségek közül választhat: **Átnevezés**, **Törlés**, **Összes** **további törlése** (az adott lépés és az utána következő összes lépés eltávolítása), **Feljebb** vagy **Lejjebb**.

![](media/desktop-shape-and-combine-data/shapecombine_querystepreorder.png)

Továbbá kiválaszthat egy **alkalmazott lépést** bárhol a listában, és onnantól folytathatja az adatok formázását. A Lekérdezésszerkesztő automatikusan beszúr egy új lépést közvetlenül a kiválasztott **alkalmazott lépés** után. Próbáljuk is ki.

Először kiválasztjuk az **alkalmazott lépést**, a **Health care quality** oszlop típusának módosítása előtt. Ezután lecseréljük azokat az értékeket, amelyek esetében a „(tie)” szöveg is szerepel a cellában úgy, hogy csak a szám maradjon. Kattintson a jobb gombbal arra a cellára, amely a „35 (tie)” szöveget tartalmazza, majd a megjelenő menüből válassza az *Értékek lecserélése...* lehetőséget. Jegyezze meg, melyik **alkalmazott lépés** van kijelölve (a típus módosítása előtti lépés).

![](media/desktop-shape-and-combine-data/shapecombine_replacevalues.png)

Mivel be szeretnénk szúrni egy lépést, a Lekérdezésszerkesztő figyelmeztet ennek veszélyeire: az ezt követő lépések a lekérdezés meghibásodását okozhatják. Ezért óvatosan kell eljárnunk. Mivel ez egy útmutató, amelynek célja, hogy bemutassa lépések létrehozását, törlését, beszúrását és étrendezését a Lekérdezésszerkesztőben, folytatjuk tovább, és kiválasztjuk a **Beszúrás** lehetőséget.

![](media/desktop-shape-and-combine-data/shapecombine_insertstep.png)

Háromszor szerepel „tie” érték az oszlopban, ezért mindegyiket lecseréljük. Amikor új alkalmazott lépést hoz létre, a Lekérdezésszerkesztő a művelet alapján nevezi el. Ebben az esetben az **Érték felülírva** nevet kapja. Ha több azonos nevű lépés szerepel a lekérdezésben, a Lekérdezésszerkesztő (egymást követő) sorszámozással tesz különbséget az **alkalmazott lépések** között.

A következő képen három **Érték felülírva** lépés látható a **Lekérdezés beállításai** panelen, ám még egy érdekes dolgot is mutat: mivel eltávolítottuk a „(tie)” szöveg összes példányát a **Health care quality** oszlopból, a **Típus módosítva** lépés most már *hiba nélkül* befejeződik.

![](media/desktop-shape-and-combine-data/shapecombine_replacedvaluesok.png)

> [!NOTE]
> Lehetősége van a **Hibák eltávolítása** művelet elvégzésére is (a menüszalagon vagy a helyi menüben), ami minden hibát tartalmazó sort eltávolít. Ebben az esetben a művelet minden olyan államot eltávolított volna az adataink közül, amelyben a „*(tie)*” szöveg szerepel, ezt pedig szeretnénk elkerülni. Azt szeretnénk, hogy mindegyik állam szerepeljen a táblázatban.

Ez talán kicsit összetett, azonban jól mutatja, hogy a Lekérdezésszerkesztő milyen hatékony és sokoldalú eszköz.

Utolsó lépésként módosítsuk a táblázat nevét egy leíró névre. Amikor nekilátunk jelentések készítésének, nagyon hasznos, ha a táblázatok neve jól leírja azok tartalmát. Ez főleg abban az esetben igaz, ha egyszerre több adatforráshoz csatlakozunk, és a táblázatok listája megjelenik a **Jelentés** nézet **Mezők** panelében.

A táblázat neve egyszerűen módosítható: a **Lekérdezés beállításai** panel **Tulajdonságok** területén gépelje be a tábla új nevét, ahogyan az a lenti képen látható, majd nyomja le az **Enter** billentyűt. Adjuk a táblázatnak a *RetirementStats* nevet.

![](media/desktop-shape-and-combine-data/shapecombine_renametable.png)

Most már az adatok formázása olyan, amilyet szerettünk volna. Csatlakozzunk egy másik adatforráshoz, és vonjuk össze az adatokat.

## <a name="combine-data"></a>Adatok összevonása
Érdekes adataink vannak az egyes államokról, amelyeknek még hasznát fogjuk venni újabb elemzések és lekérdezések készítésekor. Ám van egy probléma: a legtöbb helyen az államok a kétbetűs rövidítésükkel szerepelnek, nem a teljes nevükkel. Valahogyan össze kell párosítanunk tehát a neveket a rövidítésekkel.

Szerencsére létezik egy másik nyilvános adatforrás, amely pontosan erre használható. Azonban jelentős formázást kell rajta végrehajtanunk, hogy csatlakoztathassuk a nyugdíjba vonulással kapcsolatos adatokat tartalmazó táblázatunkhoz. Az államok rövidítéseit tartalmazó webes erőforrás a következő címen található:

<http://en.wikipedia.org/wiki/List_of_U.S._state_abbreviations>

A Lekérdezésszerkesztő **Kezdőlap** menüszalagján válasszuk az **Új forrás \> Web** lehetőséget, írjuk be a webcímet, és kattintsunk az OK gombra. A Kezelőben ekkor megjelenik a webhelyen talált tartalom.

 ![](media/desktop-shape-and-combine-data/designer_gsg_usstateabbreviationsnavigator.png)

Válasszuk a **Table[edit]** elemet, mert az tartalmazza a kívánt adatokat. Azonban jelentős formázásra lesz szükség ahhoz, hogy a táblázat tartalma a számunkra fontos adatokra korlátozódjon.

> [!TIP]
> Létezik egyszerűbb módja az alábbi lépések végrehajtásának? Igen, létrehozhatunk egy *kapcsolatot* a két táblázat között, és ez alapján is formázhatjuk az adatokat. A következő lépések hasznosak, hiszen a segítségükkel megismerheti a táblázatok kezelését, de érdemes tudni, hogy a kapcsolatok segítségével gyorsan felhasználhat több táblázatból származó adatokat.
> 
> 

Az adatok formázásához hajtsuk végre a következő lépéseket:

* Távolítsa el az első két sort. Ezek a webhelyen létrehozott táblázat maradványai, és nincs szükségünk rájuk. A **Kezdőlap** menüszalagról válassza a **Sorok számának csökkentése \> Sorok eltávolítása \> Legelső sorok eltávolítása** lehetőséget.

![](media/desktop-shape-and-combine-data/shapecombine_removetoprows.png)

Ekkor megjelenik a **Legelső sorok eltávolítása** ablak, amelyben megadhatja a törölni kívánt sorok számát.

* Távolítsa el az alsó 26 sort. Ezek olyan területeket tartalmaznak, amelyekre nincs szükségünk. A **Kezdőlap** menüszalagról válassza a **Sorok számának csökkentése \> Sorok eltávolítása \> Utolsó sorok eltávolítása** lehetőséget.

![](media/desktop-shape-and-combine-data/shapecombine_removebottomrows.png)

* Mivel a RetirementStats táblázat nem tartalmaz adatokat Washington államról, ezt az államot ki kell szűrnünk a listánkból. A Region Status oszlop melletti legördülő nyílra kattintva törölje a jelölést a **Federal district** melletti jelölőnégyzetből.

![](media/desktop-shape-and-combine-data/shapecombine_filterdc.png)

* Távolítson el néhány felesleges oszlopot. Most csak az államneveknek a hivatalos kétbetűs rövidítésükre való leképezésére van szükségünk, így a következő oszlopokat törölhetjük: **Column2**, **Column3**, majd a **Column5** oszloptól a **Column10** oszlopig az összes oszlopot. Először jelölje ki a Column2 oszlopot, majd a **CTRL** billentyű lenyomva tartása mellett jelölje ki a többi eltávolítandó oszlopot (így egyszerre több, nem egymás melletti oszlopot is kiválaszthat). A menüszalag Kezdőlap területéről válassza az **Oszlopok eltávolítása \> Oszlopok eltávolítása** lehetőséget.

![](media/desktop-shape-and-combine-data/shapecombine_removecolumns.png)

* Alakítsa az első sort fejléccé. Mivel eltávolítottuk az első három sort, a jelenlegi legfelső sort szeretnék fejlécként használni. Válassza az **Első sor használata fejlécként** lehetőséget a **Kezdőlap** fülről vagy a menüszalag **Átalakítás** területéről.

![](media/desktop-shape-and-combine-data/shapecombine_usefirstrowasheaders.png)

>[!NOTE]
>Itt érdemes megemlíteni, hogy a Lekérdezésszerkesztőben az alkalmazott lépések *sorrendje* fontos, mert meghatározhatja, hogyan lesznek formázva az adatok. Érdemes azt is megfontolni, hogy egy adott lépés hogyan befolyásolhatja a soron következő lépéseket. Ha az Alkalmazott lépések közül eltávolít egy lépést, lehetséges, hogy a lekérdezés lépéseinek sorrendjéből adódóan a következő lépések nem úgy fognak működni, ahogyan eredetileg tervezte.

>[!NOTE]
>Ha átméretezi a Lekérdezésszerkesztő ablakát, például csökkenti a szélességét, a menüszalag egyes elemei összecsukódnak a látható terület legjobb kihasználása érdekében. Ha növeli a Lekérdezésszerkesztő ablakának szélességét, a menüszalag elemei kibomlanak, hogy a lehető legjobban kihasználják a nagyobb menüszalag területét.

* Nevezze át az oszlopokat és magát a táblázatot. Az oszlopok többféleképpen is átnevezhetők. Először is válassza ki az oszlopot, majd válassza az **Átnevezés** lehetőséget a menüszalag **Átalakítás** területén, vagy kattintson a jobb gombbal, és válassza az **Átnevezés…** lehetőséget. a megjelenő helyi menüből. Az alábbi képen mindkét lehetőséget nyíl mutatja. Ezek közül elég az egyiket kiválasztania.

![](media/desktop-shape-and-combine-data/shapecombine_rename.png)

Nevezzük át az oszlopokat a következőképpen: *State Name* és *State Code*. A táblázat átnevezéséhez egyszerűen írja be a nevet a **Lekérdezés beállításai** panel **Név** mezőjébe. Adjuk a táblázatnak a *StateCodes* nevet.

Most, hogy a kívánt módon formáztuk StateCodes táblázatot, vonjuk össze a két táblázatot vagy lekérdezést. Mivel a két táblázatunk az adatokon végzett lekérdezéseink eredményei, ezért ezeket gyakran *lekérdezéseknek* nevezzük.

A lekérdezések összevonásának két fő módja van: *egyesítés* és *hozzáfűzés*.

Ha hozzá szeretne adni egy vagy több oszlopot egy másik lekérdezéshez, **egyesítse** a lekérdezéseket. Ha további sorokat szeretne hozzáadni egy meglévő lekérdezéshez, **fűzze őket hozzá** a lekérdezéshez.

Ebben az esetben egyesíteni szeretnénk a lekérdezéseket. Első lépésként a Lekérdezésszerkesztő bal oldali paneljén válassza ki azt a lekérdezést, *amellyel* a másik lekérdezést egyesíteni szeretnénk. Ebben az esetben ez a *RetirementStats*. Ezután válassza az **Összevonás \> Lekérdezések egyesítése** lehetőséget a menüszalag **Kezdőlap** fülén.

![](media/desktop-shape-and-combine-data/shapecombine_mergequeries.png)

A rendszer felkérheti az adatvédelmi szintek beállítására. Ezzel elkerülheti, hogy nem kívánt adatokat jelöljön ki vagy helyezzen át az adatok összevonásakor.

![](media/desktop-shape-and-combine-data/shapecombine_mergequeriesb.png)

Ezután megjelenik az **Egyesítés** ablak, ahol kiválaszthatjuk, melyik táblázatot egyesítjük a már kiválasztott táblázattal, majd kijelölhetjük az egyesítéshez használni kívánt oszlopokat. A *RetirementStats* táblázatból (vagy lekérdezésből) válassza ki a State oszlopot, majd válassza ki a *StateCodes* lekérdezést. (Ebben az esetben egyszerű a választás, hiszen nincs is másik lekérdezés. Ha több adatforráshoz csatlakozik, több lekérdezés közül választhat.) Miután kiválasztottuk a megfelelő egyező oszlopokat (vagyis a **State** oszlopot a *RetirementStats* táblázatból és a **State Name** oszlopot a *StateCodes* táblázatból), az **Egyesítés** ablak az alábbi képen látható módon néz ki, és az **OK** gomb aktiválódik.

![](media/desktop-shape-and-combine-data/shapecombine_merge.png)

Létrejött egy **NewColumn** nevű oszlop a lekérdezés végén, amely a meglévő lekérdezéssel egyesített táblázat (lekérdezés) adatait tartalmazza. Az egyesített lekérdezés összes oszlopa a **NewColumn** oszlopba lesz sűrítve, de a **Kibontás** lehetőséggel kibonthatja a táblázatot, és tetszőleges oszlopokat adhat hozzá.

![](media/desktop-shape-and-combine-data/shapecombine_mergenewcolumn.png)

Az egyesített táblázat kibontásához és a kívánt oszlopok kiválasztásához kattintson a kibontás ikonra (![Kibontás](media/desktop-shape-and-combine-data/icon.png)). Ekkor megjelenik a **Kibontás** ablak.

![](media/desktop-shape-and-combine-data/shapecombine_mergeexpand.png)

Ebben az esetben kizárólag a **State Code** oszlopra van szükségünk, ezért csak ezt választjuk ki, majd az **OK** gombra kattintunk. Töröljük az Eredeti oszlopnév használata előtagként melletti négyzet jelölését, mert nincs szükségünk rá. Ha bejelölve hagyjuk ezt a négyzetet, az egyesített oszlop neve **NewColumn.State Code** lesz (az eredeti oszlopnév, vagyis a **NewColumn**, amelyet egy pont követ, majd a lekérdezéshez adni kívánt oszlop neve).

>[!NOTE]
>Szeretné kipróbálni, milyen további módokon adhatja a **NewColumn** oszlopot a táblázathoz? Nyugodtan kísérletezhet, és ha nem a kívánt eredményt kapja, egyszerűen törölje az adott lépést a **Lekérdezés beállításai** panel **Alkalmazott lépések** listájából. Ekkor a lekérdezés visszatér a **Kibontás** lépés alkalmazása előtti állapotra. Tetszőleges számú alkalommal próbálkozhat, amíg a kibontási folyamattal a kívánt eredményt nem éri el.

Most egyetlen lekérdezésünk (táblázatunk) van, amelyet két, igényeink szerint formázott adatforrás összevonásával hoztunk létre. Ez a lekérdezés alapul szolgálhat számos más érdekes adatkapcsolathoz, például az államokra lebontott lakhatási költségek statisztikái, demográfiai adatok vagy munkalehetőségek megjelenítéséhez.

A módosítások mentéséhez és a Lekérdezésszerkesztő bezárásához a menüszalag **Kezdőlap** fülén kattintson a Bezárás és alkalmazás elemre. Az átalakított adatkészlet ezután megjelenik a Power BI Desktopban, és elérhető jelentések készítéséhez.

![](media/desktop-shape-and-combine-data/shapecombine_closeandapply.png)

## <a name="next-steps"></a>Következő lépések
A Power BI Desktop műveletek és lehetőségek széles tárházát tartalmazza. A program képességeivel kapcsolatos további információkért lásd az alábbi forrásanyagokat:

* [Első lépések a Power BI Desktopban](desktop-getting-started.md)
* [Lekérdezések áttekintése a Power BI Desktopban](desktop-query-overview.md)
* [Adatforrások a Power BI Desktopban](desktop-data-sources.md)
* [Csatlakozás adatokhoz a Power BI Desktopban](desktop-connect-to-data.md)
* [Gyakori lekérdezési feladatok a Power BI Desktopban](desktop-common-query-tasks.md)   

