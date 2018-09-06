---
title: A Power BI Premium kapacitásának figyelése a cégnél
description: A Power BI felügyeleti portál és a Power BI Premium kapacitás-metrikák alkalmazás használata
author: mgblythe
ms.author: mblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 08/29/2018
LocalizationGroup: Premium
ms.openlocfilehash: 8e19bc596bef3862dca79ac92ffbd74954a9c756
ms.sourcegitcommit: 6be2c54f2703f307457360baef32aee16f338067
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/30/2018
ms.locfileid: "43300161"
---
# <a name="monitor-power-bi-premium-capacities-in-your-organization"></a>A Power BI Premium kapacitásának figyelése a cégnél

A cikk azt tekinti át, hogyan monitorozhatóak a Power BI Premium kapacitásmetrikái. A kapacitás felhasználásának figyelemmel kísérése segít abban, hogy megalapozott döntéseket hozhasson a kapacitáskezelést illetően. 

A kapacitás monitorozható a Power BI Premium Metrics alkalmazással vagy a felügyeleti portálon is. Az alkalmazás használatát javasoljuk, mert az jelentősen több információt nyújt, de a jelen cikkben mindkét monitorozási lehetőséget megvizsgáljuk.

## <a name="install-the-premium-capacity-metrics-app"></a>A Premium Capacity Metrics alkalmazás telepítése

A [Premium Capacity Metrics alkalmazást](https://app.powerbi.com/groups/me/getapps/services/capacitymetrics) közvetlenül is megnyithatja, de ha szeretné, ugyanúgy telepítheti is, mint bármely más alkalmazást a Power BI-ban.

> [!IMPORTANT]
> Az alkalmazást csak akkor telepítheti és használhatja, ha legalább egy kapacitásnak Ön a kapacitásadminisztrátora. Ha a Power BI rendszergazdája, az még nem elegendő ehhez. 

1. A Power BI-ban kattintson az **Alkalmazások** elemre.

    ![Ugrás az alkalmazásokra](media/service-admin-premium-monitor-capacity/apps.png)

2. A jobb oldalon kattintson az **Alkalmazások beszerzése** lehetőségre.

3. Az **Alkalmazások** kategóriában keresse meg a **Power BI Premium Capacity Metrics alkalmazást**.

4. Az alkalmazás telepítéséhez regisztrálnia kell.

Az alkalmazás telepítése után már megtekintheti a cég kapacitásainak információit. Most vizsgáljuk meg a legfontosabb elérhető metrikákat.

## <a name="use-the-metrics-app"></a>A metrika alkalmazás használata 
Az alkalmazás a megnyitás után egy irányítópultot jelenít meg, amelyen egy összefoglaló áttekintés látható minden olyan kapacitásról, amelyhez Önnek adminisztrátori jogosultsága van.

![Premium-jelentések áttekintése](media/service-admin-premium-monitor-capacity/app-dashboard.png)

### <a name="filtering"></a>Szűrés

A **Szűrők az összes oldalra** lapon kiválaszthatja a kapacitást, az adatkészletet és/vagy a legutóbbi hét napra kiterjedő dátumtartományt. Ezek a szűrők az aktuális jelentés minden releváns oldalára és csempéjére alkalmazva lesznek. Ha nincs szűrő kiválasztva, akkor a jelentésben alapértelmezés szerint a legutóbbi hétre vonatkozó metrikák jelennek meg minden elérhető kapacitásról.

![Premium-jelentések áttekintése](media/service-admin-premium-monitor-capacity/premium-report-overview.png)

### <a name="summary-tab"></a>Összefoglalás lap

Az **Összefoglalás** lapon az entitásokra, a rendszerre és az adatkészletekre vonatkozó kapacitások nézete jelenik meg.

![Minden oldalra alkalmazott szűrők](media/service-admin-premium-monitor-capacity/premium-summary-report.png)

| **Terület** | **Metrikák** |
| --- | --- |
| **Entitások** | * Az Önhöz tartozó kapacitások száma<br> * A kapacitásában meglévő különálló adatkészletek száma<br> * A kapacitásában meglévő különálló munkaterületek száma |
| **Rendszer** | * Az átlagos memóriahasználat GB-ban az elmúlt hét napban<br> * A legmagasabb memóriahasználat GB-ban az elmúlt hét napban, az események helyi idejével<br> * Az a szám, ahányszor a CPU-használat meghaladta a küszöbérték 80%-át a legutóbbi hét napban, három perces gyűjtőkbe csoportosítva<br> * A legtöbb eset, amikor a CPU-használat meghaladta a 80%-ot a legutóbbi hét napban, egyórás gyűjtőkbe elosztva, és az esemény helyi idejével<br> * Az a szám, ahányszor a Közvetlen lekérdezés/Élő kapcsolat értéke meghaladta a küszöbérték 80%-át a legutóbbi hét napban, három perces gyűjtőkbe csoportosítva<br> * A legtöbb eset, amikor a Közvetlen lekérdezés/Élő kapcsolat értéke meghaladta a 80%-ot a legutóbbi hét napban, egyórás gyűjtőkbe elosztva, és az esemény helyi idejével |
| **Adatkészlethez tartozó számítási feladatok** | * A frissítések teljes száma a legutóbbi hét napban<br> * A sikeres frissítések teljes száma a legutóbbi hét napban<br> * A sikertelen frissítések teljes száma a legutóbbi hét napban<br> * A nem elegendő mennyiségű memória miatt sikertelen frissítések teljes száma<br> * A frissítések átlagos időtartama percekben kifejezve és a művelethez szükséges teljes idő<br> * Az átlagos frissítési idő percekben kifejezve, valamint a beütemezett időpont és a művelet kezdete közötti átlagos késés<br> * A lekérdezések teljes száma a legutóbbi hét napban<br> * A sikeres lekérdezések teljes száma a legutóbbi hét napban<br> * A sikertelen lekérdezések teljes száma a legutóbbi hét napban<br> * A lekérdezések átlagos időtartama percekben kifejezve és a művelethez szükséges teljes idő<br> * A memóriaterhelés miatt kizárt modellek teljes száma |
|  |  |

### <a name="refreshes-tab"></a>Frissítések lap

A **Frissítések** lap listázza a frissítések teljes számát, a sikerességi rátát, az átlagos és a maximális frissítési és várakozási időt, valamint az átlagos és maximális frissítési időtartamot adatkészletek szerint a legutóbb hét napra vonatkozóan. Az utolsó két diagram a frissítéseket és a GB-ban kifejezett memóriafogyasztást hasonlítja össze, valamint az átlagos várakozási időt egyórás gyűjtőkbe csoportosítva, helyi időben kifejezve. A felső sávdiagramok az első öt adatkészletet mutatják aszerint, hogy mennyi időt vett igénybe az adatkészlet frissítése (a frissítés időtartama), és hogy mennyi volt a maximális várakozási idő. Ha több magas frissítési várakozási érték is van, az azt jelzi, hogy a kapacitáshasználat a csúcsértékhez közelít.

![A Premium szint frissítési jelentése](media/service-admin-premium-monitor-capacity/premium-refresh-report.png)

### <a name="datasets-tab"></a>Adatkészletek lap

Az **Adatkészletek** lap azt mutatja, hogy összesen hány adatkészlet lett kizárva memóriaterhelés miatt, órákra lebontva.

![Prémium szint adatkészlet-jelentése](media/service-admin-premium-monitor-capacity/premium-datasets-report.png)

### <a name="system-tab"></a>Rendszer lap

A **Rendszer** lapon a processzor magas kihasználtsága (hányszor haladta meg a 80%-ot a terhelés), a közvetlen lekérdezések és élő kapcsolatok magas kihasználtsága, valamint a memóriafogyasztás látható.

![Premium szint rendszerjelentése](media/service-admin-premium-monitor-capacity/premium-system-report.png)

## <a name="monitor-power-bi-embedded-capacity"></a>A Power BI Embedded-kapacitás monitorozása

A Power BI Premium Capacity Metrics alkalmazással *A SKU*-kapacitásokat is monitorozhat a Power BI Embedded szolgáltatásban. Ha Ön az adott kapacitás adminisztrátora, akkor a kapacitás megjelenik a jelentésben is. A jelentést azonban csak akkor lehet frissíteni, ha a Power BI-nak megad bizonyos engedélyeket az A SKU-kra vonatkozóan:

1. Nyissa meg a kapacitást az Azure Portalon.
1. Kattintson a **Hozzáférés-vezérlés (IAM)** lehetőségre, és adja hozzá a „Power BI Premium” alkalmazást az Olvasó szerepkörhöz. Ha az alkalmazást nem találja név szerint, az ügyfél-azonosító használatával is hozzáadhatja azt: cb4dc29f-0bf4-402a-8b30-7511498ed654.

    ![Engedélyek a Power BI Embeddedhez](media/service-admin-premium-monitor-capacity/embedded-permissions.png)

> [!NOTE]
> Power BI Embedded kapacitás használatát monitorozhatja az alkalmazással vagy az Azure Portalon, a Power BI felügyeleti portálján azonban nincs erre lehetőség.

## <a name="basic-monitoring-in-the-admin-portal"></a>Alapszintű monitorozás a felügyeleti portálon

A felügyeleti portál **Kapacitásbeállítások** területén négy kijelző van, amelyeken a kapacitás által felhasznált terhelés és erőforrás-fogyasztás látható a legutóbbi hét napra vonatkozóan. A négy csempe egyórás időszakokkal működik, és megmutatja, hány óráig volt a vonatkozó metrika a legutóbbi hét nap során 80% fölötti értéken. Ez a metrika azt jelzi, hogy a végfelhasználói élmény minősége csökkenhet.

![7 napot használat](media/service-admin-premium-monitor-capacity/usage-in-days.png)

| **Metrika** | **Leírás** |
| --- | --- |
| Processzor |Ahányszor a processzorhasználat túllépte a 80%-ot. |
| Memóriaakadozás |A háttérrendszerbeli magok memóriaterhelését mutatja. Ez egészen pontosan azt jelzi, hogy az adathalmazok hányszor lettek kiürítve a memóriából a több adathalmaz használata miatti memóriaterhelés következtében. |
| Memóriahasználat |Átlagos memóriahasználat, gigabájtban (GB) kifejezve. |
| DQ/másodperc | Ahányszor a Direct Query-kapcsolatok és élő kapcsolatok száma meghaladta a korlát 80%-át. <br> * A DirectQuery és élő kapcsolatos lekérdezések másodpercenkénti maximális száma korlátozott.* A korlátok a következők: 30/s P1-nél, 60/s P2-nél és 120/s P3 esetén. * A Direct Query és az élő kapcsolatos lekérdezések száma összeadódik. Ha például 15 DirectQueryvel és 15 élő kapcsolattal rendelkezik egy adott másodpercben, elérte a korlátot<br>* Ez mind a helyszíni, mind a felhőkapcsolatokra vonatkozik. |
|  |  |

A metrikák az elmúlt hét használati adatait tükrözik.  Ha szeretne részletesebb nézetet látni a metrikákról, kattintson az összesítő csempék egyikére.  Ez megnyitja a prémium szintű kapacitása metrikáinak részletes diagramjait tartalmazó lapot. Az alábbi ábrán a CPU-metrika részletei láthatóak.

![Részletes használati diagram – Processzor](media/service-admin-premium-monitor-capacity/premium-usage-detailed-chart-cpu.png)

Ezeket a diagramokat a rendszer óránként összegzi az elmúlt hétre vonatkozóan, és segítenek megállapítani, hogy mikor történhetett teljesítménnyel kapcsolatos esemény a prémium szintű kapacitásában.

Exportálhatja bármelyik metrika mögöttes adatait egy CSV-fájlba.  Ezzel a művelettel részletes adatokat kaphat három perces időközökkel az elmúlt hét minden egyes napjára vonatkozóan.

## <a name="next-steps"></a>Következő lépések

Most, hogy megismerkedett a Power BI Premium kapacitásainak monitorozásával, tudjon meg többet a kapacitás optimalizálásáról is.

> [!div class="nextstepaction"]
> [A Power BI Premium-kapacitás erőforrás-kezelése és optimalizálása](service-premium-understand-how-it-works.md)
