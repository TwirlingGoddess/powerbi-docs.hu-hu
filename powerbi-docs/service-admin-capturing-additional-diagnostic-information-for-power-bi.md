---
title: "További diagnosztikai adatok gyűjtése"
description: "További diagnosztikai adatok gyűjtése"
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 06/28/2017
ms.author: asaxton
ms.openlocfilehash: 7910270ecafd383600ff19e6c6c2bfc1ad6e6d4a
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="capturing-additional-diagnostic-information"></a>További diagnosztikai adatok gyűjtése
## <a name="capturing-additional-diagnostic-information-for-power-bi"></a>További diagnosztikai adatok gyűjtése a Power BI számára
A következő útmutatók két lehetséges módszert kínálnak további diagnosztikai adatok manuális begyűjtésére a Power BI-webügyféltől.  Elég az egyiket végrehajtani.

## <a name="network-capture---edge--internet-explorer"></a>Hálózati rögzítés – Edge & Internet Explorer
1. Nyissa meg a [Power BI](https://app.powerbi.com)-t az Edge-ben vagy az Internet Explorerben.
2. Nyissa meg az Edge fejlesztői eszközeit az F12 lenyomásával.
3. Megjelenik a Fejlesztői eszközök ablak: 
   
   ![](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-developer-tools.png)
4. Váltson a Hálózat fülre. Itt látható az eddig rögzített forgalom. 
   
   ![](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-network-tab.png)
5. Az ablakban böngészve minden felmerülő probléma reprodukálható. A fejlesztői eszközök ablaka a munkamenet során bármikor megjeleníthető és elrejthető az F12 billentyű lenyomásával.
6. A rögzítés leállításához válassza a piros négyzetet a fejlesztői eszközök terület Hálózat fülén.
   
   ![](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-network-tab-stop.png)
7. Válassza a lemez ikont a **Rögzített adatok HAR-fájlba exportálásához**
   
   ![](media/service-admin-capturing-additional-diagnostic-information-for-power-bi/edge-network-tab-save.png)
8. Adjon nevet a HAR-fájlnak és mentse.
   
    A HAR-fájl minden információt tartalmaz a böngészőablak és a Power BI közötti hálózati kérelmekről.  Ez magában foglalja az egyes kérelmek tevékenységazonosítóját, pontos időbélyegét és az ügyféltől visszakapott bármely esetleges hibaüzenetet.  Tartalmazza a képernyőn megjelenő vizualizációk feltöltéséhez használt adatokat is.
9. A HAR-fájlt átadhatja vizsgálatra a támogatási szolgálatnak.

További kérdései vannak? [Kérdezze a Power BI-közösséget!](http://community.powerbi.com/)

