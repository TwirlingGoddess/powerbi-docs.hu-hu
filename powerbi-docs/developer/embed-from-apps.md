---
title: Jelentések és irányítópultok beágyazása alkalmazásokból
description: Megtudhatja, hogyan integrálhat vagy ágyazhat be egy jelentést vagy irányítópultot egy Power BI-alkalmazásból, és nem az alkalmazás-munkaterületről.
author: markingmyname
ms.author: maghan
ms.date: 07/13/2018
ms.topic: how-to
ms.service: powerbi
ms.component: powerbi-developer
ms.custom: mvc
manager: kfile
ms.openlocfilehash: 2817ccb25fc9aa6d3e8150c776558366dcf0ccb6
ms.sourcegitcommit: 0c870a006e525447497e678484874a2f137b9abd
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/17/2018
ms.locfileid: "39088839"
---
# <a name="embed-reports-or-dashboards-from-apps"></a>Jelentések és irányítópultok beágyazása alkalmazásokból

A **Power BI**-ban létrehozhat a összetartozó **irányítópultokat** és **jelentéseket** egy helyen összefűző alkalmazásokat, majd közzéteheti azokat a vállalatban nagy csoportok számára elérhetően. Ezeknek az alkalmazásoknak a használata akkor releváns, ha minden felhasználó Power BI-felhasználó, tehát megoszthatja velük a tartalmakat Power BI-alkalmazásokkal. Szeretnénk ismertetni néhány gyors lépést arról, hogyan végezheti el tartalom beágyazását egy közzétett Power BI-alkalmazásból egy külső fél alkalmazásába.

## <a name="how-to-grab-report-embed-url-for-embedding"></a>Jelentés beágyazási URL-címének megragadása beágyazáshoz

1. Hozza létre az alkalmazás egy példányát egy felhasználói munkaterületen (Saját munkaterület) úgy, hogy megosztja azt saját magával, vagy végigvezet egy másik felhasználót ezen a folyamaton.

2. Nyissa meg a kívánt jelentést a Power BI szolgáltatásban.

3. Lépjen a Fájl -> Beágyazás a SharePoint Online-ban szakaszba, és ragadja meg a jelentés beágyazási URL-címét (az alábbi képernyőképen látható), vagy hívja a GetReports/GetReports REST API-t, és másolja ki a megfelelő jelentésbeágyazási embedURL mezőt a válaszból (vegye figyelembe, hogy a REST-hívásnak nem szabad munkaterület-azonosítót tartalmaznia az URL-cím részeként, mert az alkalmazás példánya a felhasználó munkaterületén jön létre).

4. Használja a JS SDK-hoz a 3. lépésben lekért beágyazási URL-címet.

    ![Beágyazás alkalmazásokból](media/embed-from-apps/embed-from-app.png)

## <a name="how-to-grab-dashboard-embed-url-for-embedding"></a>Irányítópult beágyazási URL-címének megragadása beágyazáshoz

1. Hozza létre az alkalmazás egy példányát egy felhasználói munkaterületen (Saját munkaterület) úgy, hogy megosztja azt saját magával, vagy végigvezet egy másik felhasználót ezen a folyamaton.

2. Hívja a GetDashboards REST API-t, és másolja ki a válaszból a megfelelő irányítópult embedURL mezőjét (vegye figyelembe, hogy a REST-hívásnak nem szabad munkaterület-azonosítót tartalmaznia az URL-cím részeként, mert az alkalmazás példánya a felhasználó munkaterületén jön létre).

3. Használja a JS SDK-hoz a 4. lépésben lekért beágyazási URL-címet.

## <a name="next-steps"></a>Következő lépések

Tekintse át azt is, hogyan végezhet beágyazást az alkalmazás-munkaterületekről a külső ügyfelek és a cége számára.

> [!div class="nextstepaction"]
>[Beágyazás külső ügyfelek számára](embed-sample-for-customers.md)

> [!div class="nextstepaction"]
>[Beágyazás a cég számára](embed-sample-for-your-organization.md)