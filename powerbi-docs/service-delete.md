---
title: Irányítópult, jelentés, munkafüzet, adatkészlet vagy munkaterület törlése
description: Tudja meg, hogy törölhet szinte bármit a Power BI szolgáltatásból
author: mihart
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 09/11/2018
ms.author: mihart
LocalizationGroup: Common tasks
ms.openlocfilehash: 770b2796eb8f29cadfe8371cb2baef12cec7c0e8
ms.sourcegitcommit: 52ac456bf2ac025b22ea634c28482f22e1cc19ac
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/10/2018
ms.locfileid: "48909897"
---
# <a name="delete-almost-anything-in-power-bi-service"></a>A Power BI szinte bármelyik elemének törlése
Ebből a cikkből megtudhatja, hogyan törölhet egy irányítópultot, jelentést, munkafüzetet, adatkészletet, alkalmazást, vizualizációt vagy munkaterületet a Power BI szolgáltatásból.

## <a name="delete-a-dashboard"></a>Irányítópult törlése
Az irányítópultok eltávolíthatók. Az irányítópult eltávolítása nem törli az alapjául szolgáló adatkészletet vagy az adott irányítópulthoz társított jelentéseket.

* Ha az irányítópultnak Ön a tulajdonosa, eltávolíthatja. Ha kollégákkal osztotta meg az irányítópultot, és törli a saját Power BI-munkaterületéről, azzal a kollégák Power BI-munkaterületeiről is törli.
* Ha megosztottak Önnel egy irányítópultot, de már nem szeretné látni, eltávolíthatja.  Ebben az esetben az irányítópult eltávolításával senki más Power BI-munkaterületéről nem távolítja el azt.
* Ha az irányítópult egy [szervezeti tartalomcsomag](service-organizational-content-pack-disconnect.md) része, csak úgy távolítható el, ha eltávolítja a kapcsolódó adatkészletet.

### <a name="to-delete-a-dashboard"></a>Az irányítópult törlése
1. Kattintson az **Irányítópultok** fülre a munkaterületén.
2. Keresse meg a törölni kívánt irányítópultot, és kattintson a Törlés ikonra ![törlés ikon](media/service-delete/power-bi-delete-icon.png).

    ![videó](media/service-delete/power-bi-delete-dash.gif)

## <a name="delete-a-report"></a>Jelentés törlése
Aggodalomra semmi ok, egy jelentés törlésével nem törlődik az adatkészlet, amelyen a jelentés alapul.  A jelentésből rögzített vizualizációk szintén megmaradnak – maradnak az irányítópulton, hacsak nem törli őket külön.

### <a name="to-delete-a-report"></a>Jelentések törlése
1. Kattintson a **Jelentések** fülre a munkaterületén.
2. Keresse meg a törölni kívánt jelentést, és kattintson a Törlés ikonra   ![törlés ikon](media/service-delete/power-bi-delete-icon.png).   

    ![a munkaterület jelentések lapja](media/service-delete/power-bi-delete-reportnew.png)
3. Erősítse meg a törlési szándékát.

   ![Jelentés törlése párbeszédpanel](media/service-delete/power-bi-delete-report.png)

   > [!NOTE]
   > Ha a jelentés egy [tartalomcsomag](service-organizational-content-pack-introduction.md) része, ezzel a módszerrel nem törölhető.  Lásd: [Szervezeti tartalomcsomaggal való kapcsolat eltávolítása](service-organizational-content-pack-disconnect.md).
   >
   >

## <a name="delete-a-workbook"></a>Munkafüzet törlése
A munkafüzetek eltávolíthatók. Egy munkafüzet eltávolításával azonban eltávolítja az összes olyan jelentést és irányítópult-csempét is, amely ennek a munkafüzetnek az adatait tartalmazza.

Ha a munkafüzetet a rendszer a OneDrive Vállalati verziójában tárolja, a POWER BI szolgáltatásból való törléssel a OneDrive-ról nem törlődik.

### <a name="to-delete-a-workbook"></a>Munkafüzetek törlése
1. Kattintson a **Munkafüzetek** fülre a munkaterületén.
2. Keresse meg a törölni kívánt munkafüzet, és kattintson a Törlés ![törlés ikon](media/service-delete/power-bi-delete-report2.png) ikonra.

    ![Munkafüzetek lap](media/service-delete/power-bi-delete-workbooknew.png)
3. Erősítse meg a törlési szándékát.

   ![Munkafüzet eltávolítása párbeszédpanel](media/service-delete/power-bi-delete-confirm.png)

## <a name="delete-a-dataset"></a>Adatkészlet törlése
Az adatkészletek törölhetők. Egy adatkészlet törlésével azonban törli az összes olyan jelentést és irányítópult-csempét is, amely az adott adatkészlet adatait tartalmazza.

Ha az adatkészlet egy vagy több [szervezeti tartalomcsomag](service-organizational-content-pack-disconnect.md) része, csak úgy törölheti, ha eltávolítja azokból a tartalomcsomagokból, ahol használatban van, megvárja, amíg a rendszer az utasítást feldolgozza, és újra megpróbálja a törlést.

### <a name="to-delete-a-dataset"></a>Az adatkészlet törlésének módja
1. Kattintson az **Adatkészletek** fülre a munkaterületén.
2. Keresse meg a törölni kívánt adatkészletet, és kattintson a három pontra (...).  

    ![Adatkészletek lap](media/service-delete/power-bi-delete-datasetnew.png)
3. A legördülő listából válassza a **Törlés** lehetőséget.

   ![három pont menü](media/service-delete/power-bi-delete-datasetnew2.png)
4. Erősítse meg a törlési szándékát.

   ![Irányítópult törlése párbeszédpanel](media/service-delete/power-bi-delete-dataset-confirm.png)

## <a name="delete-an-app-workspace"></a>Alkalmazás munkaterületének törlése
> [!WARNING]
> Egy alkalmazás-munkaterület létrehozásakor létrehoz egy Office 365-csoportot. Az alkalmazás munkaterületének törlésekor ezt az Office 365-csoportot is törli. Ez azt jelenti, hogy ha törli a csoportot, akkor törlődik a többi O365 termékből is, például a SharePointból vagy a Microsoft Teams szolgáltatásból.
>
>

Ha Ön az alkalmazás munkaterületének létrehozója, törölheti azt. Törléskor a rendszer a kapcsolódó alkalmazást az összes csoporttagnál törli, és eltávolítja az AppSource-ból is, ha az egész szervezete számára elérhetővé tette az alkalmazást. Az alkalmazás-munkaterület törlése nem azonos egy alkalmazás-munkaterület elhagyásával.

### <a name="to-delete-an-app-workspace---if-you-are-an-admin"></a>Az alkalmazás-munkaterület törlésének módja – rendszergazdaként
1. A bal oldali navigációs panelen válassza a **Munkaterületek** elemet

    ![Alkalmazás munkaterületei](media/service-delete/power-bi-delete-workspace.png)
2. Kattintson a törölni kívánt munkaterülettől jobbra található három pontra (...), és válassza a **Munkaterület szerkesztése** lehetőséget.

   ![három pont menü > Munkaterület szerkesztése](media/service-delete/power-bi-edit-workspace.png)
3. A **Munkaterület szerkesztése** ablakban válassza a **Munkaterület törlése** > **Törlés** lehetőséget.

    ![munkaterület törlése](media/service-delete/power-bi-delete-workspace2.png)

### <a name="to-remove-an-app-workspace-from-your-list"></a>Alkalmazás-munkaterület eltávolítása a listából
Ha már nem szeretne tag lenni egy alkalmazás munkaterületén, ***elhagyhatja***, és ezzel a rendszer eltávolítja azt a listájáról. Ha elhagy egy munkaterületet, a munkaterület többi tagja számára nem változik semmi.  

> [!IMPORTANT]
> Ha Ön az egyetlen rendszergazda az alkalmazás munkaterületén, a Power BI nem fogja engedélyezni, hogy elhagyja a munkaterületet.
>
>

1. Lépjen az eltávolítani kívánt alkalmazás-munkaterületre.
2. A jobb felső sarokban kattintson a három pontra (...), és válassza a **Kilépés a munkaterületről** > **Kilépés** lehetőséget.

      ![kilépés a munkaterületből](media/service-delete/power-bi-leave-workspace.png)

   > [!NOTE]
   > A legördülő listában megjelenő lehetőségek attól függnek, hogy az adott alkalmazás-munkaterületen tag-e, vagy pedig rendszergazda.
   >
   >

## <a name="delete-or-remove-an-app"></a>Egy alkalmazás törlése vagy eltávolítása
Az alkalmazások egyszerűen eltávolíthatók az alkalmazásokat listázó lapon. Véglegesen azonban csak az alkalmazás egy rendszergazdája törölhet egy alkalmazást.

### <a name="remove-an-app-from-your-app-list-page"></a>Alkalmazás eltávolításának módja az alkalmazásokat listázó lapról
Ha töröl egy alkalmazást az alkalmazásokat listázó oldalról, azzal más tagoktól nem törli az alkalmazást.

1. Nyissa meg az alkalmazásokat listázó oldalt a bal oldali navigációs panelen az **Alkalmazások** elemre kattintva.
2. Vigye a mutatót a törölni kívánt alkalmazás fölé, majd kattintson a Törlés ![](media/service-delete/power-bi-delete-report2.png) ikonra.

   ![alkalmazások kiválasztása](media/service-delete/power-bi-delete-app.png)

   Ha véletlenül távolít el egy alkalmazást, számos módon visszaszerezheti.  Megkérheti az alkalmazás létrehozóját, hogy küldje el újra, megkeresheti a hivatkozást tartalmazó eredeti e-mailt, ellenőrizheti az [Értesítési központban](service-notification-center.md), hogy listázva van-e még az alkalmazás, vagy ellenőrizheti a szervezet [AppSource](service-install-use-apps.md)-át.

## <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás
Ez a cikk bemutatta, hogyan törölheti a Power BI szolgáltatás főbb alkotóelemeit. Vannak azonban egyéb dolgok is, amelyeket törölhet a Power BI szolgáltatásban.  

* [A Kiemelt irányítópult eltávolítása](service-dashboard-featured.md)
* [Egy irányítópult eltávolítása (kedvencnek jelölés visszavonása)](service-dashboard-favorite.md)
* [Jelentésoldal törlése](service-delete.md)
* [Irányítópult csempe törlése](service-dashboard-edit-tile.md)
* [Jelentés-vizualizáció törlése](service-delete.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)
