---
title: Mire használhatják a fejlesztők a Power BI-t?
description: A Power BI lehetőségek széles tárházát kínálja a fejlesztők számára. Ezek a beágyazási lehetőségektől az egyéni vizualizációkig és az adatkészletek streameléséig terjednek.
services: powerbi
author: markingmyname
ms.author: maghan
ms.date: 05/03/2018
ms.topic: overview
ms.service: powerbi
ms.custom: mvc
manager: kfile
ms.openlocfilehash: 473052ee652c1fd6e68294efdbd7334cbb2df714
ms.sourcegitcommit: 493f160d04ed411ff4741c599adc63ba1f65230f
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/07/2018
ms.locfileid: "33810966"
---
# <a name="what-can-developers-do-with-power-bi"></a>Mire használhatják a fejlesztők a Power BI-t?

A fejlesztőknek több módszer is rendelkezésére áll ahhoz, hogy a Power BI-tartalmat alkalmazásokban használjanak. Többek között **beágyazást végezhetnek a Power BI-jal**, használhatnak **egyéni vizualizációkat** vagy **adatokat tölthetnek be a Power BI-ba**.

## <a name="embedding"></a>Beágyazás
A Power BI szolgáltatás (SaaS) és a Power BI Embedded szolgáltatás az Azure-ban (PaaS) API-kkal is rendelkezik az irányítópultok és jelentések beágyazásához. Ez azt jelenti, hogy a tartalmak (például irányítópultok, átjárók és alkalmazás-munkaterületek) beágyazásához egy funkciókészlet és a Power BI legújabb szolgáltatásai használhatók.

![PBIE-minta](media/what-can-you-do/what-can-you-do-01.png)

## <a name="develop-custom-visuals"></a>Egyéni vizualizációk létrehozása
Az egyéni vizualizációk révén saját vizualizációkat hozhat létre, amelyeket a Power BI-jelentésekben használhat. Az egyéni vizualizációk TypeScriptben, a JavaScript egy bővített változatában készülnek. A TypeScript néhány speciális funkciót is támogat, és korai hozzáférést biztosít az ES6/ES7-funkciókhoz. A vizualizációk stílusa CSS-stíluslapokkal alakítható ki. A fejlesztők munkájának megkönnyítésére a Less előfordító programot használjuk. Ez támogat bizonyos összetettebb funkciókat, például a beágyazást, a változókat, a feltételeket és a ciklusokat. Ha nem szeretné használni ezeket a funkciókat, egyszerű CSS-kódot is írhat a Less-fájlba.

![CV-minta](media/what-can-you-do/powerbi-custom-visual-store.png)

## <a name="push-data-into-power-bi"></a>Adatok leküldése a Power BI szolgáltatásba
A Power BI API lehetővé teszi az adatok leküldését az adatkészletekbe. Ennek segítéségével kiegészítheti sorokkal az adatkészletekben lévő táblákat. Az irányítópultok csempéi vagy a jelentésekben lévő vizualizációk ezután tükrözik az új adatokat.

![Adatminta leküldése](media/what-can-you-do/powerbi-push-data.png)

## <a name="next-steps"></a>Következő lépések
[Beágyazás a Power BI szolgáltatással](embedding.md)  
[Egyéni vizualizációk közzététele az Office áruházban](office-store.md)  
[Adatok küldése az irányítópultokra](walkthrough-push-data.md)
