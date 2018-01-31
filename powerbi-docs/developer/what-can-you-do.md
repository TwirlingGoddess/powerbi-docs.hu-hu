---
title: "Mire használhatják a fejlesztők a Power BI-t?"
description: "A Power BI lehetőségek széles tárházát kínálja a fejlesztők számára. Ezek a beágyazási lehetőségektől az egyéni vizualizációkig és az adatkészletek streameléséig terjednek."
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 07/20/2017
ms.author: maghan
ms.openlocfilehash: b310562ac31694f398a659018743b8fa7aa46e35
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/30/2018
---
# <a name="what-can-developers-do-with-power-bi"></a>Mire használhatják a fejlesztők a Power BI-t?
A Power BI lehetőségek széles tárházát kínálja a fejlesztők számára. Ezek a beágyazási lehetőségektől az egyéni vizualizációkig és az adatkészletek streameléséig terjednek.

## <a name="embedding"></a>Beágyazás
A Power BI szolgáltatás és az Azure-beli Power BI Embedded szolgáltatás együtt egy közös API-t kínál az irányítópultok és jelentések beágyazásához. Ez azt jelenti, hogy a tartalmak (például irányítópultok, átjárók és alkalmazás-munkaterületek) beágyazásához egyetlen egységes API-felület, konzisztens funkciókészlet és a Power BI legújabb szolgáltatásai használhatók. További információkért lásd: [Beágyazás a Power BI-jal](embedding.md).

![](media/what-can-you-do/powerbi-embed-sample.png)

## <a name="custom-visuals"></a>Egyéni vizualizációk
Az egyéni vizualizációk révén saját vizualizációkat hozhat létre, amelyeket a Power BI-jelentésekben használhat. Az egyéni vizualizációk a JavaScript egy bővített változatában, TypeScriptben készülnek, amely támogat bizonyos különleges funkciókat, és korábban hozzáférhetővé teszi az ES6/ES7 funkciókat. A vizualizációk stílusa CSS-stíluslapokkal alakítható ki. A kényelem érdekében a Less előfordítót alkalmazzuk, amely támogat bizonyos különleges funkciókat, mint például a beágyazás, a változók, a mixinek, a feltételek vagy a ciklusok. Ha nem szeretné használni ezeket a funkciókat, egyszerű CSS-kódot is írhat a Less-fájlba.

Az egyéni vizualizációk fejlesztésével és közzétételével kapcsolatos további információkért lásd: [Egyéni vizualizációk közzététele az Office Áruházban](office-store.md).

![](media/what-can-you-do/powerbi-custom-visual-store.png)

## <a name="push-data-into-power-bi"></a>Adatok leküldése a Power BI szolgáltatásba
A Power BI API lehetővé teszi az adatok leküldését az adatkészletekbe. Ennek segítéségével kiegészítheti sorokkal az adatkészletekben lévő táblákat. Az irányítópultok csempéi vagy a jelentésekben lévő vizualizációk ezután tükrözik az új adatokat.

További információkért lásd: [Adatok leküldése az irányítópultokra](walkthrough-push-data.md)

## <a name="next-steps"></a>További lépések
[Beágyazás a Power BI szolgáltatással](embedding.md)  
[Power BI Embedded munkaterület-csoport tartalmainak migrálása a Power BI-ba](migrate-from-powerbi-embedded.md)  
[JavaScript API Git-adattár](https://github.com/Microsoft/PowerBI-JavaScript)  
[Power BI C# Git-adattár](https://github.com/Microsoft/PowerBI-CSharp)  
[Egyéni vizualizációk közzététele az Office áruházban](office-store.md)  
[Power BI-vizualizációk Git-adattára](https://github.com/Microsoft/PowerBI-visuals)  
[JavaScript beágyazási minta](https://microsoft.github.io/PowerBI-JavaScript/demo/)  
[Power BI Premium-tanulmány](https://aka.ms/pbipremiumwhitepaper)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

