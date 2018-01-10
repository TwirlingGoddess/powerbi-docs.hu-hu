---
title: "Jelentés beágyazása iFrame használatával"
description: "A Power BI jelentéskészítő kiszolgáló telepítése nagyon gyorsan elvégezhető. A letöltés, a telepítés és a konfigurálás néhány percen belül elvégezhető, és a rendszere máris működésre kész."
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 11/09/2017
ms.author: maghan
ms.openlocfilehash: 0019b0a8d3fa628a1b3932a4c19eba0bf0d66ee3
ms.sourcegitcommit: eec6b47970bf69ed30638d1a20051f961ba792f2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/06/2018
---
# <a name="quickstart-embed-a-power-bi-report-using-an-iframe-and-url-parameters"></a>Rövid útmutató: Power BI-jelentés beágyazása egy iFrame és URL-paraméterek használatával

Az alkalmazásában egy iFrame használatával bármilyen jelentést beágyazhat. 

## <a name="url-parameter"></a>URL-paraméter

Bármely jelentés URL-címéhez hozzáadhatja a `?rs:Embed=true` lekérdezési sztringet.

Példa:

```
http://myserver/reports/powerbi/Sales?rs:embed=true
```

Ez használható a Power BI jelentéskészítő kiszolgáló bármelyik típusú jelentése esetén.

## <a name="iframe"></a>iFrame

Ha megvan az URL-cím, létrehozhat egy weblapon egy iFrame-et, amely megjeleníti a jelentést.

Példa:

```
<iframe width="800" height="600" src="http://myserver/reports/powerbi/Sales?rs:embed=true" frameborder="0" allowFullScreen="true"></iframe>
```

## <a name="url-filter"></a>URL-szűrő

Az URL-címhez hozzáadhat egy lekérdezésiszting-paramétert a Power BI-jelentésben visszaadott adatok szűrésére.

A szintaxis nagyon egyszerű – a jelentés URL-címével kezdje, adjon hozzá egy kérdőjelet, majd ezt a szűrési szintaxist.

URL?filter=***Tábla***/***Mező*** eq '***érték***'

A következő szempontokat vegye figyelembe:

- A **Tábla** és a **Mező** nevei megkülönböztetik a kis- és nagybetűket, az **érték** viszont nem.
- A jelentés olyan mezők alapján is szűrhető, amelyek a jelentés nézetében nem láthatók.
- Az **értéket** aposztrófok között kell megadni.
- A mezőnek sztring típusúnak kell lennie.
- A tábla és a mező nevei nem tartalmazhatnak szóközöket.

###  <a name="example-filter-on-a-field"></a>Példa: Szűrés egy mező alapján

Vegyük például a [Kiskereskedelmi elemzési mintát](../sample-datasets.md). Tegyük fel, hogy a jelentéskészítő kiszolgáló „power-bi” mappájában található egy jelentés, amelynek az URL-címe a következő:

```
https://report-server/reports/power-bi/Retail-Analysis-Sample
```

A Kiskereskedelmi elemzési minta térképi vizualizációján az Észak-Karolinában és más államokban található üzleteket láthatja.

![Kiskereskedelmi elemzési minta – térképi vizualizáció](media/quickstart-embed/report-server-retail-analysis-sample-map.png)

Az **Store** (Üzlet) tábla **Territory** (Terület) mezőjében tárolt *NC* érték Észak-Karolinát jelenti. Tehát ha szűrni szeretné a jelentést, hogy csak az Észak-Karolinában található üzletek adatait jelenítse meg, akkor fűzze hozzá az URL-címhez a következőt:

?filter=Store/Territory eq 'NC'

A jelentés így már szűrve lett Észak-Karolinára, és a jelentés oldalán található összes vizualizáció csak Észak-Karolina adatait jeleníti meg.

![Kiskereskedelmi elemzési minta – szűrt vizualizációk](media/quickstart-embed/report-server-retail-analysis-sample-filtered-map.png)

### <a name="create-a-dax-formula-to-filter-on-multiple-values"></a>DAX-képlet létrehozása több érték alapján történő szűréshez

A szűrés egy másik módja, ha létrehoz a Power BI-ban egy számított oszlopot, amely két mezőt egyetlen értékké fűz össze. Ezt követően már szűrhet erre az értékre.

A Kiskereskedelmi elemzési mintában például két mező található: Territory (Terület) és Chain (Üzletlánc). A Power BI Desktopban [létrehozhat egy számított oszlopot](../desktop-tutorial-create-calculated-columns.md) (Mezőt), TerritoryChain (TerületÜzletlánc) néven. Ne feledje, hogy a **Mező** neve nem tartalmazhat szóközöket. Itt látható az oszlop DAX-képlete.

TerritoryChain = [Territory] & "-" & [Chain]

Tegye közzé a jelentést a Power BI jelentéskészítő kiszolgálón, majd használja az URL-cím lekérdezési sztringjét, hogy a jelentés csak az Észak-Karolinában található Lindseys üzletek adatait jelenítse meg.

```
https://report-server/reports/power-bi/Retail-Analysis-Sample?filter=Store/TerritoryChain eq 'NC-Lindseys'

```

## <a name="next-steps"></a>Következő lépések

[Rövid útmutató: Power BI-jelentés létrehozása a Power BI jelentéskészítő kiszolgálóra](quickstart-create-powerbi-report.md)  
[Rövid útmutató: Többoldalas jelentés létrehozása a Power BI jelentéskészítő kiszolgálóra](quickstart-create-paginated-report.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)