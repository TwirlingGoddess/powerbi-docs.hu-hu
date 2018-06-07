---
title: Helyszíni adatátjáró proxybeállításainak konfigurálása
description: Információk a helyszíni adatátjáró proxybeállításainak konfigurálásáról.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-gateways
ms.topic: conceptual
ms.date: 11/21/2017
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: c0ad0c22d0787eaaa45cb36c74c01f6a1d1f85e3
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34722658"
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

Az alapértelmezett hitelesítő adatok használatán kívül hozzáadhat <proxy> elemet is, így részletesebben definiálhatja a proxykiszolgáló beállításait. Meghatározhatja például, hogy a helyszíni adatárjáró még a helyi erőforrásokhoz is mindig használja a proxyt, ha a bypassonlocal paramétert false (hamis) értékre állítja. Ez segíthet a hibakeresésben, ha a proxy naplófájljában nyomon szeretne követni minden olyan http-kérelmet, amely egy helyszíni adatátjáróról érkezik. Az alábbi konfigurációs példa meghatározza, hogy minden kérelemnek egy meghatározott, 192.168.1.10 IP-című proxyn keresztül kell áthaladnia.

    <system.net>
        <defaultProxy useDefaultCredentials="true">
            <proxy  
                autoDetect="false"  
                proxyaddress="http://192.168.1.10:3128"  
                bypassonlocal="false"  
                usesystemdefault="true"
            />  
        </defaultProxy>
    </system.net>

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
2. Indítsa újra a **helyszíni adatátjáró-szolgáltatást**.
   
    Rendszergazdai parancssorból adja ki a következő parancsokat.
   
        net stop PBIEgwService
   
        net start PBIEgwService
3. Indítsa el a **helyszíni adatátjáró konfiguráló programját**. Kattintson a Start gombra, és keressen rá a *helyszíni adatátjáró* kifejezésre.
4. Jelentkezzen be a Power BI szolgáltatásba.
5. Állítsa helyre az átjárót a helyreállítási kulcs használatával.
   
    Ezzel teszi lehetővé, hogy az új szolgáltatásfiók visszafejtse az adatforrások eléréséhez szükséges tárolt hitelesítő adatokat.

## <a name="next-steps"></a>További lépések
[Helyszíni adatátjáró (személyes mód)](service-gateway-personal-mode.md)
[Tűzfal-információk](service-gateway-onprem-tshoot.md#firewall-or-proxy)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

