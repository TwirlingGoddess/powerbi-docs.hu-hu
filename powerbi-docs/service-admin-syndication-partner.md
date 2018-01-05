---
title: "Nem sikerült hozzáadni a Power BI-t az O365-partnerhez"
description: "Nem sikerült hozzáadni a Power BI-t az Office 365 típusú szindikálási partnerhez. A szindikálási modell az Office 365 által használt egyik beszerzési modell."
services: powerbi
documentationcenter: 
author: guyinacube
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
ms.date: 09/05/2017
ms.author: asaxton
ms.openlocfilehash: e5b2540461464e64acac4bc3b2be2e6ac5ee3f1d
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="unable-to-add-power-bi-to-office-365-partner-subscription"></a>Nem sikerült hozzáadni a Power BI-t az Office 365 típusú partneri előfizetéshez
Az Office 365 lehetővé teszi a cégeknek az Office 365 saját megoldásokkal integrált, csomagalapú továbbértékesítését, és a cégek egyetlen kapcsolatfelvételi pontot biztosíthatnak a végfelhasználóknak a vásárláshoz, a számlázáshoz és a támogatáshoz.

Ha érdekli a Power BI és az Office 365-előfizetés együttes beszerzése, javasoljuk, hogy érdeklődjön a partnernél ezzel kapcsolatban. Ha a partner kínálatában nem szerepel a Power BI, különböző lehetőségeket vehet fontolóra.

1. Megvásárolhatja a szolgáltatást egy másik csatornán, közvetlenül a Microsofttól vagy egy másik partnertől. Ez a lehetőség nem érhető el minden ügyfélnek, a partnerrel való kapcsolattól függ. A lehetőség meglétét az **Office 365 felügyeleti portál** > **Számlázás** > **Előfizetések** menüpontjának megnyitásával ellenőrizheti. Ha látja az **Előfizetések** elemet, közvetlenül vásárolhatja meg a szolgáltatást a Microsofttól, vagy felveheti a kapcsolatot egy olyan partnerrel, akinek a kínálatában szerepel a Power BI.
   
    ![](media/service-admin-syndication-partner/billingsub.png)
2. Ha nem látja az **Előfizetések** elemet a **Számlázás** menüpontban, nem vásárolhat közvetlenül a Microsofttól vagy egy másik partnertől. 
   
   ![](media/service-admin-syndication-partner/billing.png)

Ha nem tudja közvetlenül megvásárolni a Power BI-t, attól függően, hogy milyen típusú Power BI-előfizetés érdekli, más lehetőségei is vannak.

[Power BI (ingyenes)](#power-bi-free)

[Power BI Pro és Premium](#power-bi-pro)

## <a name="power-bi-free"></a>Power BI (ingyenes)
Ha elégedett az ingyenesen elérhető Power BI-jal, regisztrálhat az ingyenes szolgáltatásra. Az egyéni regisztrációk (más néven alkalmi előfizetések), alapértelmezés szerint le vannak tiltva. Ha regisztrálni próbál a Power BI szolgáltatásra, egy üzenet jelenik meg, amely arról tájékoztat, hogy az informatikai részleg kikapcsolta a Microsoft Power BI-regisztrációt.

    Your IT department has turned off signup for Microsoft Power BI.

![](media/service-admin-syndication-partner/sorry.png)

Az alkalmi előfizetések engedélyezéséhez megkérheti a partnert, hogy kapcsolja be azt. Ha Ön a bérlő rendszergazdája, és ismeri az Azure Active Directory PowerShell-parancsok használatát, saját maga is engedélyezheti az alkalmi előfizetéseket. [További információ](https://technet.microsoft.com/library/jj151815.aspx)

1. Először jelentkezzen be az Azure Active Directoryba az Office 365 hitelesítő adataival. Az első sor kérni fogja a hitelesítő adatokat. A második sor kapcsolódik az Azure Active Directoryhoz.
   
        $msolcred = get-credential
        connect-msolservice -credential $msolcred
   
    ![](media/service-admin-syndication-partner/aad-signin.png)
2. Ha már bejelentkezett, kiadhatja az alábbi parancsot az ingyenes regisztráció engedélyezéséhez.
   
        Set-MsolCompanySettings -AllowAdHocSubscriptions $true

## <a name="power-bi-pro-and-premium"></a>Power BI Pro és Premium
Ha szeretne Power BI Pro- vagy Power BI Premium-előfizetést vásárolni, a partnerrel együttműködve kell mérlegelnie a rendelkezésre álló lehetőségeket.

* A partner beleegyezik abba, hogy felvegye a Power BI-t a portfóliójába, így megvásárolhatja azt tőle.
* A partner segítségével olyan modellre válthat, amelyben a Power BI közvetlenül a Microsofttól vagy egy Power BI-t értékesítő másik partnertől vásárolható meg.

Az alábbi videó az Office 365-szindikálást és a Power BI megvásárlását ismerteti:

<iframe width="560" height="315" src="https://www.youtube.com/embed/C357phT94A8" frameborder="0" allowfullscreen></iframe>

## <a name="next-steps"></a>Következő lépések
[Az Azure AD kezelése a Windows PowerShell használatával](https://technet.microsoft.com/library/jj151815.aspx)  
[Mi a Power BI Premium?](service-premium.md)

További kérdései vannak? [Kérdezze a Power BI-közösséget!](http://community.powerbi.com/)
