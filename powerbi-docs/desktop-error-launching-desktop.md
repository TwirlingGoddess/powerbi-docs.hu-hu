---
title: "A Power BI Desktop indítási hibáinak elhárítása"
description: "A Power BI Desktop indítási hibáinak elhárítása"
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
ms.date: 01/24/2018
ms.author: davidi
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 43263afb63fa0350a240cae602f4a2acf8ef8edd
ms.sourcegitcommit: 4217430c3419046c3a90819c34f133ec7905b6e7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/12/2018
---
# <a name="resolve-issues-when-power-bi-desktop-will-not-launch"></a>A Power BI Desktop meghiúsult indulásával kapcsolatos hibák elhárítása
A **Power BI Desktop** esetében azok a felhasználók, akik a **Power BI helyszíni adatátjáró** korábbi verzióit telepítették és futtatják, esetenként nem tudják elindítani a Power BI Desktopot a rendszergazdai szabályzatok korlátozásai miatt, amelyeket a Power BI helyszíni adatátjáró alkalmazott a helyi gép nevesített csöveire. 

## <a name="resolve-issues-with-the-on-premises-data-gateway-and-power-bi-desktop"></a>A helyszíni adatátjáróval és a Power BI Desktoppal kapcsolatos hibák elhárítása
A helyszíni adatátjáróval kapcsolatos hibák elhárítására és a Power BI Desktop indításának engedélyezésére három lehetőség létezik:

### <a name="resolution-1-install-the-latest-version-of-power-bi-on-premises-data-gateway"></a>1. megoldás: A Power BI helyszíni adatátjáró legújabb verziójának telepítése
A Power BI helyszíni adatátjáró legújabb verziója nem helyez korlátozásokat a helyi gép nevesített csöveire, és engedi a Power BI Desktop megfelelő indítását. Ha továbbra is szeretné használni a Power BI helyszíni adatátjárót, ezt a megoldást ajánlott alkalmazni. A Power BI helyszíni adatátjáró legújabb verzióját [innen](https://go.microsoft.com/fwlink/?LinkId=698863) töltheti le. Megjegyzés: a hivatkozás egy, a futtatható telepítőre mutató közvetlen letöltési hivatkozás.

### <a name="resolution-2-uninstall-or-stop-the-power-bi-on-premises-data-gateway-windows-service"></a>2. megoldás: A Power BI helyszíni adatátjáró Windows-szolgáltatás eltávolítása vagy leállítása
Ha már nincs szüksége a Power BI helyszíni adatátjáróra, eltávolíthatja vagy leállíthatja ezt a Windows-szolgáltatást, így a szabályzat korlátozási is megszűnnek, és a Power BI Desktop indíthatóvá válik.

### <a name="resolution-3-run-power-bi-desktop-with-administrator-privilege"></a>3.megoldás: Futtassa a Power BI Desktopot rendszergazdai jogosultsággal
Harmadik lehetőségként rendszergazdai jogosultsággal is futtathatja a Power BI Desktopot, ami biztosítja annak sikeres indítását. Ekkor is javasolt azonban telepíteni a Power BI helyszíni adatátjáró legújabb verzióját, a cikkben korábban leírtaknak megfelelően.

## <a name="help-with-other-issues-when-launching-power-bi-desktop"></a>A Power BI Desktop egyéb indítási hibáival kapcsolatos támogatás
Igyekszünk a **Power BI Desktop** lehető legtöbb hibájára kitérni. Rendszeresen vizsgáljuk az olyan hibákat, amelyek több felhasználót is érintenek, és ezeket a cikkeinkben tárgyaljuk.

Ha a **Power BI Desktop** indításával kapcsolatos hiba nem kapcsolódik a helyszíni adatátjáróhoz, vagy ha a fenti megoldások nem működnek, küldhet egy hibajegyet a [Power BI támogatási csapatának](https://support.powerbi.com) (https://support.powerbi.com) a probléma azonosítása és megoldása érdekében.

A **Power BI Desktoppal** kapcsolatos egyéb esetleges jövőbeli hibák esetén (reményeink szerint ilyenek nem, vagy csak elvétve akadnak majd), hasznosnak bizonyulhat a nyomkövető és gyűjtő naplófájlok bekapcsolása a problémák hatékonyabb elkülönítése és azonosítása érdekében. A nyomkövetés bekapcsolásához válassza a **Fájl > Lehetőségek és beállítások > Beállítások**, majd a **Diagnosztika** lehetőséget, és jelölje be a **Nyomkövetés engedélyezése** beállítást a *Diagnosztikai beállítások* területen. Tisztában vagyunk vele, hogy ennek a beállításnak a megadásához a **Power BI Desktopnak** futnia kell, ezért inkább a **Power BI Desktop** indításával kapcsolatos jövőbeli problémák esetében lehet hasznos.

