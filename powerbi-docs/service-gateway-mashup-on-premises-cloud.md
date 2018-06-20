---
title: Helyszíni és felhőbeli adatforrások egyesítése vagy összefűzése
description: A helyszíni adatátjáró használata a helyszíni és a felhőbeli adatforrások egyesítésére vagy összeűzésére egyetlen lekérdezésbe.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-gateways
ms.topic: conceptual
ms.date: 06/06/2018
ms.author: mblythe
LocalizationGroup: Gateways
ms.openlocfilehash: 3550a3fc0cfc51b61e1d7e51a50c2a36325f2388
ms.sourcegitcommit: 49570ab8f5b5cd5bab4cd388f4281b1372bcb80b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/09/2018
ms.locfileid: "35250660"
---
# <a name="merge-or-append-on-premises-and-cloud-data-sources"></a>Helyszíni és felhőbeli adatforrások egyesítése vagy összefűzése

A helyszíni adatátjáró lehetővé teszi, hogy a helyszíni és a felhőbeli adatforrásokat egyesítse vagy összefűzze ugyanazon a lekérdezésen belül. Ez a funkció olyankor hasznos, ha különböző adatforrásokból kíván adatokat lekérni, de nem szeretne több külön lekérdezést használni.

## <a name="prerequisites"></a>Előfeltételek

- A helyi számítógépen [telepített átjáró](service-gateway-install.md).
- Egy Power BI Desktop-fájl, amely helyszíni és felhőbeli adatforrásokat kombináltan használó lekérdezéseket tartalmaz.

1. Válassza a Power BI szolgáltatás jobb felső sarkában lévő fogaskerék ikont ![Beállítások fogaskerék ikonja](media/service-gateway-mashup-on-premises-cloud/icon-gear.png) > **Átjárók kezelése**.

    ![Átjárók kezelése](media/service-gateway-mashup-on-premises-cloud/manage-gateways.png)

2. Válassza ki a konfigurálni kívánt átjárót.

3. Az **Átjárófürt beállításai** fülön válassza **Az ezen átjárófürtön keresztüli frissítés engedélyezése a felhasználó felhőalapú adatforrásai számára** > **Alkalmaz** lehetőséget.

    ![Frissítés az átjárófürtön keresztül](media/service-gateway-mashup-on-premises-cloud/refresh-gateway-cluster.png)

4. Az átjárófürtnél vegye fel a lekérdezésekben használt [helyszíni adatforrásokat](service-gateway-enterprise-manage-scheduled-refresh.md#add-a-data-source). A felhőbeli adatforrásokat nem szükséges itt megadnia.

4. Töltse fel a helyszíni és felhőbeli adatforrásokat kombináltan használó lekérdezéseket tartalmazó Power BI Desktop-fájlt a Power BI szolgáltatásba.

5. Az új adathalmazhoz tartozó **Adathalmaz beállításai** lapon:

    - A helyszíni adatforrásnál válassza ki az adatforráshoz társított átjárót.

    - Az **Adatforrás azonosító adatai** szakasznál szükség szerint módosítsa az adatforrás azonosító adatait.

    ![Adathalmaz beállításai](media/service-gateway-mashup-on-premises-cloud/dataset-settings.png)

6. Most, hogy beállította a felhőbeli hitelesítéseket, a **Frissítés most** lehetőség választásával azonnal frissítheti az adathalmazt, de ütemezhet rendszeres frissítést is.


## <a name="next-steps"></a>Következő lépések

Az átjárók adatfrissítésével kapcsolatban további információt [Az adatforrás használata ütemezett frissítéshez](service-gateway-enterprise-manage-scheduled-refresh.md#using-the-data-source-for-scheduled-refresh) című cikkben talál.