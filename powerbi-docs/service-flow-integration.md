---
title: "Oktatóanyag: A Power BI és a Microsoft Flow integrálása"
description: "Tanulja meg, hogyan hozhat létre Power BI- adatriasztások által indított folyamatokat."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: YhmNstC39Mw
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/30/2017
ms.author: mihart
ms.openlocfilehash: efab2e6be1d376a0da70c13bb66144ba34afa58c
ms.sourcegitcommit: f2b38777ca74c28f81b25e2f739e4835a0ffa75d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/17/2017
---
# <a name="microsoft-flow-and-power-bi"></a>A Microsoft Flow és a Power BI

A [Microsoft Flow](https://flow.microsoft.com/en-us/documentation/getting-started) SaaS-szolgáltatással munkafolyamatokat automatizálhat az üzleti felhasználók által használt, egyre növekvő számú alkalmazás és SaaS-szolgáltatás között. A Flow segítségével kedvenc alkalmazásait és szolgáltatásait (többek között a Power BI-t) integrálva automatizálhatja az értesítések küldését, a fájlok szinkronizálását, az adatgyűjtést és még sok más feladatot. A munkafolyamatok automatizálásával egyszerűbben végezhetők el az ismétlődő feladatok.

[Kezdjen el megismerkedni a Flow-val most.](https://flow.microsoft.com/documentation/getting-started)

Nézze meg, hogyan hoz létre Sirui egy olyan folyamatot, amely részletes e-mailt küld a munkatársainak, amikor valamilyen esemény adatriasztást vált ki a Power BI-ban. Ha végzett, a videó alatti részletes útmutatást követve próbálja ki Ön is.

<iframe width="560" height="315" src="https://www.youtube.com/embed/YhmNstC39Mw" frameborder="0" allowfullscreen></iframe>

## <a name="create-a-flow-that-is-triggered-by-a-power-bi-data-alert"></a>Power BI-adatriasztás által indított folyamat létrehozása
Ez az oktatóanyag bemutatja, hogyan hozzon létre két különböző folyamatot; az egyiket sablonból, a másikat teljesen az alapoktól. A feladat elvégzéséhez [hozzon létre egy adatriasztást a Power BI-ban](service-set-data-alerts.md) majd [iratkozzon fel a Microsoft Flow](https://flow.microsoft.com/en-us/#home-signup) szolgáltatásra (ingyenes).

## <a name="create-a-flow-that-uses-power-bi---from-a-template"></a>Power BI-t használó folyamat létrehozása sablonból
Ennek a feladatnak a végrehajtása során sablon alapján hozunk létre egy egyszerű folyamatot, amelyet egy Power BI-adatriasztás (értesítés) indít majd el.

1. Jelentkezzen be a Microsoft Flow-ba (flow.microsoft.com).
2. Kattintson a **Saját folyamatok** lehetőségre.
   
   ![](media/service-flow-integration/power-bi-my-flows.png)
3. Kattintson a **Létrehozás sablonból** lehetőségre.
   
    ![](media/service-flow-integration/power-bi-template.png)
4. A keresőmezőt használva keressen Power BI-sablonokat, majd válassza ki az **Adatvezérelt Power BI-riasztás esetén üzenet közzététele egy Slack-csatornában** lehetőséget.
   
    ![](media/service-flow-integration/power-bi-template2.png)
5. Kattintson a **Sablon használata** lehetőségre.
   
   ![](media/service-flow-integration/power-bi-use-template.png)
6. Amikor a rendszer kéri, a **Bejelentkezésre** kattintva csatlakozzon a Slackhez és a Power BI-hoz, és kövesse az utasításokat. Egy zöld pipa jelzi, ha be van jelentkezve.  Miután jóváhagyta a kapcsolatokat, válassza a **Folytatás** lehetőséget.
   
   ![](media/service-flow-integration/power-bi-flow-signin.png)

### <a name="build-the-flow"></a>A folyamat létrehozása
Ez a sablon egy triggerből (Power BI-adatriasztás újabb ír olimpiai érem megszerzésekor) és egy műveletből (Slack-üzenet feladása) áll. Amikor kiválaszt egy mezőt, a Flow megjelenít egy dinamikus tartalmat, amit belefoglalhat az üzenetbe.  Ebben a példában a csempe értékét és a csempe URL-címét foglaljuk bele az üzenet szövegébe.

![](media/service-flow-integration/power-bi-flow-template.png)

1. A triggerek legördülő menüjéből válassza ki a Power BI-adatriasztás lehetőséget. Válassza az **Új érem Írországnak** (New medal for Ireland) lehetőséget. A riasztások létrehozásával kapcsolatban tekintse meg a [Power BI-beli adatriasztásokról](service-set-data-alerts.md) szóló cikket.
   
   ![](media/service-flow-integration/power-bi-trigger-flow.png)
2. A Slackbe történő feladáshoz adja meg egy csatorna nevét és az üzenet szövegét (a Flow által létrehozott alapértelmezett üzenetet is választhatja). Látni fogja, hogy a rendszer megjeleníti az üzenet szövegébe foglalt dinamikus tartalmat.
   
   > [!NOTE]
   > Írja be az "@" jelet a csatornanév elejére.  Például ha a Slack-csatorna neve "channelA", a Flowban a "@channelA"-t kell beírni.
   > 
   > 
   
   ![](media/service-flow-integration/power-bi-flow-slacker.png)
3. Ha elkészült, válassza a **Folyamat létrehozása** vagy a **Folyamat mentése** lehetőséget.  A rendszer létrehozza és ellenőrzi a folyamatot.  A Flow értesíteni fogja, ha hibát észlel.
4. Hibák esetén a **Folyamat szerkesztése** lehetőségre kattintva hárítsa el azokat. Ha nincsenek hibák, a **Kész** gombra kattintva futtathatja az új folyamatot.
   
   ![](media/service-flow-integration/power-bi-flow-running.png)
5. Az üzenet megtekintéséhez nyissa meg Slack-fiókját.  
   
   ![](media/service-flow-integration/power-bi-slack-message.png)

## <a name="create-a-flow-that-uses-power-bi---from-scratch-blank"></a>Power BI-t használó folyamat létrehozása sablon nélkül
Ennek a feladatnak a végrehajtása során sablon nélkül hozunk létre egy egyszerű folyamatot, amelyet egy Power BI-adatriasztás (értesítés) indít majd el.

1. Jelentkezzen be a Microsoft Flow-ba.
2. Kattintson a **Saját folyamatok** > **Üres folyamat létrehozása** lehetőségre.
   
   ![](media/service-flow-integration/power-bi-my-flows.png)
3. A keresőmezőt használva keressen rá a Power BI-triggerekre, majd válassza a **Folyamat aktiválása adatvezérelt Power BI-riasztás esetén** lehetőséget.

### <a name="build-your-flow"></a>A folyamat létrehozása
1. A legördülő listából válassza ki a riasztás nevét.  A riasztások létrehozásával kapcsolatban tekintse meg a [Power BI-beli adatriasztásokról](service-set-data-alerts.md) szóló cikket.
   
    ![](media/service-flow-integration/power-bi-totalstores.png)
2. Kattintson az **Új lépés** > **Művelet hozzáadása** lehetőségre.
   
   ![](media/service-flow-integration/power-bi-new-step.png)
3. Keressen rá az **Outlook** kifejezésre, majd kattintson a **Create event** (Esemény létrehozása) lehetőséget tartalmazó találatra.
   
   ![](media/service-flow-integration/power-bi-create-event.png)
4. Töltse ki az eseményhez kapcsolódó mezőket. Amikor kiválaszt egy mezőt, a Flow megjelenít egy dinamikus tartalmat, amit belefoglalhat az üzenetbe.
   
   ![](media/service-flow-integration/power-bi-flow-event.png)
5. Ha elkészült, kattintson a **Folyamat létrehozása** lehetőségre.  A Flow menti és ellenőrzi a folyamatot. Ha nincsenek hibák, a **Kész** gombra kattintva tudja futtatni a folyamatot.  Az új folyamatot a rendszer felveszi a **Saját folyamatok** lapra.
   
   ![](media/service-flow-integration/power-bi-flow-running.png)
6. Amikor egy Power BI-adatriasztás elindítja a folyamatot, az alábbihoz hasonló Outlook-eseményértesítést fog kapni.
   
    ![](media/service-flow-integration/power-bi-flow-notice.png)

## <a name="next-steps"></a>Következő lépések
* [Microsoft Flow ‒ első lépések](https://flow.microsoft.com/en-us/documentation/getting-started/)
* [Adatriasztások beállítása a Power BI szolgáltatásban](service-set-data-alerts.md)
* [Adatriasztások beállítása az iPhone-on](mobile-set-data-alerts-in-the-mobile-apps.md)
* [Adatriasztások beállítása a Windows 10-hez készült Power BI mobilalkalmazásban](mobile-set-data-alerts-in-the-mobile-apps.md)
* További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

