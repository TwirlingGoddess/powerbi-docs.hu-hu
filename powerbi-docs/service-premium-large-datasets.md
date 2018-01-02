---
title: "Nagyméretű adathalmazok Power BI Premium-támogatása"
description: "A Power BI Premium mostantól támogatja a legfeljebb 10 GB méretű adathalmazok használatát."
services: powerbi
documentationcenter: 
author: MarkMcGeeAtAquent
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
ms.date: 12/11/2017
ms.author: v-mamcge
ms.openlocfilehash: 82ac4382fe80d83b60705f135b50738718f28876
ms.sourcegitcommit: 7eb15c813a0d14322cb1316bb7aab23cbc13aae6
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/11/2017
---
# <a name="power-bi-premium-support-for-large-datasets"></a>Nagyméretű adathalmazok Power BI Premium-támogatása

A Power BI Premium támogatja a legfeljebb 10 GB méretű Power BI Desktop- (.pbix-) fájlok feltöltését. Egy nagyméretű adathalmaz használatához tegye azt közzé egy prémium szintű kapacitáshoz társított munkaterületen.
 
## <a name="best-practices"></a>Ajánlott eljárások

Ez a szakasz ismerteti a nagyméretű adathalmazok használatának ajánlott eljárásait.

**A nagyméretű modellek rendkívül erőforrás-igényesek lehetnek** a kapacitásának terhére; ajánlott legalább a P1 termékváltozatot alkalmazni minden 1 GB-nál nagyobb modellhez. A következő táblázatban a különböző méretű .pbix-fájlokhoz ajánlott termékváltozatok vannak megadva:


   |Termékváltozat  |A .pbix-fájl mérete   |
   |---------|---------|
   |P1    | < 3 GB        |
   |P2    | < 6 GB        |
   |P3    | legfeljebb 10 GB   |



**A .pbix-fájlok nagy mértékben tömörített állapotban tartalmazzák az adatokat**. Az adatok mérete valószínűleg többszörösére fog nőni a memóriába való betöltéskor, és ehhez képest is a többszörösére nőhet az adatok frissítése során.

**A nagyméretű adathalmazok ütemezett frissítése hosszú időt vehet igénybe**, és rendkívül erőforrás-igényes lehet. Ennek megfelelően nem ütemezzen túl sok egymással átfedő frissítést. Azt is fontos megjegyezni, hogy az ütemezett frissítési feladatok időkorlátja minden adathalmaz esetében a duplájára, négy órára lett növelve ebben az esetben.

**A jelentés kezdeti betöltése a nagyméretű adathalmazok esetében hosszú időt vehet igénybe**, ha már eltelt némi idő az adathalmaz utolsó használata óta, mivel a modell a prémium szintű kapacitáshoz tartozó memóriába van betöltve. A hosszabb ideig töltődő jelentések esetében egy betöltési folyamatjelző mutatja a betöltés előrehaladását.

**Ha a munkaterületet eltávolítja a prémium szintű kapacitásból**, a modell és az ahhoz társított összes jelentés és irányítópult sem fog működni.

**Bár a lekérdezésenkénti memória- és időkorlátozások a prémium szintű kapacitás esetében jóval magasabbak**, erősen ajánlott a látványelemeket szűrőkkel és szeletelőkkel korlátozni kizárólag a szükséges elemek megjelenítésére.

## <a name="next-steps"></a>Következő lépések
[Mi a Power BI Premium?](service-premium.md)  
[A Power BI Premium kibocsátási megjegyzései](service-premium-release-notes.md)  
[Microsoft Power BI Premium-tanulmány](https://aka.ms/pbipremiumwhitepaper)  
[Egy Power BI vállalati bevezetését ismertető tanulmány megtervezése](https://aka.ms/pbienterprisedeploy)  
[A Pro-próbaverzió kiterjesztett aktiválása](service-extended-pro-trial.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)
