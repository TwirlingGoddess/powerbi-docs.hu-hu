---
title: "Egyéni vizualizációk a Power BI-ban"
description: "Egyéni vizualizációk a Power BI-ban"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 11/20/2017
ms.author: mihart
ms.openlocfilehash: c50b984cd8babc845dbe0223613e463a7a8ee76d
ms.sourcegitcommit: 12236d08c27c7ee3fabb7ef9d767e9dee693f8aa
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/21/2017
---
# <a name="custom-visuals-in-power-bi"></a>Egyéni vizualizációk a Power BI-ban
Power BI-jelentések létrehozása vagy szerkesztése során számos különböző vizualizációtípus használatára van lehetősége. Ezek a vizualizációk a **Vizualizációk** ablaktáblában láthatók. A Power BI Desktop letöltésekor vagy a Power BI szolgáltatás (app.powerbi.com) megnyitásakor a vizualizációk egy készlete azonnal elérhető. 

![](media/power-bi-custom-visuals/power-bi-visualizations.png)

Ennél azonban több vizualizáció is a rendelkezésére áll. A három pontot ábrázoló gombra kattintva újabb vizualizációforrást nyithat meg, az *egyéni vizualizációkét*.

Az egyéni vizualizációkat a közösség tagjai, illetve a Microsoft hozza létre, és az [AppSource](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals) alatt vannak tárolva. Ezek a vizualizációk letölthetők, és hozzáadhatók a Power BI-jelentésekhez. Az összes egyéni vizualizáció jóvá lett hagyva a Microsoft által, és a Power BI-ban alapból megtalálható vizualizációkhoz hasonlóan működnek: szűrhetők, kiemelhetők, szerkeszthetők, megoszthatók stb. 

Mi az az AppSource? Egyszerűen szólva az a hely, ahol a Microsoft-szoftverekhez alkalmazásokat, beépülő modulokat és bővítményeket találhat. Az [AppSource](https://appsource.microsoft.com) többek között az Office 365, az Azure, a Dynamics 365, Cortana és a Power BI több millió felhasználóját köti össze olyan megoldásokkal, amelyekkel minden eddiginél hatékonyabban, mélyebb betekintéssel vagy látványosabban dolgozhatnak.

## <a name="two-types-of-custom-visuals"></a>Az egyéni vizualizációk két típusa

A Power BI AppSource webhelyen elérhető egyéni vizualizációk 2 kategóriába sorolhatók: **jóváhagyott** és **minősített**. Az *AppSource által jóváhagyott* vizualizációk futtathatók böngészőkben, jelentésekben és irányítópultokban.  A *Power BI-minősítéssel* rendelkező vizualizációk szigorú teszteken feleltek meg, és további forgatókönyvek, például [e-mailes előfizetések](service-report-subscribe.md) és [PowerPointba történő exportálás](service-publish-to-powerpoint.md) esetén is támogatottak.

A minősített egyéni vizualizációk listájának megtekintéséhez vagy saját vizualizáció közzétételéhez lásd a [minősített egyéni vizualizációkat](power-bi-custom-visuals-certified.md) ismertető szakaszt.

Ön olyan webfejlesztő, aki szeretne saját vizualizációkat létrehozni, és hozzáadni azokat az AppSource-hoz?  A [fejlesztői eszközöket ismertető](service-custom-visuals-getting-started-with-developer-tools.md) rész megtekintésével megtudhatja, hogyan [tehet közzé egyéni vizualizációkat az AppSource-on](https://appsource.microsoft.com/marketplace/apps?product=power-bi-visuals).

## <a name="download-or-import-custom-visuals-from-microsoft-appsource"></a>Egyéni vizualizáció letöltése vagy importálása a Microsoft AppSource-ról
Az egyéni vizualizációk letöltésének és importálásának két módja van. Megteheti ezt a Power BI-on belülről és az AppSource webhelyről. 

###    <a name="import-custom-visuals-from-within-power-bi"></a>Egyéni vizualizációk importálása a Power BI-on belül
1. Válassza a Vizualizációk ablaktábla alján található, három pontot ábrázoló gombot. 

    ![](media/power-bi-custom-visuals/power-bi-visualizations2.png)

2. A legördülő listából válassza az **Importálás az áruházból** lehetőséget.

    ![](media/power-bi-custom-visuals/power-bi-custom-visual-import.png)

3. Tekintse át a listát, és keresse meg az importálni kívánt vizualizációt. 

    ![](media/power-bi-custom-visuals/power-bi-import-visual.png)

4.  Az egyes vizualizációk kijelölésével további információkat tudhat meg róluk.

    ![](media/power-bi-custom-visuals/power-bi-select.png)

5.  A részletek lapon többek között képernyőképeket, videókat és részletes leírásokat tekinthet meg. 

    ![](media/power-bi-custom-visuals/power-bi-synoptic.png)

6. A képernyő alján értékelések is találhatók.

    ![](media/power-bi-custom-visuals/power-bi-reviews.png)

7.    Az egyéni vizualizáció importálásához válassza a **Hozzáadás** parancsot. Az egyéni vizualizáció ikonja ekkor megjelenik a Vizualizációk ablaktábla alján, és már használhatja is a jelentésben.

       ![](media/power-bi-custom-visuals/power-bi-custom-visual-imported.png)


###    <a name="download-and-import-custom-visuals-from-microsoft-appsource"></a>Egyéni vizualizáció letöltése és importálása a Microsoft AppSource-ról

1. A [Microsoft AppSource](https://appsource.microsoft.com) webhelyről kiindulva válassza az **Alkalmazások** lapot. 

    ![](media/power-bi-custom-visuals/power-bi-appsource-apps.png)

2. Ez átirányítja Önt az [Alkalmazások találatainak oldalára](https://appsource.microsoft.com/en-us/marketplace/apps), ahol megtekintheti az egyes kategóriák legnépszerűbb alkalmazásait, beleértve a *Power BI-alkalmazásokat*. Mi azonban egyéni vizualizációkat keresünk, szóval szűkítsük le a találatokat a bal oldali navigációs listában található **Power BI-vizualizációk** lehetőség kiválasztásával.

    ![](media/power-bi-custom-visuals/power-bi-appsource-visuals.png)

3. Az AppSource minden egyes egyéni vizualizációhoz megjelenít egy csempét.  Minden csempe tartalmaz egy képernyőképet az egyéni vizualizációról, illetve egy rövid leírást és egy letöltési hivatkozást. További részletekért kattintson a csempére. 

    ![](media/power-bi-custom-visuals/powerbi-custom-select-visual.png)

4. A részletek lapon többek között képernyőképeket, videókat és részletes leírásokat tekinthet meg. Az egyéni vizualizáció letöltéséhez kattintson a **Letöltés most** hivatkozásra, és fogadja el a használati feltételeket. 

    ![](media/power-bi-custom-visuals/power-bi-appsource-get.png)

5. Kattintson az egyéni vizualizáció letöltési hivatkozására.

    ![](media/power-bi-custom-visuals/powerbi-custom-download.png)

    A letöltési oldal az egyéni vizualizációnak a Power BI Desktopba és Power BI szolgáltatásba történő importálásával kapcsolatos utasításokat is tartalmaz.

    Egy mintajelentést is letölthet, amely tartalmazza az egyéni vizualizációt, és bemutatja annak képességeit.

    ![](media/power-bi-custom-visuals/powerbi-custom-try-sample.png)

6. Mentse a .pbiviz-fájlt, majd nyissa meg a Power BI-t.    
7. Nyissa meg a jelentést, amelyhez hozzá szeretné adni az egyéni vizualizációt, majd a **Vizualizációk** ablaktábla alján kattintson a három pontot ábrázoló gombra, és válassza az **Importálás fájlból** lehetőséget.  

      ![](media/power-bi-custom-visuals/power-bi-custom-visual-import-from-file.png)

8. Válassza ki az egyéni vizualizáció fájlját. Ezzel hozzáadja annak ikonját a **Vizualizációk** ablaktábla aljához. Az egyéni vizualizáció most már használható a jelentésben.

    ![](media/power-bi-custom-visuals/power-bi-chord.png)
    
##    <a name="considerations-and-troubleshooting"></a>Megfontolandó szempontok és hibaelhárítás


- Az egyéni vizualizáció az importálásakor az adott jelentéshez lesz hozzáadva. Ha egy másik jelentésben is használni szeretné a vizualizációt, abba a jelentésbe is importálnia kell. Ha egy egyéni vizualizációval rendelkező jelentést a **Mentés másként** lehetőséggel ment, az új jelentéssel együtt az egyéni vizualizáció egy másolata is mentve lesz.

- Ha nem látja a **Vizualizációk** ablaktáblát, akkor nem rendelkezik a jelentés szerkesztéséhez szükséges engedélyekkel.  Csak azokhoz a jelentésekhez adhat hozzá egyéni vizualizációkat, amelyek szerkesztésére jogosult, az Önnel megosztott jelentésekhez nem.


További kérdései vannak? [Forduljon a Power BI közösségéhez](http://community.powerbi.com/)

