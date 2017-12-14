---
title: "Kapcsolódás a Microsoft Dynamics NAV-hoz a Power BI-jal"
description: Microsoft Dynamics NAV a Power BI-hoz
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: 7d5db73a05a74de934fa8ac630f673fe4f5bb3af
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="connect-to-microsoft-dynamics-nav-with-power-bi"></a>Kapcsolódás a Microsoft Dynamics NAV-hoz a Power BI-jal
A Power BI használatával egyszerűen elemezheti Microsoft Dynamics NAV-adatait. A Power BI lekéri az értékesítési és a pénzügyi adatokat is, majd irányítópultot és jelentést is magában foglaló alkalmazást készít az adatok alapján. A Power BI-nak szüksége van az Ön engedélyeire az adatokat tartalmazó táblákhoz, ebben az esetben az értékesítési és pénzügyi adatokhoz. További információt a követelményekről lent talál. Az alkalmazás telepítése után az irányítópult és a jelentések a Power BI szolgáltatásban ([https://powerbi.com](https://powerbi.com)) és a Power BI-mobilalkalmazásokban is megtekinthetők. 

[Kapcsolódjon a Microsoft Dynamics NAV-hoz a Power BI-jal](https://app.powerbi.com/getdata/services/microsoft-dynamics-nav), vagy tájékozódjon tovább a [Dynamics NAV integrációjáról](https://powerbi.microsoft.com/integrations/microsoft-dynamics-nav) a Power BI-jal.

## <a name="how-to-connect"></a>A kapcsolódás menete
[!INCLUDE [powerbi-service-apps-get-more-apps](./includes/powerbi-service-apps-get-more-apps.md)]

1. Válassza a **Microsoft Dynamics NAV**, majd a **Beolvasás** lehetőséget.  
   ![](media/service-connect-to-microsoft-dynamics-nav/mdnav.png)
2. Amikor a rendszer kéri, adja meg Microsoft Dynamics NAV OData URL-címét. Az URL-címnek a következő mintának kell megfelelnie:
   
    `https//instance.navserver.com:7048/DynamicsNAV90_Instance1/OData/Company('CRONUS%20International%20Ltd.')`
   
   * „instance.navserver.com”, az Ön NAV-kiszolgálójának nevével
   * „DynamicsNAV90\_Instance1” a saját NAV-kiszolgálópéldány nevével
   * „Company('CRONUS%20International%20Ltd.')” az Ön vállalatának NAV-beli nevével
     
     Ez az URL-cím egyszerűen kinyerhető úgy, hogy a Dynamics NAV webes szolgáltatásainak megnyitása után megkeresi a powerbifinance webszolgáltatást, és kimásolja az OData URL-címet, de lehagyja a „/powerbifinance” végződést.  
     ![](media/service-connect-to-microsoft-dynamics-nav/param.png)
3. Válassza az **Alapszintű** lehetőséget és adja meg Microsoft Dynamics NAV hitelesítő adatait.
   
    A Microsoft Dynamics NAV-fióknak rendszergazdai jogosultsággal (vagy legalább az értékesítési és a pénzügyi adatokhoz való engedélyekkel) kell rendelkeznie.  Jelenleg csak az alapszintű (felhasználónév és jelszó) hitelesítés támogatott.
   
    ![](media/service-connect-to-microsoft-dynamics-nav/creds.png)
4. A Power BI betölti a Microsoft Dynamics NAV-adatokat, és használatra kész irányítópultot és jelentést hoz létre.   
   ![](media/service-connect-to-microsoft-dynamics-nav/dashboard.png)

## <a name="view-the-dashboard-and-reports"></a>Az irányítópult és a jelentések megtekintése
[!INCLUDE [powerbi-service-apps-open-app](./includes/powerbi-service-apps-open-app.md)]

[!INCLUDE [powerbi-service-apps-open-app](./includes/powerbi-service-apps-what-now.md)]

## <a name="whats-included"></a>A csomag tartalma
Az irányítópult és a jelentések az alábbi táblákból származó adatokat tartalmaznak:  

* ItemSalesAndProfit  
* ItemSalesByCustomer  
* powerbifinance  
* SalesDashboard  
* SalesOpportunities  
* SalesOrdersBySalesPerson  
* TopCustomerOverview  

## <a name="system-requirements"></a>Rendszerkövetelmények
A Microsoft Dynamics NAV-adatok Power BI-ba történő importálásához engedélyekkel kell rendelkeznie azokhoz a fent felsorolt táblákhoz, amelyekből az értékesítési és pénzügyi adatok beolvasódnak. A tábláknak adatokat is kell tartalmazniuk, az üres táblák importálása egyelőre hibát okoz.

## <a name="troubleshooting"></a>Hibaelhárítás
A Power BI a Microsoft Dynamics NAV webes szolgáltatásával olvassa be az adatokat. Ha nagy mennyiségű adatot tárol a Microsoft Dynamics NAV-példányában, akkor ajánlott igény szerint módosítani a frissítés gyakoriságát, hogy minimalizálja a webes szolgáltatás terhelését. Javasolt továbbá egy rendszergazdával létrehozatni és megosztatni az alkalmazást ahelyett, hogy minden rendszergazda sajátot hozna létre.

**„Nem sikerült érvényesíteni a paramétereket. Győződjön meg arról, hogy minden paraméter érvényes.”**  
Ha ezt a hibaüzenetet kapja a Microsoft Dynamics NAV URL-címének begépelése után, akkor győződjön meg a következő követelmények teljesüléséről:

* Az URL-cím pontosan megfelel a következő mintának:
  
    `https//instance.navserver.com:7048/DynamicsNAV90_Instance1/OData/Company('CRONUS%20International%20Ltd.')`
  
  * „instance.navserver.com”, az Ön NAV-kiszolgálójának nevével
  * „DynamicsNAV90\_Instance1” a saját NAV-kiszolgálópéldány nevével
  * „Company('CRONUS%20International%20Ltd.')” az Ön vállalatának NAV-beli nevével
* Minden betű kisbetű.  
* Az URL-cím sémája 'https'.  
* Az URL-cím vége nincs perjellel lezárva.

**„A bejelentkezés sikertelen volt”**  
Ha a Microsoft Dynamics NAV hitelesítő adatok megadása után a „bejelentkezés sikertelen volt” hibaüzenetet kapja, akkor a következő problémák egyike állhat fenn:

* A használt fióknak nincs engedélye a Microsoft Dynamics NAV-adatok beolvasására az Ön fiókjából. Győződjön meg arról, hogy rendszergazdai fiókot használ, és próbálkozzon újra.
* A Dynamics NAV-példány, amelyhez kapcsolódni próbál, nem rendelkezik érvényes SSL-tanúsítvánnyal. Ebben az esetben részletesebb hibaüzenetet kap („unable to establish trusted SSL relationship” – nem sikerült létrehozni megbízható SSL-kapcsolatot). Vegye figyelembe, hogy a saját aláírású tanúsítványok használata nem támogatott.

**„Hoppá!”**  
Ha a hitelesítő párbeszédablak után a „Hoppá!” hibaüzenet jelenik meg, akkor a Power BI az adatok beolvasása során ütközött problémába.

* Ellenőrizze, hogy az URL-cím megfelel-e a fent megadott sémának. Gyakori hiba, hogy csak az alábbi részt adják meg:
  
    `https//instance.navserver.com:7048/DynamicsNAV90\_Instance1/OData`
  
    Meg kell adni a „Company('CRONUS%20International%20Ltd.')” részt is, a saját NAV-beli vállalatnévvel kitöltve:
  
    `https//instance.navserver.com:7048/DynamicsNAV90\_Instance1/OData/Company('CRONUS%20International%20Ltd.')`

## <a name="next-steps"></a>További lépések
* [Alkalmazások a Power BI-ban](service-install-use-apps.md)
* [Adatok beolvasása a Power BI-ban](service-get-data.md)
* További kérdései vannak? [Kérdezze a Power BI-közösséget!](http://community.powerbi.com/)

