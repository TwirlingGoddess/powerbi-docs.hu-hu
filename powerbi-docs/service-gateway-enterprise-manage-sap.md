---
title: "SAP HANA-adatforrások kezelése"
description: "Hogyan kell kezelni a helyszíni adatátjárót és az átjáróhoz tartozó adatforrásokat. Ez a cikk kifejezetten az SAP HANA használatára vonatkozik."
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 10/05/2017
ms.author: davidi
ms.openlocfilehash: d65bdf17997809cd4bcaa2718da42ba41398bcf4
ms.sourcegitcommit: b3ee37e1587f1269ee7dd9daf1685a06dea3b50c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/23/2017
---
# <a name="manage-your-sap-hana-data-source"></a>SAP HANA-adatforrások kezelése
Miután telepítette a helyszíni adatátjárót, fel kell vennie az adatátjáróval használható adatforrásokat. Ez a cikk az adatátjárók és az adatforrások használatával foglalkozik. Az SAP HANA-adatforrás ütemezett frissítéshez vagy DirectQueryhez is használható.

## <a name="download-and-install-the-gateway"></a>Az átjáró letöltése és telepítése
Az átjáró letölthető a Power BI szolgáltatásból. Válassza a **Letöltések** > **Adatátjáró** lehetőséget, vagy nyissa meg az [átjáró letöltési oldalát](https://go.microsoft.com/fwlink/?LinkId=698861).

![](media/service-gateway-enterprise-manage-sap/powerbi-download-data-gateway.png)

## <a name="add-a-gateway"></a>Átjáró hozzáadása
Átjáró hozzáadásához egyszerűen [töltse le](https://go.microsoft.com/fwlink/?LinkId=698861) és telepítse az átjárót a saját környezete egyik kiszolgálóján. Az átjáró a telepítése után megjelenik az **Átjárók kezelése** alatti listában.

> [!NOTE]
> Az **Átjárók kezelése** lehetőség csak akkor jelenik meg, ha Ön legalább egy átjárónak rendszergazdája. Ez akkor lehetséges, ha Önt rendszergazdaként adták hozzá, vagy ha Ön telepít és konfigurál egy átjárót.
> 
> 

## <a name="remove-a-gateway"></a>Átjáró eltávolítása
Egy átjáró eltávolítása az átjáró alá tartozó valamennyi adatforrás törlésével jár.  Ez hibát okoz az adatforrásokra támaszkodó irányítópultokban és jelentésekben is.

1. Kattintson a fogaskerék ikonra ![](media/service-gateway-enterprise-manage-sap/pbi_gearicon.png) a jobb felső sarokban > **Átjárók kezelése**.
2. Átjáró > **Eltávolítás**
   
   ![](media/service-gateway-enterprise-manage-sap/datasourcesettings7.png)

## <a name="add-a-data-source"></a>Adatforrás hozzáadása
Adatforrást hozzáadhat úgy, hogy az átjárót kijelölve az **Adatforrás hozzáadása** lehetőségre kattint, vagy az Átjáró > **Adatforrás hozzáadása** lehetőséget választja.

![](media/service-gateway-enterprise-manage-sap/datasourcesettings1.png)

Ezután kiválaszthatja a listából az **Adatforrástípus** elemet.

![](media/service-gateway-enterprise-manage-sap/datasourcesettings2-sap.png)

Ezt követően megadhatja az adatforrásra vonatkozó információkat, köztük a **Kiszolgálót**, a **Felhasználónevet** és a **Jelszót**.

> [!NOTE]
> Az adatforrás felé irányuló összes lekérdezés ezeket a hitelesítő adatokat fogja használni. További információkért tekintse meg a helyszíni adatátjárókról szóló általános cikk leírását a [hitelesítő adatok](service-gateway-onprem.md#credentials) tárolásáról.
> 
> 

![](media/service-gateway-enterprise-manage-sap/datasourcesettings3-sap.png)

Miután mindent kitöltött, rákattinthat a **Hozzáadás** elemre.  Az adatforrás ettől kezdve használható ütemezett frissítéshez vagy DirectQuery-lekérdezéshez egy helyszíni SQL Server-kiszolgálón. Siker esetén megjelenik *A kapcsolat sikeresen létrejött* üzenet.

![](media/service-gateway-enterprise-manage-sap/datasourcesettings4.png)

### <a name="advanced-settings"></a>Speciális beállítások
Konfigurálhatja az adatforrás adatvédelmi szintjét. Ezzel szabályozható az adatgyűjtés módja. Ez a lehetőség csak az ütemezett frissítéseknél működik, a DirectQueryre nem vonatkozik. [További információk](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540)

![](media/service-gateway-enterprise-manage-sap/datasourcesettings9.png)

## <a name="remove-a-data-source"></a>Adatforrás eltávolítása
Az adatforrás eltávolítása hibát okoz az adott adatforrást használó irányítópultokon és jelentésekben.  

Adatforrás eltávolításához válassza az Adatforrás > **Eltávolítás** lehetőséget.

![](media/service-gateway-enterprise-manage-sap/datasourcesettings6.png)

## <a name="manage-administrators"></a>Rendszergazdák kezelése
Az átjáró Rendszergazdák lapján az átjárót rendszergazdai jogosultsággal kezelő felhasználókat (vagy biztonsági csoportokat) vehet fel és távolíthat el.

![](media/service-gateway-enterprise-manage-sap/datasourcesettings8.png)

## <a name="manage-users"></a>Felhasználók kezelése
A Felhasználók lapon az adatforrás használatára jogosult felhasználókat vagy biztonsági csoportokat vehet fel és távolíthat el.

> [!NOTE]
> A felhasználók listája csak azt szabja meg, hogy ki tehet közzé jelentéseket. A jelentések tulajdonosai irányítópultokat vagy tartalomcsomagokat hozhatnak létre, és oszthatnak meg más felhasználókkal.
> 
> 

![](media/service-gateway-enterprise-manage-sap/datasourcesettings5.png)

## <a name="using-the-data-source"></a>Az adatforrás használata
A létrehozott adatforrás elérhető lesz DirectQuery-kapcsolatokkal, vagy ütemezett frissítésen keresztül.

> [!NOTE]
> A kiszolgáló- és adatbázisnévnek meg kell egyeznie a Power BI Desktopban és a helyszíni adatátjáróban megadott adatforrásban!
> 
> 

Az adatkészlet és az átjárón belüli adatforrás kapcsolata a kiszolgáló és az adatbázis nevén alapul. Ezeknek egyezniük kell. Ha például IP-címet ad meg a kiszolgáló neveként a Power BI Desktopban, akkor az átjáró konfigurációjában is az IP-címet kell megadnia az adatforráshoz. Ha a Power BI Desktopban a *KISZOLGÁLÓ\PÉLDÁNY* formát használta, az átjáró konfigurációjában is ezt kell megadnia az adatforráshoz.

Ez a DirectQuery és az ütemezett frissítés esetén egyaránt érvényes.

### <a name="using-the-data-source-with-directquery-connections"></a>Az adatforrás használata DirectQuery-kapcsolatokkal
Gondoskodjon róla, hogy a kiszolgáló és az adatbázis neve megegyezzen a Power BI Desktopban és a helyszíni adatátjáróban konfigurált adatforrásban. DirectQuery-adatkészletek közzétételéhez arról is gondoskodnia kell, hogy a felhasználója szerepeljen az adatforrás **Felhasználók** lapján. A DirectQuery-hez történő kijelölésre a Power BI Desktopban az első adatimportáláskor kerül sor. [További információk](desktop-use-directquery.md)

A Power BI Desktop vagy az **Adatok beolvasása** lehetőség használatával történő közzététel után a jelentéseknek működniük kell. Az adatforrásnak az átjáróban történő létrehozása után eltelhet néhány perc, mire a kapcsolat használható lesz.

### <a name="using-the-data-source-with-scheduled-refresh"></a>Adatforrás használata ütemezett frissítéssel
Ha Ön szerepel az átjáróban konfigurált adatforrás **Felhasználók**  lapján, és a kiszolgáló- és adatbázisnevek egyeznek, akkor az átjáró megjelenik az ütemezett frissítéshez választható lehetőségek között.

![](media/service-gateway-enterprise-manage-sap/powerbi-gateway-enterprise-schedule-refresh.png)

## <a name="next-steps"></a>Következő lépések
[Helyszíni adatátjáró](service-gateway-onprem.md)  
[Helyszíni adatátjáró – részletesen](service-gateway-onprem-indepth.md)  
[A helyszíni adatátjáró hibaelhárítása](service-gateway-onprem-tshoot.md)  
További kérdései vannak? [Kérdezze a Power BI-közösséget](http://community.powerbi.com/)

