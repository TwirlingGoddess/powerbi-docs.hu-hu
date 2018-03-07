---
title: "Helyszíni adatátjáró proxybeállításainak konfigurálása"
description: "Információk a helyszíni adatátjáró proxybeállításainak konfigurálásáról."
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
ms.date: 11/21/2017
ms.author: davidi
LocalizationGroup: Gateways
ms.openlocfilehash: 27b8d36ed870501170efdb81c40edb6cb4727499
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="configuring-proxy-settings-for-the-on-premises-data-gateway"></a>Helyszíni adatátjáró proxybeállításainak konfigurálása
Munkakörnyezete megkövetelheti, hogy proxyn keresztül érje el az Internetet. Ez megakadályozhatja, hogy a helyszíni adatátjáró a szolgáltatáshoz kapcsolódjon.

## <a name="does-your-network-use-a-proxy"></a>Használ proxyt az Ön hálózata?
A superuser.com alábbi bejegyzése arról szól, hogy hogyan állapítható meg, használ-e proxyt az Ön hálózata.

[Honnan tudhatom, hogy milyen proxykiszolgálót használok? (SuperUser.com)](https://superuser.com/questions/346372/how-do-i-know-what-proxy-server-im-using)

## <a name="configuration-file-location-and-default-configuration"></a>A konfigurációs fájl helye és az alapértelmezett konfiguráció
A proxyadatok egy .NET-es konfigurációs fájlban vannak beállítva. A fájl helye és neve a használt átjárótól függően változó.

### <a name="on-premises-data-gateway"></a>Helyszíni adatátjáró
A helyszíni adatátjáró konfigurációjában két fő fájl játszik szerepet.

**Konfiguráció**

Az első az átjáró konfigurálására használt konfigurációs képernyőhöz való. Ha az átjáró konfigurálásával van problémája, akkor ezt a fájlt kell megvizsgálnia.

    C:\Program Files\On-premises data gateway\enterprisegatewayconfigurator.exe.config

**Windows-szolgáltatás**

A második a Power BI szolgáltatással kommunikáló és a kérelmeket kezelő Windows-szolgáltatásé.

    C:\Program Files\On-premises data gateway\Microsoft.PowerBI.EnterpriseGateway.exe.config

## <a name="configuring-proxy-settings"></a>Proxybeállítások konfigurálása
Az alapértelmezett proxykonfiguráció a következő.

    <system.net>
        <defaultProxy useDefaultCredentials="true" />
    </system.net>

Az alapértelmezett konfiguráció Windows-hitelesítéssel működik. Ha az Ön proxyja másféle hitelesítési formát használ, akkor módosítania kell a beállításokat. Ha nem biztos a dolgában, forduljon a hálózati rendszergazdához.

A .NET-konfigurációs fájlok proxy elemeinek konfigurációjáról a [defaultProxy elem (hálózati beállítások)](https://msdn.microsoft.com/library/kd3cf2ex.aspx) című cikkből tájékozódhat.

## <a name="changing-the-gateway-service-account-to-a-domain-user"></a>Az átjárószolgáltatás fiókjának módosítása egy tartományi felhasználóra
Ha a proxybeállításokat a fent ismertetett módon az alapértelmezett hitelesítő adatok használatára konfigurálja, akkor hitelesítési hibák merülhetnek fel. Ennek az az oka, hogy az alapértelmezett szolgáltatásfiók a szolgáltatás biztonsági azonosítója, nem pedig egy hitelesített tartományi felhasználó. A proxyn való megfelelő hitelesítés érdekében megváltoztathatja az átjáró szolgáltatásfiókját.

> [!NOTE]
> A kötelező jelszómódosítás elkerülése érdekében javasolt felügyelt szolgáltatásfiókot használni. Ismertető [felügyelt szolgáltatásfiók](https://technet.microsoft.com/library/dd548356.aspx) létrehozásáról az Active Directoryban.
> 
> 

### <a name="change-the-on-premises-data-gateway-service-account"></a>Helyszíni adatátjáró szolgáltatásfiókjának módosítása
1. Cserélje ki a Windows-szolgáltatásfiókot a **helyszíni adatátjáró szolgáltatáséra**.
   
    Ennek a szolgáltatásnak az alapértelmezett fiókja az *NT SERVICE\PBIEgwService*. Ezt érdemes felváltani egy olyan tartományi felhasználófiókkal, amely az Ön Active Directory-tartományában található. A kötelező jelszómódosítás elkerülése érdekében esetleg érdemes lehet felügyelt szolgáltatásfiókot használni.
   
    A fiók cseréjét a Windows-szolgáltatás tulajdonságai között, a **Bejelentkezés** oldalon hajthatja végre.
2. A **helyszíni adatátjáró-szolgáltatás** újraindítása.
   
    Rendszergazdai parancssorból adja ki a következő parancsokat.
   
        net stop PBIEgwService
   
        net start PBIEgwService
3. Indítsa el a **helyszíni adatátjáró konfiguráló programját**. Kattintson a Start gombra, és keressen rá a *helyszíni adatátjáró* kifejezésre.
4. Jelentkezzen be a Power BI-ba.
5. Állítsa helyre az átjárót a helyreállítási kulcs használatával.
   
    Ezzel teszi lehetővé, hogy az új szolgáltatásfiók visszafejtse az adatforrások eléréséhez szükséges tárolt hitelesítő adatokat.

## <a name="next-steps"></a>További lépések
[Helyszíni adatátjáró (személyes mód)](service-gateway-personal-mode.md)
[Tűzfal-információk](service-gateway-onprem-tshoot.md#firewall-or-proxy)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

