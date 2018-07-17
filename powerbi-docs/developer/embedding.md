---
title: Beágyazás a Power BI-jal
description: A Power BI az irányítópultok és jelentések alkalmazásokba való beágyazását lehetővé tevő API-kat kínál.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 06/22/2018
ms.author: maghan
ms.openlocfilehash: 82a4c9c58567f5ace943363b7bed59fa744e85a5
ms.sourcegitcommit: 2a7bbb1fa24a49d2278a90cb0c4be543d7267bda
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/26/2018
ms.locfileid: "36944100"
---
# <a name="embedding-with-power-bi"></a>Beágyazás a Power BI-jal
A Power BI az irányítópultok és jelentések alkalmazásokba való beágyazását lehetővé tevő API-kat kínál. A Power BI API-k a tartalmak beágyazása során egységes funkciókat, valamint a legújabb Power BI-funkciókhoz (például irányítópultokhoz, átjárókhoz és alkalmazás-munkaterületekhez) történő hozzáférést teszik elérhetővé.

## <a name="a-single-api"></a>Egyetlen API
A Power BI-tartalmak beágyazása során két fő forgatókönyv képzelhető el.  Egyrészt a cégen belüli felhasználók számára történő beágyazás (a felhasználóknak rendelkezniük kell Power BI-licenccel), másrészt Power BI-licencet nem kívánó beágyazás más felhasználók és ügyfelek számára. A Power BI REST API mindkét forgatókönyvet támogatja. 

Power BI-licenccel nem rendelkezők számára ugyanazt az API-t használva ágyazhat be irányítópultokat és jelentéseket egyéni alkalmazásokba függetlenül attól, hogy azt a cége vagy az ügyfele számára készíti. Az ügyfelek így megtekinthetik az alkalmazás által kezelt adatokat. A cégen belüli Power BI-felhasználók ezen kívül *saját adataikat* is megtekinthetik közvetlenül a Power BI-ban vagy a beágyazott alkalmazásban. A beágyazáshoz teljes körűen igénybe veheti a JavaScript és a REST API-k lehetőségeit.

Ha látni kívánja, hogyan működik a beágyazás tekintse meg a [JavaScript beágyazását szemléltető példát](https://microsoft.github.io/PowerBI-JavaScript/demo/).

## <a name="embedding-for-your-organization"></a>Beágyazás a cég számára
Amennyiben cége számára végzi a beágyazást, kibővítheti a Power BI szolgáltatást. A tartalom megtekintéséhez az alkalmazás felhasználójának be kell jelentkeznie a Power BI szolgáltatásba. Amikor a cég egyik felhasználója bejelentkezik, csak azokhoz az irányítópultokhoz és jelentésekhez lesz hozzáférése, amelyeknek ők a tulajdonosai, vagy amelyeket a Power BI szolgáltatásban megosztottak vele. 

*Példák a cégen belüli beágyazásra: belső webalkalmazások, SharePoint Online-kijelzők és [Microsoft Teams-integráció (ehhez rendszergazdai jogosultsággal kell rendelkeznie)](https://powerbi.microsoft.com/en-us/blog/power-bi-teams-up-with-microsoft-teams/).*

Amennyiben a cége számára végez beágyazást, tekintse át a következőket:

* [Jelentés integrálása egy alkalmazásba](integrate-report.md)
* [Irányítópult integrálása egy alkalmazásba](integrate-dashboard.md)
* [Csempe integrálása egy alkalmazásba](integrate-tile.md)

Amikor Power BI-felhasználók számára végez beágyazást, az önkiszolgáló lehetőségek (pl. a szerkesztés, mentés stb.) a [JavaScript API-n](https://github.com/Microsoft/PowerBI-JavaScript) keresztül érhetők el.

A gyors indulás érdekében követheti az [Előkészítési eszköz vállalaton belüli beágyazáshoz](https://aka.ms/embedsetup/UserOwnsData) lépéseit, és letölthet egy mintaalkalmazást, amely végigvezeti Önt a jelentés integrálásán a cég számára.

## <a name="embedding-for-your-customers"></a>Beágyazás ügyfelek számára
Amikor az ügyfelei számára végez beágyazást, irányítópultokat és jelentéseket ágyazhat be olyan felhasználók számára, akik nem rendelkeznek Power BI-fiókkal. Az ügyfélnek nem szükséges ismernie a Power BI működését. Beágyazott alkalmazás létrehozásához legalább egy Power BI Pro-fiók megléte szükséges. Ez a Power BI Pro-fiók szolgál fő fiókként az alkalmazás számára. Ebben az esetben proxyfiókként működik. A Power BI Pro-fiók lehetővé teszi beágyazási tokenek létrehozását, amelyek hozzáférést biztosítanak a Power BI szolgáltatás olyan irányítópultjaihoz és jelentéseihez, amelyeket az alkalmazás kezel, vagy amelyek az alkalmazáshoz tartoznak. 

*Az ügyfél számára végzett beágyazásra egy példa, ha más vállalatoknak értékesít egy ISV-alkalmazást.*

![A beágyazás folyamata ügyfelek számára végzett beágyazás során](media/embedding/powerbi-embed-flow.png)

Az irányítópultok, jelentések és csempék beágyazásához ugyanazokat az API-kat használja, mintha a cége számára végezné a beágyazást.

> [!IMPORTANT]
> Bár a beágyazás maga igényli a Power BI szolgáltatás meglétét, az ügyfeleknek nem kell rendelkezniük Power BI-előfizetéssel. Nem kell bejelentkezniük a Power BI szolgáltatásba a beágyazott tartalmak megtekintéséhez az alkalmazásban.
> 

Amikor készen áll az éles környezetbe való áthelyezésre, az alkalmazás-munkaterülethez hozzá kell rendelni egy kapacitást. A Power BI Embedded a Microsoft Azure-on belül elérhetővé tesz az alkalmazásban felhasználható kapacitást.

A beágyazással kapcsolatos további információért lásd a [Power BI-irányítópultok, -jelentések és -csempék beágyazását](embedding-content.md) ismertető cikket.

A gyors indulás érdekében követheti az [Előkészítési eszköz ügyfél számára végzett beágyazáshoz](https://aka.ms/embedsetup/AppOwnsData) lépéseit, és letölthet egy mintaalkalmazást, amely végigvezeti Önt a jelentés alkalmazásba integrálásán.

Ha a Power BI-munkaterületcsoportok szolgáltatást használja az Azure-ban, tekintse meg a [tartalmak a Power BI-munkaterületcsoportok Azure-szolgáltatásból történő migrálását](migrate-from-powerbi-embedded.md) ismertető témakört, amely ismerteti a migrálás pontos folyamatát.

## <a name="next-steps"></a>Következő lépések
[Power BI-irányítópultok, -jelentések és -csempék beágyazása](embedding-content.md)  
[Power BI Embedded-munkaterületcsoport tartalmainak migrálása a Power BI-ba](migrate-from-powerbi-embedded.md)  
[Power BI Premium – pontosan mi is ez?](../service-premium.md)  
[JavaScript API Git-adattár](https://github.com/Microsoft/PowerBI-JavaScript)  
[Power BI C# Git-adattár](https://github.com/Microsoft/PowerBI-CSharp)  
[JavaScript beágyazási minta](https://microsoft.github.io/PowerBI-JavaScript/demo/)  
[Embedded elemzési kapacitásának tervezésével kapcsolatos tanulmány](https://aka.ms/pbiewhitepaper)  
[Power BI Premium-tanulmány](https://aka.ms/pbipremiumwhitepaper)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

