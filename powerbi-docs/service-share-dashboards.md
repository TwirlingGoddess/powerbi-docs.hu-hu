---
title: "Irányítópult megosztása munkatársakkal és másokkal – Power BI"
description: "Tudnivalók Power BI-irányítópultoknak a cégen belüli és kívüli munkatársakkal való megosztásáról és általában a megosztásról."
services: powerbi
documentationcenter: 
author: maggiesMSFT
manager: kfile
backup: ajayan
editor: 
tags: 
featuredvideoid: 0tUwn8DHo3s
qualityfocus: monitoring
qualitydate: 08/14/2017
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/08/2018
ms.author: maggies
ms.openlocfilehash: d0fbe2ca891096cf8b1ae2145260c3341c451658
ms.sourcegitcommit: 804ee18b4c892b7dcbd7d7d5d987b16ef16fc2bb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/09/2018
---
# <a name="share-your-power-bi-dashboards-with-coworkers-and-others"></a>Irányítópult megosztása munkatársakkal és másokkal
A *Megosztással* egyszerűen biztosíthatja néhány személy hozzáférését az irányítópultjaihoz és jelentéseihez. A Power BI-ban [többféle módon valósítható meg az irányítópultok közös használata és terjesztése](service-how-to-collaborate-distribute-dashboards-reports.md), amelyek közül a megosztás csak az egyik lehetőség.

![Megosztás ikon az irányítópultok listájában](media/service-share-dashboards/power-bi-share-dash.png)

Akár a cégen belül, akár azon kívül oszt meg tartalmat, a megosztáshoz Önnek és a címzetteknek is [Power BI Pro-licencre](service-free-vs-pro.md) van szükségük, vagy pedig a tartalomnak kell egy [Prémium-kapacitásban](service-premium.md) lennie. Javaslatai vannak? A Power BI csapata mindig szívesen fogadja visszajelzését, amelyet a [Power BI-közösség webhelyén](https://community.powerbi.com/) küldhet el.

Irányítópultot megoszthat saját munkaterületéről vagy egy alkalmazás munkaterületéről. A megosztott irányítópultot a címzettjei megtekinthetik és használhatják, de nem szerkeszthetik. Az irányítópultok és a jelentések adatait ugyanúgy látják, ahogyan Ön is, hacsak nem alkalmaz [sorszintű biztonságot (RLS-t)](service-admin-rls.md). A munkatársai, akikkel megosztotta az irányítópultot, továbboszthatják azt másokkal, ha engedélyezi. A cégén kívüli címzettek is megtekinthetik és használhatják, de nem szerkeszthetik az irányítópultot. 

[Irányítópultot megoszthat bármely Power BI mobilalkalmazásból is](mobile-share-dashboard-from-the-mobile-apps.md). Irányítópultot megoszthat a Power BI szolgáltatásból és a Power BI-mobilalkalmazásokból, de a Power BI Desktopból nem.

## <a name="video-share-a-dashboard"></a>Videó: Irányítópult megosztása
Nézze meg, hogyan osztja meg Amanda az irányítópultját cégen belüli és azon kívüli munkatársaival. Ez után próbálja ki Ön is a videó alatt látható részletes utasítások szerint.

<iframe width="560" height="315" src="https://www.youtube.com/embed/0tUwn8DHo3s?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

## <a name="share-a-dashboard"></a>Irányítópult megosztása
1. Nyisson meg egy irányítópultot a saját munkaterületén vagy egy alkalmazásén, majd válassza a **Megosztás** lehetőséget ![Megosztás ikon](media/service-share-dashboards/power-bi-share-icon.png).
2. A felső mezőbe írja be a személyek, terjesztési csoportok vagy biztonsági csoportok teljes e-mail-címét. Dinamikus terjesztési listákkal nem oszthat meg irányítópultot. 
   
   A megosztás címzettjei lehetnek a cégen kívüli címmel rendelkező személyek is, de ilyenkor figyelmeztetés jelenik meg.
   
   ![Figyelmeztetés külső megosztás esetén](media/service-share-dashboards/power-bi-share-dialog-warning.png)  
3. Ha kívánja, hozzáfűzhet egy üzenetet. Ez nem kötelező.
4. Jelölje be az **Irányítópult megosztásának engedélyezése a címzetteknek** lehetőséget, hogy a munkatársai megoszthassák másokkal az irányítópultját.
   
   A mások általi megosztás neve *újraosztás*. Akiknek engedélyezi, azok újraoszthatják az irányítópultot a Power BI szolgáltatásból vagy mobilalkalmazásokból, vagy továbbíthatják a meghívó e-mailt a cégen belüli más személyeknek. A meghívó egy hónap után lejár. A cégen kívüli személyek nem tudnak újraosztani. Ön az irányítópult tulajdonosaként kikapcsolhatja, vagy egyénenként megvonhatja az újraosztás lehetőségét az alábbi, [Irányítópult megosztásának megszüntetése vagy mások általi megosztásának megakadályozása](service-share-dashboards.md#stop-sharing-a-dashboard-or-stop-others-from-sharing) című részben leírtak szerint.
5. Válassza a **Megosztás** lehetőséget.
   
   ![Megosztás gomb választása](media/service-share-dashboards/power-bi-share-dialog-share.png)  
   
   A Power BI a megosztott irányítópultra mutató hivatkozást tartalmazó e-mailt küld az egyéni felhasználóknak, de a csoportoknak nem. Üzenet jelenik meg a **sikeres** végrehajtásról. 
   
   Amikor egy cégen belüli címzett a hivatkozásra kattint, a Power BI hozzáadja az irányítópultot a az ő **Velem megosztva** listázó oldalához. A címzett az Ön nevét kijelölve megtekintheti az összes Ön által megosztott irányítópultot. 
   
   ![Velem megosztva listázó oldal](media/service-share-dashboards/power-bi-shared-with-me-list-page.png)
   
   Amikor egy cégen kívüli címzett a hivatkozásra kattint, akkor látni fogja az irányítópultot, de nem a szokásos Power BI-portálon. További részletek: [Irányítópult megosztása cégen kívüli személyekkel](service-share-dashboards.md#share-a-dashboard-with-people-outside-your-organization).

## <a name="who-has-access-to-a-dashboard-you-shared"></a>Ki fér hozzá a megosztott irányítópulthoz?
Előfordul, hogy tudnia kell, kikkel osztott meg egy irányítópultot, és hogy ők kivel osztották újra.

1. Az irányítópultok listájában vagy magán az irányítópulton válassza a **Megosztás** lehetőséget ![Megosztás ikon](media/service-share-dashboards/power-bi-share-icon.png). 
2. Az **Irányítópult megosztása** párbeszédablakban válassza a **Hozzáférés** lehetőséget.
   
    ![Megosztás párbeszédablak, Hozzáférés lap](media/service-share-dashboards/power-bi-share-dialog-access.png)
   
    A cégen kívüli személyek **Vendég** hozzáféréssel jelennek meg.

## <a name="stop-sharing-a-dashboard-or-stop-others-from-sharing"></a>Irányítópult megosztásának megszüntetése vagy mások általi megosztásának megakadályozása
Az újraosztást csak az irányítópult tulajdonosa kapcsolhatja be és ki.

### <a name="if-you-havent-sent-the-sharing-invitation-yet"></a>Ha még nem küldte el a megosztási meghívót
* Szüntesse meg az **Irányítópult megosztásának engedélyezése a címzetteknek** jelölőnégyzet kijelölését a meghívó alján, mielőtt elküldené.

### <a name="if-youve-already-shared-the-dashboard"></a>Ha már megosztotta az irányítópultot
1. Az irányítópultok listájában vagy magán az irányítópulton válassza a **Megosztás** lehetőséget ![Megosztás ikon](media/service-share-dashboards/power-bi-share-icon.png). 
2. Az **Irányítópult megosztása** párbeszédablakban válassza a **Hozzáférés** lehetőséget.
   
    ![Megosztás párbeszédablak, Hozzáférés lap](media/service-share-dashboards/power-bi-share-dialog-access.png)
3. Válassza az **Olvasás és újraosztás** lehetőség melletti három pontot (**...**), majd a következőt:
   
   ![Olvasás és újraosztás három pontja](media/service-share-dashboards/power-bi-change-access.png)
   
   * **Olvasás**, hogy a címzett ne oszthassa meg az irányítópultot másokkal.
   * **Hozzáférés letiltása**, hogy az adott személy ne is tekinthesse meg az irányítópultot.

4. A **Hozzáférés letiltása** párbeszédablakban arra is lehetősége van, hogy a kapcsolódó tartalmakhoz (például jelentésekhez vagy adatkészletekhez) való hozzáférést is letiltsa. Ha ilyen figyelmeztető ikonnal ![Power BI figyelmeztető ikon](media/service-share-dashboards/power-bi-warning-icon.png) rendelkező elemet távolít el, a problémamentes megjelenítés érdekében ajánlatos a kapcsolódó tartalmat is eltávolítani.

## <a name="share-a-dashboard-with-people-outside-your-organization"></a>Irányítópult megosztása cégen kívüli személyekkel
A megosztás cégen kívüli címzettjei e-mailt kapnak a megosztott irányítópultra mutató hivatkozással, és az irányítópult megtekintéséhez be kell jelentkezniük a Power BI-ba. Ha nem rendelkeznek Power BI Pro-licenccel, akkor igényelhetnek egyet, miután a hivatkozásra kattintottak.

Bejelentkezés után a bal oldali navigációs panel nélkül, a saját böngészőjükben tekinthetik meg a megosztott irányítópultot, nem pedig a szokásos Power BI-portálon. Az irányítópult jövőbeni eléréséhez menteniük kell a hivatkozást a kedvencek közé.

Ennek az irányítópultnak vagy jelentésnek a tartalmát egyáltalán nem módosíthatják. Használhatják a jelentés grafikonjait (kereszt-kiemeléshez), és megváltoztathatják az irányítópulthoz kapcsolt jelentések szűrőit/szűkítéseit, de a változásokat nem menthetik.

A megosztott irányítópultot csak a közvetlen címzettek láthatják. Ha az e-mailt például a Vicki@contoso.com címre küldte, akkor az irányítópultot csak Vicki tekintheti meg. Az irányítópultot más még a hivatkozás birtokában sem fogja látni, és Vickinek is ugyanezt az e-mail-címet kell használnia az irányítópult eléréséhez. Ha más e-mail-címmel jelentkezik be, akkor ő sem fog hozzáférni az irányítópulthoz.

A cégen kívüli személyek egyáltalán nem fogják látni az adatokat, ha szerepkör- vagy sorszintű biztonság van alkalmazva a helyszíni Analysis Services rendszerbeli táblázatos modellekben.

Ha Power BI-mobilalkalmazásból küld hivatkozást cégen kívüli címzettnek, akkor a hivatkozásra kattintva az irányítópult böngészőben fog megnyílni, nem a Power BI-mobilalkalmazásban.

## <a name="limitations-and-considerations"></a>Korlátozások és megfontolandó szempontok
Irányítópultok megosztásakor vegye figyelembe a következőket:

* Ön és a munkatársai általában ugyanazokat az adatokat látják az irányítópulton. Ha tehát Ön több adathoz jogosult hozzáférni mint ők, akkor az irányítópultján ők is látni fogják az összes adatát. Ha azonban [sorszintű biztonság (RLS)](service-admin-rls.md) van érvényben egy irányítópult alapjául szolgáló adatkészletben, akkor a hozzáférhető adatok köre az egyes személyek hitelesítő adatai alapján lesz meghatározva.
* Mindenki, akivel Ön megosztotta az irányítópultot, megtekintheti és használhatja a jelentéseket az [Olvasási nézetben](service-reading-view-and-editing-view.md). Nem hozhatnak létre jelentéseket és nem menthetik a meglévő jelentések módosításait.
* Az adatkészletet senki sem tekintheti meg vagy töltheti le.
* Manuálisan mindenki [frissítheti az irányítópult adatait](refresh-data.md).
* Ha a levelezéshez az Office 365-öt használja, akkor a megosztás címzettjeként egy terjesztési csoportot is megadhat a csoporthoz tartozó e-mail-cím beírásával.
* Az Önnel egy e-mail-tartományban lévő munkatársai, valamint a más, de ugyanazon a bérlőn belül regisztrált tartományok tagjai másokkal is megoszthatják az irányítópultot. Legyen például a contoso.com és a contoso2.com tartomány egy bérlőn belül regisztrálva. Ha az Ön e-mail-címe konrads@contoso.com, akkor ravali@contoso.com és gustav@contoso2.com egyaránt újraoszthat, ha Ön engedélyezte számukra a megosztást.
* Ha munkatársai már hozzáférnek egy adott irányítópulthoz, akkor nekik közvetlenül az irányítópultra mutató, az irányítópultról kimásolt hivatkozást is küldhet. Példa: `https://powerbi.com/dashboards/g12466b5-a452-4e55-8634-xxxxxxxxxxxx`
* Hasonló módon [a mögöttes jelentésre mutató közvetlen hivatkozást is küldhet](service-share-reports.md) az adott irányítópulthoz hozzáféréssel rendelkező munkatársaknak. 

## <a name="troubleshoot-sharing"></a>A megosztás hibaelhárítása

### <a name="my-dashboard-recipients-see-a-lock-icon-in-a-tile-or-a-permission-required-message"></a>Az irányítópult címzettjeinek lakat ikon vagy „Engedély szükséges” szöveg jelenik meg a címben

Előfordulhat, hogy a megosztás címzettjeinek lakat ikon vagy „Engedély szükséges” szöveg jelenik meg a címben, amikor meg akarják nézni a jelentést.

![Blokkolt Power BI-csempe](media/service-share-dashboards/power-bi-locked_tile_small.png)

Ha ez történik, engedélyt kell adnia nekik az alapul szolgáló adatkészlethez való hozzáféréshez. Ezt a következőképp végezheti el.

1. A tartalomlistában nyissa meg az **Adatkészlet** lapot.

1. Az adatkészlet > **Engedélyek kezelése** terület mellett válassza három pontot (**...**).

    ![Engedélyek kezelése](media/service-share-dashboards/power-bi-sharing-manage-permissions.png)

3. Válassza a **Felhasználó hozzáadása** elemet.

    ![Felhasználó hozzáadása kiválasztása](media/service-share-dashboards/power-bi-share-dataset-add-user.png)

1. Írja be a személyek, terjesztési csoportok vagy biztonsági csoportok teljes e-mail-címét. Dinamikus terjesztési listákkal nem oszthat meg irányítópultot.

    ![E-mail címek hozzáadása](media/service-share-dashboards/power-bi-add-user-dataset.png)

5. Válassza a **Hozzáadás** elemet.

### <a name="i-cant-share-a-dashboard"></a>Nem tudok irányítópultot megosztani

Az irányítópult megosztásához rendelkeznie kell a mögöttes tartalmak (minden kapcsolódó jelentés és adatkészlet) újraosztásához szükséges jogosultságokkal. Ha olyan üzenetet kap, amely szerint nincs jogosultsága a megosztáshoz, forduljon a jelentés tulajdonosához, aki engedélyt adhat Önnek az adott jelentések és adatkészletek újraosztásához.


## <a name="next-steps"></a>Következő lépések
* Visszajelzés küldene? Mondja el javaslatait a [Power BI-közösség webhelyén](https://community.powerbi.com/).
* [Irányítópultok és jelentések közös használata és megosztása](service-how-to-collaborate-distribute-dashboards-reports.md)
* [Power BI-jelentés külön megosztása](service-share-reports.md)
* Kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/).

