---
title: Power BI Pro-licencek felhasználókhoz rendelése
description: Power BI Pro-licencek felhasználókhoz rendelése
services: powerbi
documentationcenter: ''
author: mgblythe
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 03/22/2018
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: cc22bfa635bb9d91624e6d4a5cdfe301d6478af6
ms.sourcegitcommit: 8552a34df8e6141eb704314c1a019992901d6e78
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/08/2018
---
# <a name="assigning-power-bi-pro-licenses"></a>Power BI Pro-licencek felhasználókhoz rendelése

A rendszergazdák több felügyeleti portál és PowerShell-parancsmag segítségével is elvégezhetik a Power BI Pro-licencek felhasználókhoz rendelését. A Power BI-licencek kezelését a háttérben az Azure Active Directory (Azure AD) végzi.

* Az Azure-előfizetéssel rendelkező felhasználók használhatják az Azure Active Directory panelt az [Azure Portalon](https://ms.portal.azure.com/#@microsoft.onmicrosoft.com/dashboard/private/39bc3cf7-31a4-43f6-954c-f2d69ca2f0). 

* A globális rendszergazdák és a felhasználói fiókok rendszergazdái használhatják az [Office 365 Felügyeleti központot](https://portal.office.com/AdminPortal/Home#/homepage).

## <a name="managing-power-bi-pro-licenses-in-the-azure-portal"></a>Power BI Pro-licencek kezelése az Azure Portalon

A Power BI az Azure AD szolgáltatásaira épül. Az Azure AD tárolja a felhasználói fiókokat és csoportokat, valamint az egyéb beállításokat, például a megvásárolt termékek információit.

### <a name="assigning-licenses-to-individual-user-accounts"></a>Licencek hozzárendelése egyéni felhasználói fiókokhoz

Ha rendelkezik Azure-előfizetéssel, az alábbi lépésekkel hozzárendelheti a Pro-licenceket egyéni felhasználói fiókokhoz:

1. Nyissa meg az [Azure Portalt](https://ms.portal.azure.com/#@microsoft.onmicrosoft.com/dashboard/private/39bc3cf7-31a4-43f6-954c-f2d69ca2f0). 

2. Válassza a bal oldali navigációs sávon az Azure Active Directory lehetőséget.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-01.png)

3. Az Azure Active Directory panelen válassza a Licencek lehetőséget.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-02.png)

4. A licencelt felhasználók listájának megjelenítéséhez a Licencek panelen válassza a Minden termék lehetőséget, majd válassza a Power BI Pro lehetőséget.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-03.png)

5. Power BI Pro-licenc további felhasználói fiókhoz való rendeléséhez válassza a Hozzárendelés lehetőséget.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-04.png)

> [!NOTE]
> A licenceléssel kapcsolatos legtöbb feladatot végrehajthatja az Azure Portalon, további Power BI Pro-licenceket azonban itt nem tud vásárolni. Power BI Pro-licencek vásárlásához használja az Office 365 Felügyeleti központot. További információkért lásd: [A Power BI Pro megvásárlása](https://docs.microsoft.com/en-us/power-bi/service-admin-purchasing-power-bi-pro).
>

## <a name="managing-power-bi-pro-licenses-in-the-office-365-admin-center"></a>Power BI Pro-licencek kezelése az Office 365 Felügyeleti központban

Ha Ön globális rendszergazda, akkor az Office 365 Felügyeleti központban megvásárolhatja a Power BI Pro-előfizetéseket, és kezelheti a cég vonatkozó licenceit.

Office 365-ös rendszergazdaként az alábbi lépésekkel rendelheti hozzá a Pro-licenceket egyéni felhasználói fiókokhoz:

1. Keresse fel az Office 365 felügyeleti központot.

2. A bal oldali navigációs panelen válassza a Felhasználók, majd az „Aktív felhasználók” lehetőséget.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-05.png)

3. Jelöljön ki egy vagy több felhasználót, és kattintson a „Terméklicencek szerkesztése” lehetőségre.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-06.png)

4. A Power BI Pro területen állítsa a kapcsolót Be állásra, majd kattintson a Mentés gombra.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-07.png)

5. Az Állapot oszlopban ellenőrizze, hogy a kijelölt fiók(ok)hoz sikeresen hozzá lett-e rendelve a Power BI Pro-licenc.

    ![image](media/service-assigning-power-bi-pro-licenses/service-assigning-power-bi-pro-licenses-08.png)

> [!NOTE]
> Ha nincs több felhasználható licenc az előfizetésében, további licencek hozzáadásához bontsa ki a Számlázás csoportot a bal oldali navigációs panelen, és válassza az Előfizetések lehetőséget. Az Előfizetések lapon válassza a Power BI Pro előfizetést, majd kattintson a „Licencek hozzáadása/eltávolítása” hivatkozásra.
>

## <a name="next-steps"></a>Következő lépések
[A Power BI Pro használata a szervezetben](service-admin-power-bi-pro-in-your-organization.md)
</br>
[A Pro meghosszabbított próbaverziójának aktiválása](service-extended-pro-trial.md)
</br>
[A Power BI szolgáltatási szerződése egyéni felhasználók számára](https://powerbi.microsoft.com/terms-of-service/)
</br>
[A Power BI Premium hirdetménye](https://aka.ms/pbipremium-announcement)
</br>
[Bejelentkezett Power BI-felhasználók keresése](service-admin-access-usage.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)