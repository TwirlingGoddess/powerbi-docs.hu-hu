---
title: További diagnosztikai adatok gyűjtése
description: További diagnosztikai adatok gyűjtése
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 06/28/2017
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 76860e740d43a1907692a7cd4fed1a6df68c93d4
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34239222"
---
# <a name="capturing-additional-diagnostic-information"></a>További diagnosztikai adatok gyűjtése
## <a name="capturing-additional-diagnostic-information-for-power-bi"></a>További diagnosztikai adatok gyűjtése a Power BI számára
A következő útmutatók két lehetséges módszert kínálnak további diagnosztikai adatok manuális begyűjtésére a Power BI-webügyféltől.  Elég az egyiket végrehajtani.

## <a name="network-capture---edge--internet-explorer"></a>Hálózati rögzítés – Microsoft Edge & Internet Explorer
1. Nyissa meg a [Power BI](https://app.powerbi.com)-t a Microsoft Edge-ben vagy az Internet Explorerben.
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

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

