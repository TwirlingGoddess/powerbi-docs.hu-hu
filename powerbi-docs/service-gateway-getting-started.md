---
title: "Első lépések Power BI-átjárókkal"
description: "Alapvető ismeretek a Power BI-adatátjárókról."
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
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 01/24/2018
ms.author: davidi
LocalizationGroup: Gateways
ms.openlocfilehash: e56af5ae1c59afc7d7aef01450bb1c778eb70b14
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="getting-started-with-power-bi-gateways"></a>Első lépések Power BI-átjárókkal
Üdvözli az **Első lépések Power BI-átjárókkal** útmutató. Ez a rövid útmutató megismerteti Önnel az átjáró szerepét és működését, valamint egy saját átjáró telepítését, konfigurálását és üzemeltetését.  

![](media/service-gateway-getting-started/gw_gettingstarted_0a.png)

Az átjárók témája olykor technikai jellegű, és mivel minden hálózat és vállalat más, az átjárók kérdése nagyon összetett is lehet. Ezt a bonyolultságot kívánjuk mérsékelni azzal, hogy az alapokkal kezdjük.

## <a name="how-power-bi-gateways-work"></a>A Power BI-átjárók működése
Az **átjáró** olyan szoftver, amely lehetővé teszi, hogy a helyszíni privát hálózaton lévő adatok elérhetőek legyenek az olyan felhőszolgáltatásokban, mint például a Power BI. Kapuőrként figyeli a kapcsolódási kérelmeket és csak akkor engedélyezi azokat, ha a felhasználói kérelem eleget tesz bizonyos feltételeknek (például hogy jogosult az átjáró használatára). A vállalatok így helyszíni hálózatukon tarthatják adatbázisaikat és -tárházaikat, mégis biztonságosan használhatják ezeknek az adatoknak a egyes részeit meggyőző jelentések és irányítópultok létrehozására a Power BI-ban.

Az átjárók a rajtuk áthaladó összes adat és az adatforrásokhoz való kapcsolódáshoz használt összes jelszó titkosításával és tömörítésével is szolgálják az adatokhoz való biztonságos hozzáférést. Mindez bizonyára egyértelműnek tűnik, de sok részletet is figyelembe kell venni.

Olykor szüksége lehet egy saját átjáróra – lehet egy nagy Excel-munkafüzete és három SQL-adatbázisa több év folyamatos értékesítési és marketing-adatával, és létre szeretne hozni egy Power BI-irányítópultot, amely minden szempontból bemutatja ezeket az eredményeket. Egyedül Ön készít jelentéseket, az Excel-munkafüzet az Öné, és csak Ön használja ezeket az adatbázisokat Power BI-jelentések készítéséhez. Az átjáró csak személyes használatra kell, nem pedig arra, hogy másokkal ossza meg ezeket az adatforrásokat.

Egy másik eset, hogy az Ön vállalata sokféle, különböző szállítóktól származó, például Analysis Services, SAP, Oracle, IBM adatbázist és más adatforrásokat használ, és ezekhez sok embernek kell hozzáférnie, hogy sokféle jelentést készítsenek. Ilyenkor olyan átjáróra van szükség, amelyen konfigurálni tudja a forrásokhoz való hozzáféréseket, és amelyet a vállalat sok tagjával meg kell osztania. Ez egy egészen másfajta átjáró.

Szerencsére a Power BI két átjárót kínál, amelyek kitűnő megoldást kínálnak erre a két helyzetre. A Power BI által kínált két átjáró a következő:

* **Helyszíni adatátjáró (személyes mód)** – egyetlen felhasználónak teszi lehetővé, hogy kapcsolódjon a forrásokhoz, és nem osztható meg másokkal. Csak a Power BI-jal használható.
* **Helyszíni adatátjáró** – Több felhasználónak teszi lehetővé a kapcsolódást több helyszíni adatforráshoz, használhatják Power BI-, PowerApps-, Flow- és Azure Logic-alkalmazások is, és mindehhez elég egyetlen átjárót telepíteni.

Mindkét átjáró hasonló feladatot lát el – biztosítja a hozzáférést a helyszíni privát hálózaton lévő adatokhoz, hogy azok használhatók legyenek olyan felhőalapú szolgáltatásokban, mint a Power BI. A személyes átjárót csak egy személy és csak a Power BI, a **helyszíni adatátjárót** sok felhasználó és sok szolgáltatás használhatja.

Az átjáró üzembe helyezése három szakaszból áll:

* Az átjáró telepítése
* Felhasználók hozzáadása az átjáróhoz (hogy használhassák az átjárót)
* Kapcsolódás adatforrásokhoz

Az átjáró használata lehetővé tesz még valamit, ami fontos lehet:

* Helyszíni adatok frissítése, hogy a Power BI jelentések tartalma is frissülhessen

Az adatfrissítés azt jelenti, hogy a Power BI-irányítópultok és -jelentések naprakészek és a legújabb adatokat tükrözik. Így amikor valaki megtekint egy helyszíni adatokkal létrehozott jelentést, akkor az a legfrissebb információkat mutatja még akkor is, ha már régebben lett létrehozva.

Az első szakasz, az átjáró telepítése egyszerű. A felhasználóknak engedélyt adni az átjáróhoz szintén egyszerű – elég hozzáadni őket a Power BI egy párbeszédablakában, és máris igénybe vehetik. Az adatforrásokhoz való kapcsolódás összetett lehet, hiszen nagyon sok adatforrás van, mindegyik a maga kapcsolódási követelményeivel és apró sajátosságaival. A frissítést egy másik útmutató tárgyalja, hogy ez a cikk az átjárókra összpontosíthasson.

Kezdjük az egyszerű résszel, és tekintsük át az átjáró telepítését.

## <a name="install-the-gateway"></a>Az átjáró telepítése
Átjáró telepítéséhez nyissa meg a Power BI szolgáltatást (ezzel a hivatkozással elindíthatja a Power BI szolgáltatást a böngészőjében és bejelentkezhet) és jelentkezzen be Power BI-fiókjával. A Power BI szolgáltatásban válassza a jobb felső sarokban lévő **letöltés ikont**, ahogyan az alábbi ábrán látható, majd az **Adatátjáró** lehetőséget.

![](media/service-gateway-getting-started/gw_gettingstarted_01.png)

Ezzel átkerül a letöltési oldalra, ahol az **Átjáró letöltése** gombra kattintva elindíthatja a letöltést.

![](media/service-gateway-getting-started/gw_gettingstarted_02.png)

Ezen a képernyőn az átjáró szerepének rendkívül tömör leírása is olvasható. Tartalmaz néhány fontos **figyelmeztetést** is – a telepített átjáró azon számítógépen fog futni, amelyiken a telepítést végzi. Ha ezt a számítógépet kikapcsolják, akkor az átjárót is (tehát nem fog működni, amíg nem fut). Vezeték nélküli hálózatot használó számítógépre telepíteni nem a legjobb megoldás. Érdemes vezetékes hálózathoz csatlakozó számítógépet használni.

Amikor készen áll, a **Tovább** gombra kattintva folytathatja a telepítést.

![](media/service-gateway-getting-started/gw_gettingstarted_03.png)

Ekkor kell eldöntenie, hogy milyen átjárót telepít – helyszíni vagy személyes átjárót. Ez az útmutató a **Helyszíni adatátjáró** telepítését mutatja be.

A döntéshozásnál figyelembe kell vennie néhány szempontot:

* Mindkét átjárótípus használatához 64 bites Windows operációs rendszer szükséges.
* Az átjárók tartományvezérlőre nem telepíthetők.
* Egyazon számítógépre két helyszíni adatátjáró telepíthető, üzemmódonként (helyszíni vagy személyes) egy-egy. 
* Egyazon számítógépen nem futtatható két ugyanolyan módban üzemelő átjáró.
* Ha több különböző számítógépre is telepít helyszíni átjárókat, azokat egy közös Power BI átjárófelügyeleti felületen keresztül felügyelheti (a személyes átjárók kivételével – lásd a következő pontot).
* Power BI-felhasználónként csak egy személyes módú átjáró futtatható. Ha egy második személyes módú átjárót telepít egy adott felhasználó számára – akár egy másik számítógépen is –, a legutóbbi telepítés a korábbi telepítések helyébe lép.

A **Tovább** gombra kattintva megkezdődik a telepítés. Meg kell adnia a telepítés helyét, és általában az alapértelmezett hely a legmegfelelőbb.

![](media/service-gateway-getting-started/gw_gettingstarted_06.png)

A telepítés folyamata gyors, és egy folyamatjelzőn követhető.

![](media/service-gateway-getting-started/gw_gettingstarted_06a.png)

Közvetlenül a befejeződése előtt meg kell adnia az átjáróhoz használandó fiókot. Ez az a fiók (felhasználónév és jelszó) legyen, amellyel a Power BI-ba bejelentkezik. Az átjáró a Power BI-fiókjához társul és Ön a Power BI szolgáltatásból fogja konfigurálni az átjárókat.

![](media/service-gateway-getting-started/gw_gettingstarted_07.png)

A rendszer bejelentkezteti, ahogyan a következő képen látható.

![](media/service-gateway-getting-started/gw_gettingstarted_08.png)

Bejelentkezés után létre kell hoznia egy **helyreállítási kulcsot**. A helyreállítási kulcsról egy másik cikk szól részletesebben, egyelőre elég annyit tudnia, hogy az átjáró helyreállításához vagy áthelyezéshez szükséges.

![](media/service-gateway-getting-started/gw_gettingstarted_09.png)

Ha minden rendben lezajlott, akkor megnyílik egy ablak, amely tudatja Önnel, hogy az átjáró készen áll.

![](media/service-gateway-getting-started/gw_gettingstarted_10.png)

Ennyiből áll egy helyszíni átjáró telepítése. Egyszerű eljárás, ahogyan ígértük. A következő lépés **felhasználók** vagy **adatforrások** hozzáadása – bármelyikkel kezdheti, és bármelyiket hozzáadhatja a kezdeti konfigurálás után is.

A következő szakasz a felhasználók hozzáadását ismerteti. Később szó lesz arról is, hogy hogyan kell adatforrásokat hozzáadni az átjáróhoz.

## <a name="add-users-to-a-gateway"></a>Felhasználók hozzáadása az átjáróhoz
A már telepített átjáró a **Power BI szolgáltatásból** kezelhető. Az átjárók kezelésére szolgáló oldalt úgy érheti el, hogy a Power BI szolgáltatásban a jobb felső sarokban lévő Fogaskerék ikont, majd az **Átjárók kezelése** lehetőséget választja.

![](media/service-gateway-getting-started/gw_gettingstarted_15.png)

A Power BI szolgáltatás vásznán belül megnyílik egy lap, amelyen az átjáróit tudja kezelni. Az **Átjáró beállításai** oldal képe a következő.

![](media/service-gateway-getting-started/gw_gettingstarted_12.png)

Ha a **Rendszergazdák** elemre koppint vagy kattint, akkor a következő, a rendszergazdák kezelésére való oldalra jut. Fontos, hogy itt csak az adható meg, hogy mely felhasználók *felügyelhetik* az átjárót. Az átjáró felhasználóinak hozzáadása (vagy eltávolítása) az egyes adatforrásokhoz egy másik – későbbi bekezdésekben ismertetett – oldalon történik.

![](media/service-gateway-getting-started/gw_gettingstarted_13.png)

Adatforrás telepítése és ellenőrzése (sikeres kapcsolódással) után az, megjelenik a hozzá társított átjáró alatt ennek az **Átjárók kezelése** képernyőnek a bal oldalán, ahogyan az alábbi ábra mutatja. Figyelje meg, hogy a jobb oldali panelen két lap közül választhat: **Adatforrás beállításai** és **Felhasználók**. A következő képen az **Adatforrás beállításai** lap látható.

![](media/service-gateway-getting-started/gw_gettingstarted_16.png)

A **Felhasználók** lehetőséget választva megjelenik egy szövegmező, amelybe beviheti a vállalati felhasználókat, akiknek hozzáférést kíván adni a kijelölt adatforráshoz. A következő képen látható, hogy Maggie és Adam hozzá van adva.

Amikor elkezd begépelni egy e-mail-címet a szövegmezőbe, a Power BI megjeleníti azoknak a felhasználóknak a listáját, akiknek az e-mail-címe megfelel a begépelt szöveggel, így azok a nevükre kattintva hozzáadhatók a listához.

E-mail-csoportok (aliasok) is felvehetők, így egyének mellett személyek csoportjainak is adhat hozzáférést.

![](media/service-gateway-getting-started/gw_gettingstarted_17.png)

Amikor a **Hozzáadás** lehetőségre kattint, a hozzáadott tagok megjelennek a mezőben, és igény esetén továbbiakat adhat hozzá. A felhasználók eltávolítása ugyanilyen egyszerű. Elég bejelölni a nevük melletti jelölőnégyzetet, majd a mező alatti **Eltávolítás** gombra kattintani.

![](media/service-gateway-getting-started/gw_gettingstarted_18.png)

Ennyi az egész. Ne feledje, hogy a felhasználókat minden adatforráshoz hozzá kell adnia, amelyhez hozzáférést kíván adni nekik. Minden adatforrás külön felhasználólistával rendelkezik, és a felhasználókat minden adatforráshoz külön kell hozzáadni.

## <a name="adding-data-sources"></a>Adatforrások hozzáadása
Ahhoz hogy az átjáró használható legyen, természetesen adatforrásokat kell hozzáadnia. Részben ebben mutatkozik meg a Power BI-átjárók összetettsége – Sokféle adatforrás elérhető, és mindegyikhez sajátos követelmények tartoznak (gyakran saját illesztőprogramot is igényelnek).

Mielőtt átirányítanánk egy másik cikkhez, fussa át az adatforrások hozzáadását. A **Power BI szolgáltatás** **Átjárók kezelése** lapján jelölje ki az átjárót, amelyhez adatforrást kíván hozzáadni, majd válassza a lap bal felső sarkában, az átjárók listája felett található **Adatforrás hozzáadása** lehetőséget.

Ekkor a jobb oldali panelen megjelenik az **Adatforrás beállításai** panel, ahogyan a következő képen látható. Itt elnevezheti az adatforrást (az **Adatforrás neve** mezőbe gépelve) és kiválaszthatja a típusát az **Adatforrás típusa** legördülő listából.

![](media/service-gateway-getting-started/gw_gettingstarted_14.png)

Az átjáró telepítésével tehát végzett, és készen áll az adatforrások hozzáadására. Kitűnő! A következő bekezdésben felsorolt forrásokban más hasznos információ mellett megtalálja az adatforrások ismertetését és az átjárók használatának részletesebb leírását.

## <a name="next-steps"></a>További lépések
[Helyszíni adatátjáró használata](service-gateway-onprem.md)  
[Helyszíni adatátjáró – részletes](service-gateway-onprem-indepth.md)  
[Helyszíni adatátjáró (személyes mód)](service-gateway-personal-mode.md)
[Helyszíni adatátjáró hibaelhárítása](service-gateway-onprem-tshoot.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

