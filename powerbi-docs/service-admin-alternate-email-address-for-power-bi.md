---
title: "Másodlagos e-mail-cím használata"
description: "Másodlagos e-mail-cím használata"
services: powerbi
documentationcenter: 
author: markingmyname
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 08/09/2017
ms.author: maghan
LocalizationGroup: Troubleshooting
ms.openlocfilehash: c97f60e39d68060c8eb3396bac4eb7725dab9c86
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="using-an-alternate-email-address"></a>Másodlagos e-mail-cím használata
Alapértelmezés szerint a rendszer a Power BI-ba való regisztráláshoz használt e-mail-címre küld tájékoztatást a Power BI-ban végzett tevékenységekről.  Ha például valaki megosztási felkérést küld Önnek, az erre az e-mail-címre fog megérkezni.

Előfordulhat, hogy azt szeretné, hogy ezek az e-mailek a Power BI-ba való regisztráláshoz használt eredeti e-mail-cím helyett egy másodlagos e-mail-címre érkezzenek.

## <a name="updating-through-office-365-personal-info-page"></a>Frissítés az Office 365 Személyi adatok oldalán keresztül
1. Nyissa meg az [Office 365 Személyi adatok oldalát](https://portal.office.com/account/#personalinfo).  Ha a rendszer kéri, jelentkezzen be a Power BI-hoz használt e-mail-címmel és jelszóval.
2. Kattintson a szerkesztés hivatkozásra a Kapcsolattartási adatok szakaszban.  
   
   > [!NOTE]
   > Ha nem látja a Szerkesztés hivatkozást, akkor az e-mail-címet az Office 365-rendszergazdája kezeli, és az e-mail-cím frissítéséhez fel kell vele venni a kapcsolatot.
   > 
   > 
   
   ![](media/service-admin-alternate-email-address-for-power-bi/contact-details.png)
3. A Másodlagos e-mail-cím mezőbe írja be az e-mail-címet, amelyre szeretné, hogy a Power BI a frissítéseket küldje.

> [!NOTE]
> A beállítás megváltoztatása nem érinti azt az e-mail-címet, amelyre a rendszer a szolgáltatási híreket, hírleveleket és egyéb promóciós leveleket küldi.  Ezek mindig a Power BI-ba való regisztráláshoz használt eredeti e-mail-címre fognak érkezni.
> 
> 

## <a name="updating-with-powershell"></a>Frissítés a PowerShell-lel
Másik megoldásként a PowerShell vagy az Azure Active Directory használatával is frissítheti a másodlagos e-mail-címet. Ezt a [Set-AzureADUser](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser) paranccsal teheti meg.

```
Set-AzureADUser -ObjectId john@contoso.com -OtherMails "otheremail@somedomain.com"
```

További információkért lásd: [Azure Active Directory PowerShell 2-es verziója](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

