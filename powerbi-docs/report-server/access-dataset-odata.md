---
title: Megosztott adatkészletek elérése OData-csatornákként a Microsoft Power BI jelentéskészítő kiszolgálóban
description: A Power BI-jelentések különféle adatforrásokhoz csatlakozhatnak. Az adatok használatának módjától függően eltérő adatforrások érhetők el.
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-report-server
ms.topic: conceptual
ms.date: 01/05/2018
ms.author: maghan
ms.openlocfilehash: 9ec0ace4cf92d559da4a2b1bd1aa0f918e2b09dc
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34294939"
---
# <a name="accessing-shared-datasets-as-odata-feeds-in-power-bi-report-server"></a>Megosztott adatkészletek elérése OData-csatornákként a Microsoft Power BI jelentéskészítő kiszolgálóban
A megosztott adatkészletek a Power BI Desktopból OData-csatorna használatával érhetők el.

1. Az OData-csatorna URL-címével csatlakozhat az OData-forráshoz.
   
    ![Jelentéskészítő kiszolgáló OData-csatorna forrása](media/access-dataset-odata/report-server-odata-feed.png)
2. Miután lekérte az adatokat a Power BI Desktopban, a Lekérdezés-szerkesztőben módosíthatja azokat.
   
    ![Power BI Desktop Lekérdezésszerkesztő OData-csatornával](media/access-dataset-odata/report-server-odata-results-query-editor.png)
3. Most már használhatja az adatokat jelentések tervezésére.
   
    ![Power BI Desktop-jelentésterv OData-csatornával](media/access-dataset-odata/report-server-odata-power-bi-desktop-report-design.png)

Használja a **Speciális beállítások** lehetőséget, hogy bekapcsolhassa a nyitott típusú oszlopokat, és ennek megfelelően formázhassa az oszlopokat a Power Query bővítményben az igényei szerint.

További információ az [OData-csatornákhoz való csatlakozásról a Power BI Desktopban](../desktop-connect-odata.md).

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

