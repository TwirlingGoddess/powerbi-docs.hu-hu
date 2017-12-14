---
title: "Power BI – Alapfogalmak"
description: "Power BI – Alapfogalmak"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: B2vd4MQrz4M
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: get-started-article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 05/31/2017
ms.author: mihart
ms.openlocfilehash: f20ea18fb46928bf7533caacf55a0cdb3d761571
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="power-bi---basic-concepts-for-power-bi-service"></a>Power BI – a Power BI szolgáltatás alapfogalmai
<!-- Shared newnav Include -->
[!INCLUDE [newnavbydefault](./includes/newnavbydefault.md)]

Ez a cikk feltételezi, hogy már [regisztrált a Power BI szolgáltatásra](service-self-service-signup-for-power-bi.md), és [hozzáadott adatokat](service-get-data.md).

A Power BI szolgáltatás megnyitásakor egy ***irányítópult*** jelenik meg. Az irányítópult megkülönbözteti a Power BI szolgáltatást a Power BI Desktoptól.

![](media/service-basic-concepts/completenewer.png)

A Power BI szolgáltatás felhasználói felületének főbb elemei:

1. Navigációs sáv
2. Csempéket tartalmazó irányítópult
3. Q&A kérdésmező
4. Súgó és visszajelzés gomb
5. Az irányítópult címe
6. Az Office 365 appindítója
7. A Power BI kezdőlapjának gombja
8. További irányítópult-műveletek

Ezeket később részletesen is ismertetjük, de először vegyük sorra a Power BI néhány alapfogalmát.

De meg is nézheti ezt a videót, mielőtt tovább olvassa a cikket.  A videóban Will ismerteti az alapfogalmakat, és végigvezeti a Power BI szolgáltatáson.

<iframe width="560" height="315" src="https://www.youtube.com/embed/B2vd4MQrz4M" frameborder="0" allowfullscreen></iframe>


## <a name="power-bi-concepts"></a>A Power BI alapfogalmai
A Power BI a következő három alapvető összetevőre épül: ***irányítópultok***, ***jelentések*** és ***adatkészletek***. Adatok nélkül nem lehetnek sem irányítópultjai, sem jelentései (illetve lehetnek üres irányítópultjai és jelentései, de amíg adatok nem kerülnek beléjük, nincs sok hasznuk), tehát ismerje meg először az **adatkészleteket**.

## <a name="datasets"></a>Adatkészletek
Az *adatkészlet* olyan adatok gyűjteménye, amelyeket *importál*, vagy amelyekhez *csatlakozik*. A Power BI sokféle adatkészlet importálását, csatlakoztatását és egy helyen történő megjelenítését teszi lehetővé.  

Az importált és a csatlakoztatott adatkészletek a navigációs sáv **Adatkészletek** fejléce alatt jelennek meg. Mindegyik itt megnevezett adatkészlet egyetlen adatforrásnak felel meg, például egy OneDrive-beli Excel-munkafüzetnek, egy helyszíni táblázatos SSAS-adatkészletnek vagy egy Salesforce-adatkészletnek. Sok különböző adatforrást támogatunk, a számuk egyre növekszik. [Itt megtekintheti a Power BI-jal használható adatkészlettípusok listáját](service-get-data.md).

**EGY** adatkészlet:

* Újra meg újra felhasználható.
* Több jelentésben is felhasználható.
* Az ebből az egy adatkészletből származó vizualizációkat több irányítópulton is megtekintheti.
  
  ![](media/service-basic-concepts/drawing2.png)

[Adatkészlet importálásához vagy a hozzá való csatlakozáshoz](service-get-data.md) kattintson az **Adatok beolvasása** elemre a navigációs sáv alján, vagy a plusz ikonra az **Adatkészletek** fejlécen. Kövesse az utasításokat az adott forrás importálásához vagy a hozzá való csatlakozáshoz, és adja hozzá az adatkészletet a munkaterületéhez. Az új adatkészletek listája a bal oldali navigációs sávon, sárga csillaggal megjelölve látható. A Power BI-ban végzett munka nem változtatja meg az alapjául szolgáló adatkészletet.

Ha Ön [része egy ***alkalmazás-munkaterületnek***](service-collaborate-power-bi-workspace.md), akkor a munkaterület bármelyik tagja által hozzáadott adatkészletek a többi tag számára is láthatók.

Az adatkészletek frissíthetők, átnevezhetők, elemezhetők, használhatók jelentéskészítésre, valamint eltávolíthatók. Ha elemezni szeretne egy adatkészletet, kattintson rá. Ilyenkor az adatkészletet a jelentésszerkesztőben nyitja meg, ahol mélyre áshat az adatokban, és vizualizációkat hozhat létre belőlük. Ez már továbbvezet a következő témához: a jelentésekhez.

### <a name="dig-deeper"></a>További ismeretek:
* [Mit jelent a Power BI Premium?](service-premium.md)
* [Adatbeolvasás a Power BI szolgáltatásban](service-get-data.md)
* [Power BI számára készült mintaadatkészletek és tartalomcsomagok](sample-datasets.md)

## <a name="reports"></a>Jelentések
A Power BI-jelentések egy vagy több diagramból állnak, és vizualizációkat tartalmaznak (diagramok vagy grafikonok, például vonaldiagram, kördiagram, fatérkép stb. formájában). A vizualizációk másik elnevezése ***vizualizációs elem***. Egyetlen jelentés vizualizációi csak egy adatkészleten alapulhatnak. Jelentések létrehozhatók újonnan a Power BI-n belül, importálhatók a munkatársak által megosztott irányítópultokból, és létrehozhatók olyan adatkészletekhez való csatlakozással, amelyek az Excelből, a Power BI Desktopból, adatbázisokból, SaaS-alkalmazásokból vagy [tartalomcsomagokból](service-organizational-content-pack-introduction.md) származnak.  Ha például csatlakozik egy Power View-lapokat tartalmazó Excel-munkafüzethez, akkor a Power BI elkészít egy jelentést a lapok alapján. Ha pedig SaaS-alkalmazáshoz csatlakozik, a Power BI egy előre elkészített jelentést importál.

A jelentések megtekintésének és használatának két módja van: az [Olvasó nézet](service-report-open-in-reading-view.md) és a [Szerkesztési nézet](service-interact-with-a-report-in-editing-view.md).  A jelentés ***Szerkesztési nézetének*** elemzési, tervezési, kiépítési és megosztási funkcióihoz csak a jelentés készítője, a társtulajdonosok és az erre feljogosított felhasználók férhetnek hozzá. Azok, akikkel ők megosztják a jelentést, az ***Olvasó nézet*** segítségével tanulmányozhatják és használhatják.   

A jelentések listája a navigációs sáv **Jelentések** fejléce alatt látható. A listán szereplő jelentések mind olyan vizualizációkat tartalmaznak egy vagy több oldalon, amelyek a jelentés alapjául szolgáló adatkészleten alapulnak. Ha meg szeretne nyitni egy jelentést, kattintson vagy koppintson rá. Alapértelmezés szerint a jelentés Olvasó nézetben nyílik meg.  A Szerkesztési nézet megnyitásához kattintson a **Jelentés szerkesztése** elemre (ha rendelkezik a szükséges engedélyekkel).  Ha egy megosztott irányítópulton jelentések találhatók, ezek a jelentések NEM láthatók a navigációs sáv listáján. A megosztott jelentéseket közvetlenül a megosztott irányítópultról kell megnyitni, az irányítópult egyik csempéjére kattintva (a csempékről később még szó lesz).

**EGY** jelentés:

* Több irányítópulthoz is társítható (az adott jelentésről rögzített csempék több irányítópulton is megjelenhetnek).
* Egy adatkészletből származó adatokból készíthető el. (Azzal az egy apró kivétellel, hogy a Power BI Desktop több adatkészletet is kombinálhat egy jelentésen belül, amelyet aztán importálni lehet a Power BI-ba.)
  
  ![](media/service-basic-concepts/drawing3new.png)

## <a name="dashboards"></a>Irányítópultok
Az *irányítópultot* Ön hozza létre, vagy egy munkatársa osztja meg Önnel. Egyetlen vászonból áll, amely csempéket és widgeteket tartalmazhat. Minden csempe egyetlen, az irányítópultra rögzített [vizualizációt](power-bi-report-visualizations.md) jelenít meg, amely egy adatkészleten alapul. Sokféleképpen adhat csempét az irányítópulthoz, de ebben az áttekintő témakörben nincs lehetőség ennek bemutatására. További információkért tekintse meg [Az irányítópult csempéi a Power BI szolgáltatásban](service-dashboard-tiles.md) című oldalt. 

A navigációs sávon a „saját” irányítópultjai az **Irányítópultok** fejléc alatt találhatók. A „saját” itt azt jelenti, hogy hozzáfér az irányítópulthoz, de nem feltétlenül Ön hozta létre. Minden irányítópult az alapjául szolgáló adatkészletek valamely részhalmazának egyedi nézetét jeleníti meg.  Ha tulajdonosa az irányítópultnak, hozzáférhet az alapjául szolgáló adatkészletekhez is. Ezek a navigációs sáv **Adatkészletek** fejléce alatt találhatók meg.  Ha az irányítópultot megosztották Önnel, a megosztás ikont ![](media/service-basic-concepts/sharing-icon.png) láthatja mellette, és a megosztás módjától függ, hogy az alapjául szolgáló adatkészletek megjelennek-e a navigációs sávon.

> [!NOTE]
> A rögzítésről és a csempékről részletesebben olvashat „Az irányítópult és a csempék” című részben.
> 
> 

**EGY** irányítópult:

* Több adatkészletből jeleníthet meg vizualizációkat.
* Több jelentésből jeleníthet meg vizualizációkat.
* Más eszközökből (pl. Excel) rögzített vizualizációkat is megjeleníthet.
  
  ![](media/service-basic-concepts/drawing1.png)

### <a name="dig-deeper"></a>További ismeretek:
**Irányítópultot [létrehozhat újonnan](service-dashboard-create.md)** – ekkor egy új, üres irányítópultot épít fel, amelybe aztán betöltheti az adatokat. 

**Ön vagy egy munkatársa létrehozhat egy irányítópultot, majd [megoszthatja](service-share-dashboards.md)** – a meghívó elfogadása után a megosztott irányítópult (minden társított jelentéssel és adatkészlettel együtt) megjelenik a navigációs sávon. Irányítópult megosztásához és a megosztott irányítópult megtekintéséhez egyaránt a Power BI Pro használatára van szükség.

**Előfordul, hogy az irányítópultot és az adatkészletet együtt importálja, vagy akkor jön létre az irányítópult, amikor Ön csatlakozik az adatkészlethez**. A Salesforce-hoz készült **Adatok beolvasása** varázsló például megkérdezi, hogy szeretné-e, ha az adatkészletből irányítópult és/vagy jelentés készülne. 

**Miért hoznak létre a felhasználók irányítópultokat?**  Csak néhány ok a sok közül:

* Azért, hogy egy pillantással átláthassák a döntéshozatalhoz szükséges összes információt.
* Azért, hogy figyelhessék a munkájukhoz szükséges információkat.
* Azért, hogy minden munkatárs naprakész információkkal rendelkezzen, és ugyanazokat az adatokat lássa és használja.
* Azért, hogy figyelhessék az üzleti folyamat, termék, vállalati egység, marketingkampány stb. állapotát.
* Azért, hogy egyedi képet kapjanak egy nagyobb irányítópultról – a számukra fontos összes mérőszámmal.

## <a name="my-workspace"></a>Saját munkaterület
És most térjünk vissza a Power BI irányítópultjához és munkaterületéhez. Nézze meg alaposabban a Power BI szolgáltatás kezdőlapjának alkotóelemeit.

![](media/service-basic-concepts/completenewer.png)

### <a name="1-navigation-bar-navbar"></a>1. **Navigációs sáv**
A navigációs sáv segítségével mozoghat a Power BI építőelemei – az irányítópultok, a jelentések és az adatkészletek – között.  

  ![](media/service-basic-concepts/navpane-new.png)

* Az **Adatok beolvasása** elemre kattintva [adatkészleteket, jelentéseket és irányítópultokat vehet fel a Power BI-ba](service-get-data.md).
* A navigációs sávot a ![](media/service-basic-concepts/expand-icon.png) ikonnal bonthatja ki vagy csukhatja össze.
* A **Keresés** használatával megtalálhatja a navigációs sáv elemeit.
* A plusz ikonra ![](media/service-basic-concepts/pbi_nancy_plus.png) kattintva létrehozhat egy új irányítópultot, vagy felvehet egy új adatkészletet.
* A listán szereplő **Irányítópultok, Jelentések** és **Adatkészletek** készen állnak a használatra.  A megosztott irányítópultok csak olvashatók, és a megosztás ikon ![](media/service-basic-concepts/sharing-icon.png) látható mellettük.
* Az irányítópultok, jelentések és adatkészletek neve általában azonos az alapjukat alkotó adatkészlet fájlnevével – de [át is nevezheti](service-rename.md) őket.
* A helyi menü megjelenítéséhez kattintson a jobb gombbal az irányítópultra, a jelentésre vagy az adatkészletre. 
  
  ![](media/service-basic-concepts/menu.png)

Egy kattintással:

* Kibonthatja vagy összecsukhatja a fejlécet.
* Megjelenítheti az irányítópultot.
* Megnyithatja a jelentés Olvasó nézetét.
* Hozzáférhet az adatkészlethez, hogy elemezze.

### <a name="2-dashboard-with-tiles"></a>2. **Az irányítópult és a csempék**
Az irányítópultokat [csempék](service-dashboard-tiles.md) alkotják.  A csempéket a jelentések Szerkesztési nézetében, a Q&A funkcióval és más irányítópultokon hozhatja létre, továbbá rögzítheti őket az Excel, az SSRS és más szolgáltatásokból is. A [widget](service-dashboard-add-widget.md) egy speciális csempe, amely magához az irányítópulthoz tartozik. A megjelenő csempéket a jelentés létrehozója/tulajdonosa helyezte el az irányítópulton.  A csempét a *rögzítés* műveletével kell hozzáadni az irányítópulthoz.

![](media/service-basic-concepts/canvas.png)

További információkért tekintse meg az **Irányítópultok** részt (feljebb).

### <a name="3-qa-question-box"></a>3. **Q&A kérdésmező**
Az adatelemzés egyik módja, hogy feltesz egy kérdést a Power BI Q&A funkciójának. Erre az egy vizualizáció formájában válaszol. A Q&A funkció nem használható arra, hogy tartalmat adjon egy jelentéshez; tartalmat csak az irányítópultokhoz adhat hozzá, csempék formájában.

A Q&A az irányítópulthoz csatlakozó adatkészlet(ek)ben keresi a választ.  Csatlakozó adatkészlet az, amelynek legalább egy csempéje rögzítve van az irányítópulton.

![](media/service-basic-concepts/qna.png)

A Q&A már a kérdés beírásának elején átirányítja Önt a Q&A lapra. A kérdés beírása közben a Q&A többek között átfogalmazással, automatikus kitöltéssel, valamint javaslatokkal segít a legjobb kérdés feltevésében és a helyes válasz megtalálásában. Ha megfelelőnek találja a kapott vizualizációt (választ), rögzítse az irányítópulton. További információkért tekintse meg a [Q&A a Power BI-ban](service-q-and-a.md) című részt.

### <a name="4-full-screen-notifications-settings-downloads-help-and-feedback"></a>4. **Teljes képernyő, Értesítések, Beállítások, Letöltések, Súgó és visszajelzés**
A jobb felső sarokban látható ikonok a beállításokra, az értesítésekre, a letöltésekre, a súgóra és a Power BI-csapatnak történő visszajelzésre mutatnak. A dupla nyílra kattintva **Teljes képernyős** módban nyithatja meg az irányítópultot.  

![](media/service-basic-concepts/help-new.png)

### <a name="5-dashboard-title-aka-what-dashboard-is-active"></a>5. **Az irányítópult címe** (melyik irányítópult aktív?)
Nem mindig könnyű megállapítani, hogy melyik irányítópult van aktív állapotban.  Az irányítópult címe megjelenik az irányítópult nézet lapján, a Q&A oldalon, a jelentés Szerkesztési és Olvasó nézetében, valamint az adatkészlet megnyitásakor.   

![](media/service-basic-concepts/dash-title-new.png)

### <a name="6-office-365-app-launcher"></a>6. **Az Office 365 appindítója**
Az appindítóval hozzáférhet az Office 365-appokhoz.

![](media/service-basic-concepts/basicconcepts2-newer.png)

### <a name="7-power-bi-home"></a>7. **A Power BI kezdőlapja**
Erre az elemre kattintva visszatérhet a legutóbb megtekintett irányítópulthoz.

   ![](media/service-basic-concepts/version-new.png)

### <a name="8-options"></a>8. **Beállítások**
A munkaterületnek ez a része azokat az ikonokat tartalmazza, amelyek az irányítópulttal való interakcióhoz szükségesek.  A **Csempe felvétele**, a **Kedvenc** és a **Megosztás** ikon mellett látható a három pont (...) ikon. Ezzel megjelenítheti az irányítópult másolási, nyomtatási, frissítési és egyéb lehetőségeit.

   ![](media/service-basic-concepts/options.png)

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)  
[Power BI-videók](videos.md)  
[Mit jelent a Power BI Premium?](service-premium.md)

További kérdései vannak? [Kérdezze a Power BI-közösséget!](http://community.powerbi.com/)

