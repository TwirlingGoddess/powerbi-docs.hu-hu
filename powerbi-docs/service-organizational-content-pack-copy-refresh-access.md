---
title: "Vállalati tartalomcsomagok: hozzáférés és másolás"
description: "Információ a Power BI vállalatitartalomcsomag-másolatok létrehozásáról és az azokhoz való hozzáférési problémák hibaelhárításáról"
services: powerbi
documentationcenter: 
author: maggiesMSFT
manager: kfile
backup: ajayan
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/12/2017
ms.author: maggies
LocalizationGroup: Share your work
ms.openlocfilehash: 328edd6f7bc1d7e0e2550eff2c34b97b5fd6442d
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="organizational-content-packs-copy-refresh-and-get-access"></a>Vállalati tartalomcsomagok: másolás, frissítés és hozzáférés kérése
> [!NOTE]
> Hallott már az új *alkalmazásokról*? Az alkalmazásokkal új módon oszthatja meg a nagyközönséggel a tartalmakat a Power BI-ban. Alkalmazásokat hozhat létre az *alkalmazás-munkaterületeken*, amelyek lecserélik a csoportokat és a csoport-munkaterületeket. Javasoljuk az alkalmazások használatát a vállalati tartalomcsomagok vagy csak olvasható munkaterületek helyett. [További információk az alkalmazásokról](service-install-use-apps.md).
> 
> 

Amikor közzétesz egy vállalati tartalomcsomagot, minden címzett ugyanazt az irányítópultot, jelentéseket, Excel-munkafüzeteket, adatkészleteket és adatokat látja (kivéve, ha SQL Server Analysis Services (SSAS) adatforrásról van szó).  A tartalomcsomagot csak a [tartalomcsomag létrehozója szerkesztheti és teheti újra közzé](service-organizational-content-pack-manage-update-delete.md).  Minden címzett menthet egy, az eredetivel párhuzamosan létező másolatot a tartalomcsomagról.

A tartalomcsomagok létrehozása nem azonos az irányítópultok megosztásával vagy az azokon való közös munkával. Olvassa el [Az irányítópultokon és jelentéseken végzett közös munka, illetve azok megosztása](service-how-to-collaborate-distribute-dashboards-reports.md) szakaszt, hogy eldönthesse, melyik lehetőség felel meg legjobban a helyzetének.

## <a name="create-a-copy-of-an-organizational-content-pack"></a>Másolat készítése egy vállalati tartalomcsomagról
Hozza létre a saját, mások által nem látható másolatát a tartalomcsomagról.

1. Válassza a tartalomcsomag irányítópultja mellett a három pontot (...) > a Másolat készítése lehetőséget.
   
    ![](media/service-organizational-content-pack-copy-refresh-access/power-bi-create-copy-organizational-content-pack.png)
2. Kattintson a **Mentés** gombra.  

Ezzel lett egy másolata, amelyet módosíthat. A módosításokat más nem fogja látni.

## <a name="help--i-can-no-longer-access-the-content-pack"></a>Segítség!  Már nem férek hozzá a tartalomcsomaghoz
Ennek több oka is lehet:

* **A tagságot érintő változások**:  A tartalomcsomagok közzététele e-mailes terjesztési listák, biztonsági csoportok és az [Office 365-ön alapuló Power BI-csoportok](https://support.office.com/article/Create-a-group-in-Office-365-7124dc4c-1de9-40d4-b096-e8add19209e9) számára történik.  Ha eltávolították a csoportból, nem lesz többé hozzáférése a tartalomcsomaghoz.
* **A terjesztést érintő változások**: A tartalomcsomag létrehozója módosítja a terjesztést. Ha például eredetileg az egész vállalat számára közzétették a tartalomcsomagot, de a létrehozó újból közzétette egy szűkebb közönség számára, lehet, hogy már nem tartozik a címzettek közé.
* **A biztonsági beállításokat érintő változások**: Ha az irányítópult és a jelentések helyszíni SSAS-adatforrásokhoz csatlakoznak, és módosítják a biztonsági beállításokat, előfordulhat, hogy visszavonták a kiszolgálóra vonatkozó engedélyeit.

## <a name="how-are-organizational-content-packs-refreshed"></a>Hogyan frissülnek a vállalati tartalomcsomagok?
Amikor egy tartalomcsomag létrejön, a frissítési beállításokat örökli az adatkészlettől.  Amikor másolatot készít egy tartalomcsomagról, az új verzió megtartja az eredeti adatkészletre mutató hivatkozást és a frissítési ütemezését. 

Lásd: [Vállalati tartalomcsomagok kezelése, frissítése és törlése](service-organizational-content-pack-manage-update-delete.md).

## <a name="next-steps"></a>Következő lépések
* [A vállalati tartalomcsomagok bemutatása](service-organizational-content-pack-introduction.md)
* [Csoportok létrehozása a Power BI-ban](service-create-distribute-apps.md)
* További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

