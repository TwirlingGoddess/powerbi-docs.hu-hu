---
title: Power BI URL-címek
description: Végpontok, amelyeknek a Power BI-t használó ügyfeleknek el kell érniük
author: markingmyname
ms.author: maghan
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 08/13/2018
ms.openlocfilehash: 8e29fa0c9471bb865619102247f38776208c3d87
ms.sourcegitcommit: 8990028a348b642ba5c96f001fe3a4280f0166ee
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/14/2018
ms.locfileid: "40101131"
---
# <a name="power-bi-urls"></a>Power BI URL-címek

A Power BI SaaS (szoftverszolgáltatás) néven is ismert **online Power BI szolgáltatáshoz** internetkapcsolatra van szükség. Az online Power BI szolgáltatást használó ügyfeleknek el kell érniük az alábbi végpontokat.

A Power BI online szolgáltatás használatához hozzá kell férnie az alábbi táblázatokban **kötelezőként** megjelölt végpontokhoz, és a hivatkozott webhelyeken **kötelezőként** megjelölt végpontokhoz is, hogy csatlakozni tudjon. Ha egy külső webhelyre mutató hivatkozás egy adott bekezdésre mutat, akkor csak az abban a bekezdésben lévő végpontokat kell megvizsgálnia.

Bizonyos funkciók működése érdekében a **választhatóként** megjelölt végpontok is **szerepelhetnek az engedélyezési listán**.

Az online Power BI szolgáltatás csak a TCP 443-as port megnyitását igényli a felsorolt végpontok felé.

A helyettesítő karakterek (*) a gyökértartomány alatti összes szintet jelentik. Ha nincs elérhető információ, azt az N/A jelölés mutatja. A **Cél(ok)** oszlop teljes tartománynevek/tartományok listája, és olyan külső webhelyekre hivatkozik, amelyek további információkat tartalmaznak a végpontokról.

>[!Important]
>Az alábbi táblázatok információi nem vonatkoznak az **Egyesült államok kormányzati felhőszolgáltatására**, **a németországi felhőre** és a **kínai felhőre**.

## <a name="authentication"></a>Hitelesítés

A Power BI működése függ az Office 365 hitelesítés és identitás szakaszban feltüntetett végpontoktól. A Power BI használatához tudnia kell csatlakozni az alább hivatkozott webhelyen található végpontokhoz.

| Sor | Szerep | Cél(ok) | Port(ok) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Kötelező:** Hitelesítés és identitás | Lásd az [Office 365 hitelesítés és identitás szakaszt](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_identity) az Office 365 engedélyezési listájának webhelyén | N.A. |

## <a name="general-site-usage"></a>Általános webhelyhasználat

A Power BI használatához tudnia kell csatlakozni az alábbi táblázatban és a hivatkozott webhelyeken megadott végpontokhoz.

| Sor | Szerep | Cél(ok) | Port(ok) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Kötelező:** Háttérbeli API-k | *.analysis.windows.net | TCP 443 |
| 2 | **Kötelező:** Office 365-integráció | Lásd az [Office 365 portál és megosztás szakaszt](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_portal-identity) az Office 365 engedélyezési listájának webhelyén | N.A. |
| 3 | **Kötelező:** Portál | app.powerbi.com | TCP 443 |
| 4 | **Kötelező:** Szolgáltatási telemetria | dc.services.visualstudio.com | TCP 443 |
| 5 | **Választható:** Tájékoztató üzenetek | dynmsg.modpim.com | TCP 443 |
| 6 | **Választható:** NPS felmérések | nps.onyx.azure.net | TCP 443 |

## <a name="administration"></a>Felügyelet

Ahhoz, hogy rendszergazdai funkciókat végezzen el a Power BI-ban, tudnia kell csatlakozni az alább hivatkozott webhelyeken megadott végpontokhoz.

| Sor | Szerep | Cél(ok) | Port(ok) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Kötelező:** A felhasználók kezeléséhez és auditnaplók megtekintéséhez | Lásd az [Office 365 portál és megosztás szakaszt](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_portal-identity) az Office 365 engedélyezési listájának webhelyén | N.A. |

## <a name="get-data"></a>Adatok lekérése

Ahhoz, hogy adatokat kérhessen le bizonyos adatforrásokból, például a OneDrive-ból, tudnia kell csatlakozni az alábbi táblázatban megadott végpontokhoz.

| Sor | Szerep | Cél(ok) | Port(ok) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Kötelező:** AppSource (belső vagy külső alkalmazások a Power BI-ban) | appsource.microsoft.com | TCP 443 |
| 2 | **Választható:** Fájlok importálása személyes OneDrive-ból | Lásd: [A OneDrive webhelyhez megkövetelt URL-címek és portok](https://support.office.com/en-ie/article/required-urls-and-ports-for-onedrive-ce15d2cc-52ef-42cd-b738-d9c6f9b03f3a) | N.A. |
| 3 | **Választható:** Power BI 60 másodperc alatt – bemutató videó | *.doubleclick.net </br> *.ggpht.com </br> *.google.com </br> *.googlevideo.com </br> *.youtube.com </br> *.ytimg.com </br> fonts.gstatic.com | TCP 443 |
| 4 | **Választható:** PubNub streamelési adatforrások | Lásd: [PubNub dokumentáció](https://support.pubnub.com/support/solutions/articles/14000043522) | N.A. |

## <a name="dashboard-and-report-integration"></a>Irányítópultok és jelentések integrációja 

A Power BI-nak szüksége van bizonyos végpontokra az irányítópultok és jelentések támogatásához. Tudnia kell csatlakozni az alábbi táblázatban és a hivatkozott webhelyeken megadott végpontokhoz.

| Sor | Szerep | Cél(ok) | Port(ok) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Kötelező:** Excel-integráció | Lásd az [Office 365 online szakaszt](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_officeonline) az Office 365 engedélyezési listájának webhelyén | N.A. |

## <a name="custom-visuals"></a>Egyéni vizualizációk

A Power BI-nak szüksége van bizonyos végpontokra az egyéni vizualizációkhoz való hozzáféréshez és azok megjelenítéséhez. Tudnia kell csatlakozni az alábbi táblázatban és a hivatkozott webhelyeken megadott végpontokhoz.

| Sor | Szerep | Cél(ok) | Port(ok) |
|-----|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|--------------|---------------------------------------------|
| 1 | **Kötelező:** Egyéni vizualizáció importálása a Marketplace felületéről és fájlból | *.microsoft.com </br> *.bing.com </br> *.msecnd.net </br> *.osi.office.net </br> *.azureedge.net </br> ajax.aspnetcdn.com </br> nexus.ensighten.com </br> store.office.com | TCP 443 |
| 2 | **Választható:** Bing Térképek | bing.com </br> platform.bing.com </br> *.dynamic.tiles.virtualearth.net </br> *.virtualearth.net | TCP 443 |
| 3 | **Választható:** PowerApps | Lásd a [Szükséges szolgáltatások szakaszt](https://docs.microsoft.com/powerapps/maker/canvas-apps/limits-and-config#required-services) a PowerApps rendszerkövetelményeinek webhelyén | N.A. |
| 4 | **Választható:** Visio | Lásd az [Office 365 online szakaszt](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2#bkmk_officeonline) az Office 365 engedélyezési listájának webhelyén | N.A. |