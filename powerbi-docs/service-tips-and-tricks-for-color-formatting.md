---
title: Tippek és trükkök a színformázáshoz a Power BI-ban
description: Tippek és trükkök a színformázáshoz a Power BI-ban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 05/02/2018
ms.author: davidi
LocalizationGroup: Visualizations
ms.openlocfilehash: 3c91a6a70899a4a59c3d98cd9ab948284df5b662
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34298389"
---
# <a name="tips-and-tricks-for-color-formatting-in-power-bi"></a>Tippek és trükkök a színformázáshoz a Power BI-ban
A Power BI sokféle lehetőséget kínál, amelyekkel egyedivé tehetők az irányítópultok és a jelentések. Ez a cikk néhány olyan ötletet fejt ki részletesen, amelyek segítségével meggyőzőbb, érdekesebb és az Ön igényeinek jobban megfelelő Power BI-vizualizációkat készíthet.

A következő tippeket kínáljuk Önnek. Van egy másik remek ötlete? Nagyszerű! Küldje el nekünk, és talán hozzáadjuk ehhez a listához.

* Egy adatpont színének módosítása
* Diagram színeinek meghatározása egy numerikus érték alapján
* Adatpontok színének meghatározása egy mező értéke alapján
* A színskála összeállításának testre szabása
* Széttartó színskálák használata
* Művelet visszavonása a Power BI-ban

A módosításhoz szerkesztenie kell a jelentést: jelölje ki saját **Jelentését** a **Saját munkaterület** panelen, majd válassza a **Jelentés szerkesztése** lehetőséget a felső menüben, ahogyan az alábbi ábrán látható.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_1.png)

Amikor a **Jelentés** vászon jobb oldalán megjelenik a **Vizualizációk** panel, megkezdheti a testre szabást.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_2.png)

## <a name="change-the-color-of-a-single-data-point"></a>Egy adatpont színének módosítása
Előfordul, hogy egy adott adatpontot szeretne kiemelni. Ez lehet egy újonnan bevezetett termék eladott mennyisége, vagy egy javuló minőségi mutató egy új program elindítása után. A Power BI-ban kiemelhet egy választott adatpontot a színe módosításával.

Az alábbi vizualizáció államokat rangsorol a megélhetési költségek szerint. 

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_3.png)

Képzelje el, hogy színes kiemeléssel gyorsan meg szeretné mutatni, hol áll Washington ebben a rangsorban. A lépések a következők:

Bontsa ki az **Adatszínek** szakaszt. A következő jelenik meg.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_4.png)

Állítsa az **Összes megjelenítése** kapcsolót **Be** helyzetbe. Így a vizualizáció összes adatelemének színe megjelenik. A kurzort az adatpontok fölé helyezve engedélyezett a görgetés, tehát az adatpontok bármelyikét módosíthatja.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_5.png)

Állítsa most a **Washington** államhoz tartozó színt zöldre. A **Washington** elemig görgetve kattintson a színmezőben lévő nyílra a paletta megnyitásához.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_6.png)

Miután választott, a **Washington** adatpont szép zöld, és kétségtelenül szembeszökő színt vesz fel.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_7.png)

A Power BI akkor is megjegyzi a választását és zölden jeleníti meg **Washingtont**, ha Ön megváltoztatja, majd visszaváltoztatja a vizualizáció típusát.

Egynél több adatpont színe is megváltoztatható. A következő ábrán **Arizona** piros, **Washington** továbbra is zöld színnel jelenik meg.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_8.png)

A színekkel sok mindent megtehet. A következő bekezdések a színátmenetekkel foglalkoznak.

## <a name="base-the-colors-of-a-chart-on-a-numeric-value"></a>Diagram színeinek meghatározása egy numerikus érték alapján
Egy diagramnak gyakran előnyére válik a színek dinamikus meghatározása egy mező numerikus értéke alapján. Ezen a módon az oszlopok magasságát megadó érték mellett egy másikat is megjeleníthet, így két értéket szemléltethet egy diagramon. Használhatja a lehetőséget egy bizonyos érték feletti (vagy alatti) adatpontok kiemelésére – például alacsony jövedelmezőségű területek kimutatására.

A következő szakaszok különböző módszereket mutatnak be a színek numerikus érték alapján történő meghatározására.

## <a name="base-the-color-of-data-points-on-a-value"></a>Adatpontok színének meghatározása egy érték alapján
A szín érték alapján történő megadásához húzza a színezés alapjául szánt mezőt a **Mező** panel **Színtelítettség** területére. A következő ábrán az **Adózatlan nyereség** mező adja meg a **Színtelítettség** értékét. Mint látható, bár a **Velo** **Bruttó értékesítés** mutatója nagyobb (az oszlopa magasabb), az **Amarilla** nagyobb **Adózatlan nyereséget** ért el (az oszlopának telítettebb a színe).

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_9.png)

## <a name="customize-the-colors-used-in-the-color-scale"></a>A színskála összeállításának testre szabása
A színskála összeállítását is testre szabhatja. Bontsa ki az **Adatszíneket** és megjelenik az adatai megjelenítéséhez használt színskála. Alapértelmezés szerint a legalacsonyabb értékű adathoz tartozik a legkevésbé telített szín, a legmagasabbhoz pedig a legtelítettebb.

A színskála sávján látható színtartomány az értékek **minimuma** és **maximuma** közötti átmeneteket mutatja. A sáv bal szélén a **legkisebb**, a jobb szélén a **legnagyobb** értékhez tartozó szín látható.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_10.png)

Más színátmenet beállításához nyissa meg a legördülő ablakot a **Minimum** vagy a **Maximum** mellett, és válassza ki a színt. A következő ábrán a **legnagyobb** értékhez tartozó szín feketére van állítva, és a színskála a **legkisebb** és a **legnagyobb** értékek közötti átmenetet mutatja.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_11.png)

Az értékek és a színek egymáshoz rendelése is módosítható. A következő ábrán a **legkisebb** és a **legnagyobb** értékhez választott két szín a narancs, illetve a zöld.

Figyelje meg az első képen, hogy a diagram oszlopai a sávon ábrázolt színátmenetet tükrözik. A legmagasabb érték zöld, a legalacsonyabb narancsszínű, a közöttük lévők pedig a skála zöld és narancs közötti árnyalatait viselik.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_12.png)

Most próbáljon meg numerikus értéket adni a **legkisebb** és a **legnagyobb** értékhez tartozó színek alatti **Minimum** és **Maximum** mezőknek (ahogyan az alábbi képen látható). Állítsa a **Minimum** és a **Maximum** értékét is 20 000 000-ra.

Ezekkel az értékekkel a színátmenet már nem alkalmazható a diagramnak a **Minimum** alatti vagy **Maximum** feletti értékeire. A **Maximum** értéknél magasabb oszlopok színe zöld, a **Minimum** alattiaké piros.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_13.png)

## <a name="use-diverging-color-scales"></a>Széttartó színskálák használata
Előfordul, hogy az adatok természetes módon széttartó jellegűek. Egy hőmérsékleti skálának például természetes középpontja a fagypont, egy jövedelmezőségi érték természetes középpontja a nulla.

Széttartó színskálák használatához állítsa a **Széttartó** csúszkát **Be** helyzetbe. A **Széttartó** beállítással újabb paletta és értékmező jelenik meg **Középérték** néven, ahogyan az alábbi képen látható.

![](media/service-tips-and-tricks-for-color-formatting/tipstrickscolor_14.png)

Amíg a **Széttartó** beállítás be van kapcsolva, a **Minimumhoz**, a **Maximumhoz** és a **Középértékhez** tartozó szín külön módosítható. A következő képen **Középértékként** 1 van megadva, ezért az 1-nél nagyobb értékek a zöld, az egynél kisebbek a piros árnyalataiban jelennek meg.

## <a name="how-to-undo-in-power-bi"></a>Művelet visszavonása a Power BI-ban
Sok más Microsoft-szolgáltatáshoz és -szoftverhez hasonlóan a Power BI is egyszerű módot kínál az utolsó parancs visszavonására. Képzelje el például, hogy megváltoztatta egy adatpont vagy adatpont-sorozat színét és a vizualizáción megjelenő szín nem teszik Önnek. Majd pedig az eredeti színt szeretné visszaállítani, csakhogy már nem emlékszik rá!

Az utolsó művelet vagy műveletek **visszavonásához** csak egyvalamit kell tennie:

- Nyomja le a Ctrl+Z billentyűkombinációt

## <a name="feedback"></a>Visszajelzés
Van egy tippje, amelyet szívesen megosztana másokkal? Kérjük, küldje el nekünk, és megvizsgáljuk, hozzáadhatjuk-e ehhez a listához.

>[!NOTE]
>A **Formátum** ikon választásával elérhető szín, tengely és kapcsolódó testreszabások a Power BI Desktopban is elérhetők.

## <a name="next-steps"></a>További lépések
[Bevezetés a színformázás és tengelytulajdonságok használatába](service-getting-started-with-color-formatting-and-axis-properties.md)

