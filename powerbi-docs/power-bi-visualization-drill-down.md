---
title: "Lehatolás a vizualizációk mélyebb szintjeire a Power BI-ban"
description: "Ez a dokumentum bemutatja, hogyan lehet lehatolni a vizualizációk mélyebb szintjeire a Microsoft Power BI szolgáltatásban és a Power BI Desktopban."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: MNAaHw4PxzE
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 02/26/2018
ms.author: mihart
LocalizationGroup: Visualizations
ms.openlocfilehash: fb834c92953c2cafcbca77bc1b3828b385755bca
ms.sourcegitcommit: 743e44fc8730fea0f7149916080b0c6d7eb6359d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/28/2018
---
# <a name="drill-down-in-a-visualization-in-power-bi"></a>Lehatolás a vizualizációk mélyebb szintjeire a Power BI-ban
## <a name="drill-down-requires-a-hierarchy"></a>A lehatoláshoz hierarchiára van szükség
Ha a vizualizáció mögött hierarchikus adatstruktúra található, a részletesebb adatszintek kibonthatók. Tegyük fel például, hogy egy vizualizáció az olimpiai érmek számát jeleníti meg, sportonkénti, szakágankénti és versenyszámonkénti adathierarchia alapján. Alapértelmezés szerint a vizualizáció az érmek számát sportok szerinti bontásban (pl. gimnasztika, síelés, vízi sportok.) jeleníti meg. Ugyanakkor mivel rendelkezik hierarchiával, egy-egy vizuális elem (például egy oszlop, egy sáv vagy egy kör) kiválasztásakor egyre részletesebb ábra jeleníthető meg. Ha a **vízi sportok** elemre kattint, megjeleníthetők az úszásra, műugrásra és vízilabdára vonatkozó adatok.  Ezután ha a **műugrásra** kattint, megtekintheti a műugró, toronyugró és szinkronugró versenyszámokra vonatkozó információkat.

Hierarchiát csak saját jelentéseihez adhat, mások által Önnel megosztottakhoz nem.
Nem tudja, mely Power BI-vizualizációk tartalmaznak hierarchiát?  Húzza a kurzort az egyik vizualizáció fölé. Ha az alábbi részletezésvezérlők megjelennek a felső sarkokban, a vizualizáció rendelkezik hierarchiával.

![](media/power-bi-visualization-drill-down/power-bi-drill-icon4.png)  ![](media/power-bi-visualization-drill-down/power-bi-drill-icon2.png)  ![](media/power-bi-visualization-drill-down/power-bi-drill-icon3.png)
![](media/power-bi-visualization-drill-down/power-bi-drill-icon5.png) ![](media/power-bi-visualization-drill-down/power-bi-drill-icon6.png)  

Sajátos hierarchiatípust képviselnek a dátumok. Amikor dátummezőt ad egy vizualizációhoz, a Power BI automatikusan felvesz egy évekből, negyedévekből, hónapokból és napokból álló időhierarchiát. Ha ezzel kapcsolatban további információra van szüksége, tekintse át a [vizualizációs hierarchiákat és a lehatolás működését](guided-learning/visualizations.yml#step-18) áttekintő cikket.


  <iframe width="560" height="315" src="https://www.youtube.com/embed/MNAaHw4PxzE?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

> [!NOTE]
> Ha meg szeretné tanulni, hogyan hozhatók létre hierarchiák a Power BI Desktopot használva, tekintse meg a [How to create and add hierarchies](https://youtu.be/q8WDUAiTGeU) (Hierarchiák létrehozása és hozzáadása) című videót
> 
> 

## <a name="two-methods-to-drill-down"></a>Két lehatolási módszer
A vizualizációkban kétféle módon lehet le- illetve felhatolni.  Ez a cikk mindkét módszert bemutatja. Mindkét módszer ugyanazt eredményezi. Használja azt, amelyiket könnyebbnek érzi.

> [!NOTE]
> A lépések követéséhez [nyissa meg a Retail Analysis (Kiskereskedelmi elemzés) mintát](sample-datasets.md) a Power BI szolgáltatásban, majd hozzon létre egy fatérképet, mely a **Total Units This Year (Egységek éves száma összesen)** értéket (Értékek) **Territory** (Terület), **City** (Város), **PostalCode** (Irányítószám), és **Name** (Név) bontásban (Csoport) tudja megjeleníteni.  
> 
> 

## <a name="method-one-for-drill-down"></a>A lehatolás első módszere
Ez a módszer a vizualizációk felső sarkaiban megjelenő lehatolási ikonokat használja.

1. A Power BI-ban nyisson meg egy jelentést [Olvasó nézetben vagy Szerkesztő nézetben](service-reading-view-and-editing-view.md). A lehatoláshoz hierarchiával rendelkező vizualizációra van szükség. 
   
   Az alábbi animáción egy hierarchia látható.  A vizualizáció területből (Territory), városból (City), irányítószámból (Postal Code) és városnévből (Name) felépülő hierarchiával rendelkezik. Minden területhez egy vagy több város, minden városhoz egy vagy több irányítószám tartozik, és így tovább. Alapértelmezés szerint a vizualizáció csak a területi adatokat jeleníti meg, mert a lista első eleme a *Territory* (Terület).
   
   ![](media/power-bi-visualization-drill-down/power-bi-hierarcy-list.png)
2. A lehatolás engedélyezéséhez kattintson a vizualizáció jobb felső sarkában látható, nyilat ábrázoló ikonra. Ha az ikon sötét színű, az adatszintek közötti mozgás engedélyezve van (a lehatolási mód be van kapcsolva). Ha nem kapcsolja be a lehatolási üzemmódot, akkor a rendszer a jelentés oldalon szereplő többi diagram tekintetében keresztszűrést alkalmaz, amikor rákattint valamelyik vizualizációs elemre (pl. az egyik oszlopra vagy egy körre).    
   
   ![](media/power-bi-visualization-drill-down/power-bi-drill-icon.png)
3. Ha **egyszerre csak egy mezőnyit** szeretne lehatolni, jelölje ki a vizualizáció egyik elemét. Egy sávdiagramban ez az egyik sáv kijelölését jelenti. Egy fatérképen ez az egyik **levél** kijelölését jelenti. Nézze meg, hogyan változik a csempe, ahogy le- és felhatol a hierarchiában. Az alábbi animációban először az egységek területenkénti éves számát, majd a területenkénti és városonkénti, majd területenkénti, városonkénti és irányítószámonkénti, és végül a területenkénti, városonkénti, irányítószámonkénti és nevenkénti teljes éves számát mutatja. Ha ismét feljebb szeretne lépni, kattintson a vizualizáció bal felső sarkában látható **Felhatolás** ![](media/power-bi-visualization-drill-down/power-bi-drill-icon5.png) ikonra, ahogy az alább látható.
   
   ![](media/power-bi-visualization-drill-down/drill.gif)
4. Ha az ***összes szintet egyszerre*** szeretné kibontani, kattintson a vizualizáció bal felső sarkában látható, lefelé mutató dupla nyílra.
   
   ![](media/power-bi-visualization-drill-down/pbi_drillall.png)
5. Ha vissza szeretne lépni, kattintson a vizualizáció bal felső sarkában látható felfelé mutató nyílra. Ha vissza szeretne lépni, kattintson a vizualizáció bal felső sarkában látható felfelé mutató nyílra.
   
   ![](media/power-bi-visualization-drill-down/pbi_drillup2.png)

## <a name="method-two-for-drill-down"></a>A lehatolás második módszere
Ehhez a módszerhez a Power BI felső menüsorában található **Tallózás** legördülő menüt kell használni.

1. A Power BI-ban nyisson meg egy jelentést [Olvasó nézetben vagy Szerkesztő nézetben](service-reading-view-and-editing-view.md). A lehatoláshoz hierarchiával rendelkező vizualizációra van szükség. 
   
   Az alábbi ábrán egy hierarchia látható.  A vizualizáció területből (Territory), városból (City), irányítószámból (Postal Code) és városnévből (Name) felépülő hierarchiával rendelkezik. Minden területhez egy vagy több város, minden városhoz egy vagy több irányítószám tartozik, és így tovább. Alapértelmezés szerint a vizualizáció csak a területi adatokat jeleníti meg, mert a lista első eleme a *Territory* (Terület).
   
   ![](media/power-bi-visualization-drill-down/power-bi-hierarcy-list.png)
2. A lehatolás engedélyezéséhez válassza ki az egyik vizualizációt, amely így aktívvá válik. Ezután a Power BI felső menüsorából válassza ki a **Tallózás** > **Lehatolás** lehetőséget. A vizualizáció jobb felső sarkában látható lehatolás ikon sötét hátterűre változik. ![](media/power-bi-visualization-drill-down/power-bi-drill-icon2.png)  
   
   ![](media/power-bi-visualization-drill-down/power-bi-explore2.png)
3. Ha sikerült engedélyezni a lehatolást, bontson ki egy-egy szintet a fatérkép egy-egy levelére kattintva. Az alábbi példában a kiválasztott terület neve **NC**, így a vizualizáció az észak-karolinai (North Carolina) területen éves szinten értékesített egységek számát mutatja, városonként.
   
   ![](media/power-bi-visualization-drill-down/power-bi-drilldown-1.png)
4. Ha szeretné az összes szintet egyszerre kibontani, kattintson a **Tallózás** > **A következő szint megjelenítése** lehetőségre.
   
   ![](media/power-bi-visualization-drill-down/power-bi-show-next-level.png)
5. Az előző szintre történő visszalépéshez kattintson a **Tallózás** > **Felhatolás** lehetőségre.
   
   ![](media/power-bi-visualization-drill-down/power-bi-drill-up2.png)

6. A vizualizáció létrehozásához használt adatok megjelenítéshez kattintson az **Adatok megjelenítése** lehetőségre. Az adatok a vizualizáció alatt, egy panelen jelennek meg. Az ablaktábla a vizualizációs szintek közötti mozgás során is megmarad. Ha további információra van szüksége, olvassa át a [vizualizáció létrehozásához használt adatok megjelenítéséről](service-reports-show-data.md) szóló cikket.

## <a name="understanding-the-hierarchy-axis-and-hierarchy-group"></a>A hierarchiatengely és hierarchiacsoport ismertetése
A hierarchiatengely és a hierarchiacsoport tulajdonképpen a megtekinteni kívánt adatok részletességét szabályozó eszközöket jelenti. A kategóriákba és alkategóriákba csoportosítható minden adat rendelkezik hierarchiával. Ez természetesen magában foglalja a dátumokat és az időt.

Ha egy Power BI-vizualizációt hierarchiával együtt szeretne létrehozni, jelöljön ki egy vagy több adatmezőt, amelyet a **Tengely**vagy a **Csoport** gyűjtőhöz ad, valamint az adatmezőkként vizsgálni kívánt adatokat, amelyeket az**Értékek** gyűjtőhöz ad. Ha a Részletezés mód ikonjai a vizualizáció jobb és bal felső sarkában jelennek meg, akkor biztos lehet benne, hogy az adatok hierarchikusak. 

Alapvetően kétféle hierarchikus adatokkal dolgozunk:
- Dátum- és időadatok – Ha egy Dátum/idő adattípussal rendelkező adatmezője van, akkor hierarchikus adatokkal dolgozik. A Power BI automatikusan létrehozza a hierarchiát azon adatmezőkhöz, amelyek értékei [Dátum/idő](https://msdn.microsoft.com/library/system.datetime.aspx) struktúra szerint elemezhetők. A **Tengely** vagy a **Csoport** gyűjtőhöz csak egy Dátum/Idő mezőt kell adnia.
- Kategorikus adatok – Ha az adatok algyűjteményeket tartalmazó gyűjteményekből származnak, vagy olyan adatsorokkal rendelkeznek, amelyeknek közös értékeik vannak, akkor hierarchikus adatokkal dolgozik.

A Power BI segítségével egyesével vagy részhalmazonként kibonthatja ezeket. Lehatolhat a szintenkénti részhalmazokig, vagy minden részhalmazt egyszerre megtekinthet egy szinten. Például lehatolhat egy adott évig, vagy megtekintheti az egyes évek eredményeit a hierarchiában lefelé haladva. Hasonlóképpen hatolhat felfelé is.

A következő szakaszok a legmagasabb, a középső és a legalsó nézetből való lehatolást ismertetik.

### <a name="hierarchical-data-and-time-data"></a>Hierarchikus és időadatok
Ehhez a példához használja fel a [kiskereskedelmi elemzési mintát](sample-datasets.md), és hozzon létre egy halmozott oszlopdiagram típusú vizualizációt, amelynek tengelye a **Hónap**, az értékei pedig az **Összes eladás**.  

Bár a Tengely adatmezője a **Hónap**, a **Tengely** gyűjtőben továbbra is létrehoz egy **Év** kategóriát is. Ennek az az oka, hogy a Power BI a teljes Dátum/Idő-struktúrát megadja az összes beolvasott értékhez. A hierarchia tetején az év adatai jelennek meg.

![](media\power-bi-visualization-drill-down/power-bi-hierarchical-axis-datetime-1.png)

A Részletezés módban kattintson a diagram sávjára, ha egy szinttel lejjebb szeretne lépni a hierarchiában. Itt három sávot láthat, amelyek az elérhető negyedéveknek felelnek meg. A bal felső sarokban található ikonok közül válassza az **Expand all down one level of the hierarchy** (Az összes kibontása a hierarchia egy szintjével lejjebb) lehetőséget. Ezt ismételje meg a hierarchia legalsó szintjével is, amely az egyes hónapok eredményeit jeleníti meg.

![](media\power-bi-visualization-drill-down/power-bi-hierarchical-axis-datetime-2.png)

A vizualizáción kívül az egyes jelentések adataiban is láthatjuk a hierarchiát. Az alábbi táblázat egy jelentés egyetlen hónapjában vagy minden hónapjában végzett lehatolásának az **Adatok megjelenítése** műveletével kapott eredményeit jeleníti meg. 

Megfigyelheti, hogy az adatok megegyeznek a negyedéves és az éves jelentésekben, azonban ha lehatol az **Értékek** részletességi szintjéig, az egyetlen hónapra vonatkozó jelentés konkrétabb adatokat jelenít meg, az összes hónapra vonatkozó jelentés pedig több adatot tartalmaz.


|Kibontás módja|Év|Negyedév|Hónap|Nap|
| ---|:---:|:---:|:---:|---|
|Egyirányú|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-year.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-quarter.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-month.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-day.png)|
|Összes|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-year.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-quarter.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-month.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-day.png)|


### <a name="hierarchical-category-data"></a>Hierarchikus kategóriaadatok
A gyűjteményekből és algyűjteményekből modellezett adatok hierarchikusak. Jó példák erre a helyadatok. Vegyünk például egy táblázatot egy olyan adatforrásban, amely az Ország, Állam, Város és Irányítószám oszlopokkal rendelkezik. Azok az adatok, amelyek megegyező Ország, Állam és Város értékekkel bírnak, hierarchikusak.

Ehhez a példához használja a [kiskereskedelmi elemzési mintát](sample-datasets.md). Hozzon létre egy halmozott oszlopdiagram típusú vizualizációt, amely az **Egységek éves számát** (Értékek) jeleníti meg a **Terület**, a **Város**, az **Irányítószám** és a **Név** szerint (Csoport).  

![](media\power-bi-visualization-drill-down/power-bi-hierarchical-axis-category-1.png)

A Részletezés módban a bal felső sarokban található ikonok közül válassza az **Expand all down one level of the hierarchy** (Az összes kibontása a hierarchia egy szintjével lejjebb) lehetőséget háromszor.
Ekkor a hierarchia legalsó szintjén kell lennie, amely a Terület, a Város és az Irányítószám szerint jeleníti meg az eredményeket.

![](media\power-bi-visualization-drill-down/power-bi-hierarchical-axis-category-2.png)

A vizualizáción kívül az egyes jelentések adataiban is láthatjuk a hierarchiát. Az alábbi táblázat egy jelentés egyetlen területén vagy minden területén végzett lehatolásának az **Adatok megjelenítése** műveletével kapott eredményeit jeleníti meg. A lehatolás során láthatja, hogy az egyetlen területre vonatkozó jelentés konkrétabb adatokat jelenít meg, az összes területre vonatkozó jelentés pedig több adatot tartalmaz.


| Kibontás módja|Terület|Település|Irányítószám|Név|
| ---|:---:|:---:|:---:|---|
|Egyirányú|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-territory.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-territory-city.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-territory-city-postal.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-one-territory-city-postal-name.png)|
|Összes|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-territory.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-territory-city.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-territory-city-postal.png)|![](media\power-bi-visualization-drill-down/power-bi-hierarchical-all-territory-city-postal-name.png)|


## <a name="considerations-and-limitations"></a>Megfontolandó szempontok és korlátozások
* Ha dátum mező felvételekor a rendszer nem hoz létre automatikusan időhierarchiát, elképzelhető, hogy a „dátum” mező nem dátum mezőként lett elmentve. Ha Ön az adatkészlet tulajdonosa, nyissa meg *Adatok* nézetben a Power BI Desktopban, válassza ki a dátumot tartalmazó oszlopot, és a Modellezés lapfülön módosítsa az **Adattípust** **Dátumra** vagy **Dátum és időre**. Ha a jelentés meg lett osztva Önnel, kérje meg a tulajdonost a módosítások végrehajtására.  
  
  ![](media/power-bi-visualization-drill-down/power-bi-change-data-type2.png)

## <a name="next-steps"></a>További lépések
[Vizualizációk a Power BI-jelentésekben](power-bi-report-visualizations.md)

[A Power BI-jelentések](service-reports.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

