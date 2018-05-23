---
title: Egyéni céges vizualizációk használata a Power BI-ban
description: Egyéni céges vizualizációk használata, kezelése és létrehozása a Power BI-ban
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 02/06/2018
ms.author: maghan
LocalizationGroup: Visualizations
ms.openlocfilehash: bc4dcc26ac2007e482b396139d572018c8a3acd3
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
---
# <a name="using-organization-custom-visuals-in-power-bi"></a>Egyéni céges vizualizációk használata a Power BI-ban

A Power BI-ban egyéni vizualizációkkal hozhat létre olyan egyedi vizualizációtípust, mely személyre szabott, vagy az átadni kívánt adatelemzésekhez van igazítva. Ezeket az egyéni vizualizációkat gyakran fejlesztők készítik, és azokat gyakran akkor hozzák létre, amikor a Power BI által tartalmazott számos látványelem nem egészen felelt meg az igényeiknek. 

Egyes szervezeteknél az egyéni vizualizációk még ennél is fontosabbak – szükségesek lehetnek a szervezet bizonyos egyedi adatainak vagy elemzéseinek átadásához, speciális adatkövetelményeik lehetnek, vagy privát üzleti eljárásokat emelhetnek ki. Az ilyen szervezeteknek egyéni vizualizációkat kell fejleszteniük, azokat meg kell osztaniuk az egész szervezetben, és gondoskodniuk kell azok megfelelő karbantartásáról. A Power BI egyéni vizualizációival a szervezetek pont ezt tehetik.

A következő képen az a folyamat látható, mely alapján a Power BI egyéni szervezeti vizualizációi a rendszergazdától a fejlesztésen és a karbantartáson át végül eljutnak az adatelemzőkhöz.

![](media/power-bi-custom-visuals-organizational/custom-visual-org-01.jpg)

A szervezeti vizualizációkat a Power BI rendszergazdája helyezi üzembe és kezeli a felügyeleti portálon. A szervezeti adattárban való üzembe helyezésük után a szervezet felhasználói könnyedén felderíthetik őket, és közvetlenül a Power BI Desktopból importálhatják az egyéni szervezeti vizualizációkat.

## <a name="using-organizational-custom-visuals"></a>Egyéni szervezeti vizualizációk használata

Az egyéni szervezeti vizualizációk a létrehozott jelentésekben való használatával kapcsolatban a következő cikkben találhat további információkat: [További információk a szervezeti vizualizációk jelentésekbe való importálásával kapcsolatban](power-bi-custom-visuals.md).
 
## <a name="administering-organizational-custom-visuals"></a>Az egyéni szervezeti vizualizációk felügyelete

Az egyéni szervezeti vizualizációk a szervezetben való felügyeletével, üzembe helyezésével és kezelésével kapcsolatban a következő cikkben találhat további információkat: [További információk az egyéni szervezeti vizualizációk üzembe helyezésével és kezelésével kapcsolatban](https://go.microsoft.com/fwlink/?linkid=866790).

> [!WARNING]
> Az egyéni vizualizációk biztonsági és adatvédelmi kockázatokat tartalmazó kódot is tartalmazhatnak. Győződjön meg arról, hogy az egyéni vizualizációk szerzője és forrása megbízható, mielőtt üzembe helyezné őket a szervezet tárházban. 
> 

## <a name="considerations-and-limitations"></a>Megfontolandó szempontok és korlátozások
 
Több szempontot és korlátozást is figyelembe kell venni.
 
Rendszergazdák:

* Az örökölt egyéni vizualizációk (mint például azok az egyéni vizualizációk, melyek nem az új verzióval ellátott API-kra épülnek) használata nem támogatott

* Ha egy egyéni vizualizációt törölnek a tárházból, leáll minden olyan meglévő jelentés megjelenítése, mely a törölt vizualizációt használja. A tárházból való törlési művelet nem vonható vissza. Az egyéni vizualizációk ideiglenes letiltásához használja a „Letiltás” funkciót.
 
Végfelhasználók:

* A Power BI-munkaterület-csoport szervezeti vizualizációkhoz való használata nem támogatott

* Az AppSource piactérről származó Visio vizualizáció, PowerApps vizualizáció és GlobeMap vizualizáció nem jelenik meg, ha a szervezet tárházának használatával van üzembe helyezve
