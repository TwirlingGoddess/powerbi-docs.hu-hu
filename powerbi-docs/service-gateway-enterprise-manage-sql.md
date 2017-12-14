---
title: "Adatforrások kezelése – SQL"
description: "Helyszíni adatátjáró és az átjáróhoz tartozó adatforrások kezelése."
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
ms.date: 11/02/2017
ms.author: davidi
ms.openlocfilehash: 95fccd70b536a26baf93bf4735750e5599e3021f
ms.sourcegitcommit: 8f72ce6b35aa25979090a05e3827d4937dce6a0d
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/27/2017
---
# <a name="manage-your-data-source---sql-server"></a>Adatforrások kezelése – SQL Server
A helyszíni adatátjáró telepítése után az átjáróval használható adatforrásokat adhat hozzá. Ez a cikk az átjárókkal és adatforrásokkal végzett munkához nyújt útmutatást. Az SQL Server-adatforrás ütemezett frissítéshez vagy DirectQueryhez is használható.

## <a name="download-and-install-the-gateway"></a>Az átjáró letöltése és telepítése
Az átjáró letölthető a Power BI szolgáltatásból. Válassza a **Letöltések** > **Adatátjáró** lehetőséget, vagy nyissa meg az [átjáró letöltési oldalát](https://go.microsoft.com/fwlink/?LinkId=698861).

![](media/service-gateway-enterprise-manage-sql/powerbi-download-data-gateway.png)

## <a name="add-a-gateway"></a>Átjáró hozzáadása
Átjáró hozzáadásához egyszerűen [töltse le](https://go.microsoft.com/fwlink/?LinkId=698861) és telepítse az átjárót a saját környezetének egyik kiszolgálójára. Az átjáró a telepítése után megjelenik az **Átjárók kezelése** alatti listában.

> [!NOTE]
> Az **Átjárók kezelése** csak akkor jelenik meg, ha Ön legalább egy átjárónak rendszergazdája. Ez úgy lehetséges, hogy rendszergazdaként hozzáadják egy átjáróhoz, vagy saját maga telepít és konfigurál egy átjárót.
> 
> 

## <a name="remove-a-gateway"></a>Átjáró eltávolítása
Egy átjáró eltávolítása az átjáró alá tartozó valamennyi adatforrás törlésével jár.  Ez az ezekre az adatforrásokra épülő irányítópultokon és jelentésekben is hibát okoz.

1. Válassza a fogaskerék ![](media/service-gateway-enterprise-manage-sql/pbi_gearicon.png) ikont a jobb felső sarokban > **Átjárók kezelése**.
2. Átjáró > **Eltávolítás**
   
   ![](media/service-gateway-enterprise-manage-sql/datasourcesettings7.png)

## <a name="add-a-data-source"></a>Adatforrás hozzáadása
Adatforrást hozzáadhat úgy, hogy az átjárót kijelölve az **Adatforrás hozzáadása** lehetőségre kattint, vagy az Átjáró > **Adatforrás hozzáadása** lehetőség használatával.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings1.png)

Ez után kiválaszthatja az **Adatforrástípust** a listából.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings2.png)

> [!NOTE]
> DirectQuery használatakor az átjáró csak az **SQL Server 2012 SP1** és későbbi verzióit támogatja.
> 
> 

Ez után az adatforrás információit, köztük a **Kiszolgálót** és az **Adatbázist** is kell megadnia.  

Ki kell választania a **Hitelesítési módszert** is.  Ez lehet **Windows** vagy **Egyszerű**.  Az **Egyszerű** lehetőséget akkor kell választani, ha Windows-hitelesítés helyett SQL-hitelesítést fog használni. Végül adja meg az ehhez az adatforráshoz használandó hitelesítő adatokat.

> [!NOTE]
> Az adatforráson minden lekérdezés ezekkel a hitelesítő adatokkal fog futni, hacsak nincs hozzá konfigurálva és engedélyezve a Kerberos használata egyszeri bejelentkezéshez (SSO). Egyszeri bejelentkezés (SSO) használata esetén az importált adatkészletek a tárolt hitelesítő adatokat használják, a DirectQuery-adatkészletek viszont az aktuális Power BI-felhasználó nevében, SSO használatával futtatják a lekérdezéseket. A helyszíni adatátjáróról szóló fő cikkben bővebben tájékozódhat a [hitelesítő adatok](service-gateway-onprem.md#credentials) tárolásáról. További információ: [a Kerberos használata egyszeri bejelentkezéshez (SSO) a Power BI-ból helyszíni adatforrásokba](service-gateway-kerberos-for-sso-pbi-to-on-premises-data.md).
> 
> 

![](media/service-gateway-enterprise-manage-sql/datasourcesettings3.png)

Miután mindent kitöltött, rákattinthat a **Hozzáadás** gombra.  Az adatforrás ettől kezdve használható ütemezett frissítéshez vagy DirectQuery-lekérdezéshez egy helyszíni SQL Server kiszolgálón. Siker esetén az *A kapcsolat sikeresen létrejött* üzenet jelenik meg.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings4.png)

### <a name="advanced-settings"></a>Speciális beállítások
Konfigurálhatja az adatforrás adatvédelmi szintjét. Ezzel szabja meg, hogy hogyan érhetők el az adatok. Ezt csak az ütemezett frissítések használják. A DirectQueryre nem vonatkozik. [További információ](https://support.office.com/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540)

![](media/service-gateway-enterprise-manage-sql/datasourcesettings9.png)

## <a name="remove-a-data-source"></a>Adatforrás eltávolítása
Egy adatforrás eltávolítása hibát okoz az adott adatforrást használó irányítópultokon és jelentésekben.  

Adatforrás eltávolításához válassza az Adatforrás > **Eltávolítás** lehetőséget.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings6.png)

## <a name="manage-administrators"></a>Rendszergazdák kezelése
Az átjáró Rendszergazdák lapján az átjárót rendszergazdai jogosultsággal kezelő felhasználókat (vagy biztonsági csoportokat) vehet fel és távolíthat el.

![](media/service-gateway-enterprise-manage-sql/datasourcesettings8.png)

## <a name="manage-users"></a>Felhasználók kezelése
A Felhasználók lapon az adatforrás használatára jogosult felhasználókat vagy biztonsági csoportokat vehet fel és távolíthat el.

> [!NOTE]
> A felhasználók listája csak azt szabja meg, hogy ki tehet közzé jelentéseket. Irányítópultokat vagy tartalomcsomagokat a jelentések tulajdonosai hozhatnak létre és oszthatnak meg más felhasználókkal.
> 
> 

![](media/service-gateway-enterprise-manage-sql/datasourcesettings5.png)

## <a name="using-the-data-source"></a>Az adatforrás használata
A létrehozott adatforrás elérhető lesz DirectQuery-kapcsolattal vagy ütemezett frissítésen keresztül.

> [!NOTE]
> A kiszolgáló- és adatbázisnévnek meg kell egyeznie a Power BI Desktopban és a helyszíni adatátjáróban megadott adatforrásban!
> 
> 

Az adatkészlet és az átjárón belüli adatforrás kapcsolata a kiszolgáló és az adatbázis nevén alapul. Ezeknek egyezniük kell. Ha például IP-címet ad meg a kiszolgáló neveként a **Power BI Desktopban**, akkor az átjáró konfigurációjában is az IP-címet kell megadnia az adatforráshoz. Ha a Power BI Desktopban a *KISZOLGÁLÓ\PÉLDÁNY* formát használta, az átjáró konfigurációjában is ezt kell megadnia az adatforráshoz.

Ez a DirectQuery használata és az ütemezett frissítés esetén is érvényes.

### <a name="using-the-data-source-with-directquery-connections"></a>Az adatforrás használata DirectQuery-kapcsolatokkal
Gondoskodjon róla, hogy a kiszolgáló- és adatbázis-név megegyezzen a **Power BI Desktopban** és a helyszíni adatátjáróban konfigurált adatforrásban. DirectQuery-adatkészletek közzétételéhez arról is gondoskodnia kell, hogy a felhasználója szerepeljen az adatforrás **Felhasználók** lapján. A DirectQuery estén a kijelölésre a Power BI Desktopban az első adatimportáláskor kerül sor. [További információ](desktop-use-directquery.md)

A Power BI Desktop vagy az **Adatok beolvasása** lehetőség használatával történő közzététel után a jelentéseknek működniük kell. Az adatforrásnak az átjáróban történő létrehozása után eltelhet néhány perc, mire a kapcsolat használható lesz.

### <a name="using-the-data-source-with-scheduled-refresh"></a>Adatforrás használata ütemezett frissítéssel
Ha Ön szerepel az átjáróban konfigurált adatforrás **Felhasználók** lapján, és a kiszolgáló- és adatbázisnevek egyeznek, akkor az átjáró megjelenik az ütemezett frissítéshez választható lehetőségek között.

![](media/service-gateway-enterprise-manage-sql/powerbi-gateway-enterprise-schedule-refresh.png)

## <a name="next-steps"></a>További lépések
* [Helyszíni adatátjáró](service-gateway-onprem.md)  
* [Helyszíni adatátjáró – részletesen](service-gateway-onprem-indepth.md)  
* [A helyszíni adatátjáró hibaelhárítása](service-gateway-onprem-tshoot.md)
* [Kerberos használata egyszeri bejelentkezéshez (SSO) a Power BI-ból a helyszíni adatforrásokhoz](service-gateway-kerberos-for-sso-pbi-to-on-premises-data.md). 
* További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

