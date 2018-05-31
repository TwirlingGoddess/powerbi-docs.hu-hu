---
title: 'Rövid útmutató: Power BI Pro-licencek felhasználókhoz rendelése az Azure-ban'
description: Ismerkedjen meg a Power BI Pro-licencek hozzárendelésével, hogy felhasználói minden tartalomhoz és funkcióhoz hozzáférhessenek a Power BI szolgáltatásban.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: quickstart
ms.date: 05/03/2018
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: d092fc26f913028f7ce30ab6b2f860d75c5db2b7
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
ms.locfileid: "34294433"
---
# <a name="quickstart-assign-power-bi-pro-licenses-in-azure"></a>Rövid útmutató: Power BI Pro-licencek felhasználókhoz rendelése az Azure-ban

A Power BI Pro egyéni licenc, amely hozzáférést biztosít a Power BI szolgáltatásban minden tartalomhoz és funkcióhoz, többek között megosztható a tartalom, és lehetőség van más Pro-felhasználókkal való együttműködésre is. Csak a Pro szintű felhasználók tehetnek közzé és használhatnak tartalmat alkalmazás-munkaterületeken, oszthatnak meg irányítópultokat, és iratkozhatnak fel irányítópultokra és jelentésekre. Ez a cikk azt ismerteti, hogyan végezhető el a Power BI Pro-licenc hozzárendelése az Azure-ban. Licenceket az [Office 365-ben is hozzárendelhet](service-admin-assigning-power-bi-pro-licenses.md).


## <a name="prerequisites"></a>Előfeltételek

A Power BI által Active Directory-keresésekhez használt Azure-előfizetés tulajdonosának kell lennie.

A kezdéshez [legalább egy licencet meg kell vásárolnia](service-admin-purchasing-power-bi-pro.md).


## <a name="assign-licenses-to-individual-user-accounts"></a>Licencek hozzárendelése egyéni felhasználói fiókokhoz

Az alábbi lépésekkel rendelheti hozzá a Power BI Pro-licenceket egyéni felhasználói fiókokhoz:

1. Nyissa meg az [Azure Portalt](https://ms.portal.azure.com/#@microsoft.onmicrosoft.com/dashboard/private/39bc3cf7-31a4-43f6-954c-f2d69ca2f0). 

2. A bal oldali navigációs sávon válassza az **Azure Active Directory** lehetőséget.

    ![Azure Active Directory](media/service-admin-assigning-power-bi-pro-licenses-azure/service-assigning-power-bi-pro-licenses-01.png)

3. Az **Azure Active Directory** alatt válassza a **Licencek** lehetőséget.

    ![Licencek](media/service-admin-assigning-power-bi-pro-licenses-azure/service-assigning-power-bi-pro-licenses-02.png)

4. A **Licencek** alatt válassza a **Minden termék**, majd a **Power BI Pro** lehetőséget a licenccel rendelkező felhasználók listájának megjelenítéséhez.

    ![Licencek – Minden termék](media/service-admin-assigning-power-bi-pro-licenses-azure/service-assigning-power-bi-pro-licenses-03.png)

5. Power BI Pro-licenc további felhasználói fiókhoz való rendeléséhez válassza a **Hozzárendelés** lehetőséget.

    ![Licenc hozzárendelése](media/service-admin-assigning-power-bi-pro-licenses-azure/service-assigning-power-bi-pro-licenses-04.png)


## <a name="next-steps"></a>Következő lépések

Javasoljuk, hogy a licencek hozzárendelése után ismerkedjen meg közelebbről is a Power BI Pro használatával.

[A Power BI Pro használata a szervezetben](service-admin-power-bi-pro-in-your-organization.md)

[Bejelentkezett Power BI-felhasználók keresése](service-admin-access-usage.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)