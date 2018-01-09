---
title: "Jelentések oldalmegjelenítési és oldalnézet-beállításai"
description: "Jelentések oldalmegjelenítési és oldalnézet-beállításai"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: 
qualityfocus: 
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/24/2017
ms.author: mihart
ms.openlocfilehash: 650e02ea7d6f31fce9e5a0a458c41d6daa3fa9e1
ms.sourcegitcommit: 74fbbca81a056dda19b3647ae058005aba5296f5
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/03/2018
---
# <a name="page-display-settings-in-a-power-bi-report"></a>Oldal megjelenítési beállításai Power BI-jelentésben
Tudjuk, milyen fontos, hogy a jelentéseinek elrendezése az utolsó pixelig tökéletes legyen. Néha azonban ez kihívást jelenthet, ugyanis Ön és a munkatársai a jelentéseket különböző méretű és méretarányú képernyőkön nézik. 

Az alapértelmezett megjelenítési nézet a **Laphoz igazítás**, az alapértelmezett méretarány pedig a **16:9**-es. Ha a jelentést egy másik méretarányban szeretné zárolni, vagy máshogyan szeretné igazítani, akkor ehhez két eszköz áll rendelkezésére: az ***Oldal nézet*** beállításai és az ***Oldalméret***-beállítások.

<iframe width="560" height="315" src="https://www.youtube.com/embed/5tg-OXzxe2g" frameborder="0" allowfullscreen></iframe>


## <a name="where-to-find-page-view-settings-in-power-bi-service-and-power-bi-desktop"></a>Az oldalnézet-beállítások helye a Power BI szolgáltatásban és a Power BI Desktopban
Az oldalnézet-beállítások a Power BI szolgáltatásban és a Power BI Desktopban is elérhetők, de a felület kismértékben eltér. Az alábbi két szakasz azt ismerteti, hogy hol találhatja meg a Nézet beállításait az egyes Power BI-eszközökben.

### <a name="in-power-bi-desktop"></a>A Power BI Desktopban
A Jelentés nézetben a **Nézet** lapot választva nyithatja meg az oldalnézet-beállításokat, illetve a telefonos elrendezés beállításait.

  ![Kiválasztás panel](media/power-bi-report-display-settings/power-bi-desktop-view-settings.png)

### <a name="in-power-bi-service-apppowerbicom"></a>A Power BI szolgáltatásban (az app.powerbi.com webhelyen)
A Power BI szolgáltatásban nyisson meg egy jelentést, majd válassza a **Nézet** lehetőséget a bal felső menüsorban.

![](media/power-bi-report-display-settings/power-bi-change-page-view.png)

Az oldal nézetének beállításai az [Olvasó nézetből](service-interact-with-a-report-in-reading-view.md) és a [Szerkesztő nézetből](service-interact-with-a-report-in-editing-view.md) is elérhetők. A jelentés tulajdonosa a Szerkesztési nézetben az egyes jelentésoldalakhoz különböző oldalnézetek-beállításokat rendelhet, melyeket a jelentéssel együtt ment a rendszer. Ha a munkatársak Olvasó nézetben nyitnak meg egy jelentést, akkor a jelentésoldalakat a tulajdonos beállításainak megfelelően fogják látni.  Olvasási nézetben a munkatársak *néhányat* módosíthatnak az oldalnézet beállításai közül, de a rendszer nem menti a módosításokat, amikor kilépnek a jelentésből.

##    <a name="page-view-settings"></a>Oldalnézet beállításai
Az *Oldalnézet* beállításainak első készlete a jelentésoldal megjelenítését a böngésző ablakához viszonyítva szabályozza.  Az alábbiak közül választhat:

* **Laphoz igazítás** (alapértelmezett): a tartalmak úgy vannak méretezve, hogy a legjobban igazodjanak a laphoz.
* **Szélességhez igazítás**: a tartalmak úgy vannak méretezve, hogy a lap szélességéhez igazodjanak.
* **Tényleges méret**: a tartalmak teljes méretükben jelennek meg.

Az *Oldalnézet* beállításainak második készlete az objektumok a jelentésvásznon való elhelyezését szabályozza

* **Rácsvonalak megjelenítése**: rácsvonalak bekapcsolása az objektumok a jelentésvásznon való elhelyezésének segítése érdekében
* **Rácshoz illesztés**: a **Rácsvonalak megjelenítése** beállítással együtt használva pontosan helyezheti el és igazíthatja az objektumokat a jelentésvásznon 
* **Objektumok zárolása**: minden objektum zárolása a vásznon, hogy azokat ne lehessen áthelyezni vagy átméretezni
* **Kiválasztás panel**: a Kiválasztás panelen a vásznon levő összes objektum fel van sorolva, és meghatározhatja, hogy melyik jelenjen meg és melyik legyen elrejtve

    ![Kiválasztás panel](media/power-bi-report-display-settings/power-bi-selection-pane.png)



## <a name="page-size-settings"></a>Oldalméret-beállítások
![](media/power-bi-report-display-settings/power-bi--page-size.png)

Az *Oldalméret* beállításai csak a jelentések tulajdonosai számára érhetők el. A Power BI szolgáltatásban (az app.powerbi.com webhelyen) ehhez meg kell tudni nyitni a jelentést a [Szerkesztési nézetben](service-reading-view-and-editing-view.md). Ezek a beállítások a jelentésvászon méretarányát és a (pixelben megadott) tényleges méretét határozzák meg.   

* 4:3-as arány
* 16:9-es arány (alapértelmezett)
* Cortana
* Letter
* Egyéni (magasság és szélesség pixelben)

## <a name="next-steps"></a>Következő lépések
[Tudnivalók az Oldalnézet-beállítások és az Oldalméret-beállítások saját Power BI-jelentésekben való használatáról](power-bi-change-report-display-settings.md).

További tudnivaló a [Power BI-jelentésekről](service-reports.md)

[Power BI – Alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Felteheti azokat a Power BI-közösségnek](http://community.powerbi.com/)

