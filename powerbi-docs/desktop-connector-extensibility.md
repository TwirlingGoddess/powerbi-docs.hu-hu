---
title: Összekötők bővíthetősége a Power BI-ban
description: Az összekötők bővíthetősége, funkciói, biztonsági beállításai és a hitelesített összekötők
author: cpopell
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 07/25/2018
ms.author: gepopell
LocalizationGroup: Connect to data
ms.openlocfilehash: c63357df043ff6a646562d398a07d8042dd5a0ee
ms.sourcegitcommit: 7fb0b68203877ff01f29724f0d1761d023075445
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/26/2018
ms.locfileid: "39256571"
---
# <a name="connector-extensibility-in-power-bi"></a>Összekötők bővíthetősége a Power BI-ban

A Power BI-ban az ügyfelek és a fejlesztők számos módon kiterjeszthetik az adatforrásokat, amelyekhez kapcsolódhatnak, például meglévő összekötőkkel és általános adatforrásokkal (ODBC, OData, Oledb, Web, CSV, XML, JSON). A fejlesztők ezeken az adatforrásokon kívül adatkiterjesztéseket hozhatnak létre (más néven **egyéni összekötőket**), az összekötőkből pedig hitelesítés útján **hitelesített összekötőket** készíthetnek.

A Power BI korábbi verzióiban az **egyéni összekötők** egy szolgáltatáskapcsolóval voltak használhatók. Mostantól elérhető egy olyan menü, amelyben biztonságosan vezérelhető a rendszeren futtatandó egyéni kód szintje: minden egyéni összekötő, vagy csak azok a hitelesített összekötők, amelyeket a Microsoft **Adatok lekérése** párbeszédpanelje oszt el.

## <a name="custom-connectors"></a>Egyéni összekötők

Az **egyéni összekötők** számos lehetőséget hordoznak magukban a kis méretű, üzleti szempontból kritikus API-któl kezdve a nagyszabású, iparágra jellemző szolgáltatásokig, amelyeket a Microsoft még nem vezetett be. Az ilyen összekötők nagy részét maga a szállító terjeszti, így ha Önnek egy adott adatösszekötőre van szüksége, célszerű a szállítóval felvennie a kapcsolatot.

**Egyéni összekötők** használatához helyezze őket a *\[Dokumentumok]\\Power BI Desktop\\Egyéni összekötők* mappába, majd a következő szakaszban ismertetettek szerint módosítsa a biztonsági beállításokat.

A **hitelesített összekötők** használatához nem kell módosítania a biztonsági beállításokat.

## <a name="data-extension-security"></a>Adatkiterjesztés biztonsága

Az adatkiterjesztések beállításainak módosításához a **Power BI Desktopban** válassza a **Fájl > Lehetőségek és beállítások > Lehetőségek > Biztonság** elemet.

![Annak szabályozása, hogy betölthet-e adatkiterjesztési biztonsági beállításokkal rendelkező egyéni összekötőket](media/desktop-connector-extensibility/data-extension-security-1.png)

Az **Adatkiterjesztések** területen két biztonsági szint közül választhat:

* (Ajánlott) Csak a tanúsítvánnyal rendelkező bővítmények betöltésének engedélyezése
* (Nem ajánlott) Bármilyen bővítmény betöltésének engedélyezése figyelmeztetés nélkül

Ha **egyéni összekötőket** vagy olyan összekötőket szeretne használni, amelyeket Ön vagy egy külső fél fejlesztett és terjeszt, válassza a **(Nem ajánlott) Bármilyen bővítmény betöltésének engedélyezése figyelmeztetés nélkül** lehetőséget. Nem javasoljuk ezt a biztonsági beállítást, hacsak nem **egyéni összekötőket** szeretne futtatni.

Az **(Ajánlott)** biztonsági beállítás esetén, ha egyéni összekötők találhatók a rendszerén, egy hibaüzenet jelenik meg, amely leírja a biztonsági okokból nem betölthető összekötőket.

![Egy párbeszédpanel ismerteti azokat az egyéni összekötőket, amelyek biztonsági okokból nem tölthetők be, ebben az esetben a TripPint](media/desktop-connector-extensibility/data-extension-security-2.png)

A hiba elhárításához és az összekötők használatához módosítania kell a biztonsági beállításokat a **(Nem ajánlott)** beállításra a korábban ismertetett módon, majd újra kell indítania a **Power BI Desktopot**.

## <a name="certified-connectors"></a>Hitelesített összekötők

Az adatkiterjesztések korlátozott részhalmazát **hitelesítettnek** tekintjük, az ilyen hitelesített összekötők pedig az **Adatok lekérése** párbeszédpanelen érhetők el, az ezek fenntartásáért és támogatásáért felelős fél azonban továbbra is az összekötőt létrehozó külső fél. Bár a Microsoft kínál ilyen összekötőket, nem vállalunk felelősséget a teljesítményükért és a folyamatos működésükért.

Ha hitelesíteni szeretne egy egyéni összekötőt, kérje meg a szállítót, hogy lépjen kapcsolatba a Microsofttal.
