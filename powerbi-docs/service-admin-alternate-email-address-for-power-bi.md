---
title: Másodlagos e-mail-cím használata
description: Másodlagos e-mail-cím használata
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 03/08/2018
ms.author: mblythe
LocalizationGroup: Troubleshooting
ms.openlocfilehash: 5013c70e4d3998eb39e0de2a92f890417175fd62
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34240906"
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

## <a name="updating-through-azure-active-directory"></a>Frissítés az Azure Active Directoryn keresztül
Active Azure Directory (AAD) Power BI-hoz tartozó beágyazási tokenjének rögzítésekor háromféle e-mail-típus használható. A három különböző típus a következő:

* a felhasználó AAD-fiókjához tartozó fő e-mail-cím
* az egyszerű felhasználónévhez (UPN) tartozó e-mail-cím
* az „other” e-mail-tömbattribútum

A Power BI a következő szempontok alapján választja ki a használandó e-mail-címet:
1.  Ha az AAD-bérlő felhasználói objektumának „mail” attribútuma létezik, akkor a Power BI ezt az attribútumot használja e-mail-címként
2.  Ha az UPN-hez tartozó e-mail-cím *nem* az **\*.onmicrosoft.com** tartománybeli cím (ez a „\@” jelet követő részből derül ki), akkor a Power BI ezt az attribútumot használja e-mail-címként
3.  Ha az AAD-s felhasználói objektum „other” e-mail-tömbattribútuma ki van töltve, akkor az ebben a listában szereplő első e-mail-cím lesz használva (mivel ez az attribútum e-mail-címek listáját is tartalmazhatja)
4. Ha a fenti feltételek egyike sem teljesül, akkor az UPN-cím lesz használva

## <a name="updating-with-powershell"></a>Frissítés a PowerShell-lel
Másik megoldásként a PowerShell vagy az Azure Active Directory használatával is frissítheti a másodlagos e-mail-címet. Ezt a [Set-AzureADUser](https://docs.microsoft.com/powershell/module/azuread/set-azureaduser) paranccsal teheti meg.

```
Set-AzureADUser -ObjectId john@contoso.com -OtherMails "otheremail@somedomain.com"
```

További információkért lásd: [Azure Active Directory PowerShell 2-es verziója](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

