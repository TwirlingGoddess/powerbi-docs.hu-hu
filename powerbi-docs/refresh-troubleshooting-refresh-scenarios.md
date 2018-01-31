---
title: "Frissítési forgatókönyvekkel kapcsolatos hibák elhárítása"
description: "Frissítési forgatókönyvekkel kapcsolatos hibák elhárítása"
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
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/24/2018
ms.author: davidi
ms.openlocfilehash: b668a1f47593e4551971146ec0d06f0d883ca812
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/25/2018
---
# <a name="troubleshooting-refresh-scenarios"></a>Frissítési forgatókönyvekkel kapcsolatos hibák elhárítása
Itt a Power BI szolgáltatásban az adatok frissítése során fellépő különféle forgatókönyvekkel kapcsolatos információkat talál.

> [!NOTE]
> Ha olyan helyzet miatt tapasztal problémákat, amely nem szerepel az alábbi listán, a [közösségi webhelyen](http://community.powerbi.com/) kérhet további segítséget, vagy létrehozhat egy [támogatási jegyet](https://powerbi.microsoft.com/support/).
> 
> 

## <a name="refresh-using-web-connector-doesnt-work-properly"></a>A webes összekötő használatával végzett frissítés nem megfelelően működik
Ha egy olyan webes összekötő szkripttel rendelkezik, amely a [**Web.Page**](https://msdn.microsoft.com/library/mt260924.aspx) függvényt használja, és az adatkészlet vagy jelentés kódját 2016. november 18. után frissítette, átjárót kell használnia, hogy az adatfrissítés megfelelően működjön.

## <a name="unsupported-data-source-for-refresh"></a>A frissítéshez nem támogatott adatforrások
Az adatkészletek konfigurálása során hibaüzenetet kaphat, miszerint az adatkészlet nem támogatott adatforrást használ a frissítéshez. Részletekért lásd: [A frissítéshez nem támogatott adatforrásokkal kapcsolatos hibák elhárítása](service-admin-troubleshoot-unsupported-data-source-for-refresh.md).

## <a name="dashboard-doesnt-reflect-changes-after-refresh"></a>Az irányítópulton nem jelennek meg a módosítások a frissítés után
Várjon körülbelül 10-15 percet, hogy a frissített adatok megjelennek az irányítópult csempéin.  Ha ekkor sem jelennek meg, rögzítse újra a vizualizációt az irányítópulton.

## <a name="gatewaynotreachable-when-setting-credentials"></a>GatewayNotReachable hibaüzenet a hitelesítő adatok beállításakor
Az adatforrások hitelesítő adatainak beállításkor előfordulhat, hogy a GatewayNotReachable hibaüzenet jelenik meg. Ennek az oka egy elavult átjáró lehet.  Telepítse a legfrissebb átjárót, és próbálkozzon újra.

## <a name="processing-error-the-following-system-error-occurred-type-mismatch"></a>Feldolgozási hiba: A következő rendszerhiba történt: Típuseltérés
Ezt az M szkript hibája okozhatja a Power BI Desktop-fájlban vagy Excel-munkafüzetben.  Az is okozhatja, hogy a Power BI Desktop verziója elavult.

## <a name="tile-refresh-errors"></a>Csempefrissítési hibák
Az irányítópult csempéivel kapcsolatos hibák és magyarázatok listáját lásd: [Csempehibák elhárítása](refresh-troubleshooting-tile-errors.md).

## <a name="refresh-fails-when-updating-data-from-sources-that-use-aad-oauth"></a>Az adatfrissítés az AAD OAuth hitelesítést használó forrásokból származó adatok frissítésekor meghiúsul
A számos különböző adatforrás által használt Azure Active Directory (**AAD**) OAuth token hozzávetőleg egy óra elteltével elévül. Előfordulhatnak olyan helyzetek, amikor az adatok frissítése a token elévülési idejénél (azaz egy óránál) tovább tart, mivel a Power BI szolgáltatás akár két órát is várakozhat az adatok betöltése során. Ilyen esetekben az adatbetöltési folyamat hitelesítési hibával meghiúsulhat.

AAD OAuth-hitelesítést használó adatforrások közé tartozik a **Microsoft Dynamics CRM Online** és a **SharePoint Online** (SPO). Ha ilyen adatforrásokhoz kapcsolódik, és hitelesítési hibát kap, amikor az adatok betöltése egy óránál tovább tart, ez lehet az ok.

A Microsoft jelenleg vizsgálja egy olyan megoldás kidolgozásának lehetőségeit, amelyben az adatfrissítési folyamat ilyenkor frissíti a tokent, és folytatja a feldolgozást. Ha azonban a Dynamics CRM Online- vagy SharePoint Online-példány (vagy egyéb AAD OAuth-adatforrás) olyan nagy méretű, hogy a kétórás adatbetöltési korlátba ütközhet, a Power BI szolgáltatásban is adatbetöltési időtúllépést tapasztalhat.

Azt is érdemes figyelembe vennie, hogy az adatfrissítés megfelelő működéséhez a **SharePoint Online**-adatforrásokhoz AAD OAuth-hitelesítéssel való kapcsolódáskor ugyanazt a fiókot kell használnia, amelyet a **Power BI szolgáltatásba** való bejelentkezéshez is használ.

## <a name="uncompressed-data-limits-for-refresh"></a>Az adatfrissítés tömörítetlen adatokra vonatkozó korlátai
A **Power BI szolgáltatásba** importált adatkészletek maximális mérete 1 GB. Az ilyen adatkészletek a nagy teljesítmény biztosítása érdekében nagymértékben tömörítve vannak. Emellett megosztott használat esetén a szolgáltatás a frissítés során feldolgozott adatok mennyiségét 10 GB-ban maximálja. Ez a korlát figyelembe veszi a tömörítést, ezért sokkal magasabb, mint 1 GB. A Power BI Premium szolgáltatásban használt adatkészletekre ez a korlát nem vonatkozik. Ha a Power BI szolgáltatásban a frissítés ebből az okból hiúsul meg, csökkentse a Power BI-ba importált adatok mennyiségét, majd próbálkozzon újra.

## <a name="scheduled-refresh-timeout"></a>Ütemezett frissítés időtúllépése
Az importált adatkészletek frissítése két óra után időtúllépési hibát ad. Az ilyen időtúllépések határa a **Premium** munkaterületeken lévő adatkészletek esetében öt órára nő. Ha eléri ezt a korlátot, érdemes fontolóra vennie az adatkészlet méretének vagy összetettségének csökkentését, vagy érdemes feldarabolni kisebb tömbökre.

## <a name="next-steps"></a>További lépések
[Adatfrissítés](refresh-data.md)  
[A helyszíni adatátjáróval kapcsolatos hibák elhárítása](service-gateway-onprem-tshoot.md)  
[A személyes Power BI Gateway hibáinak elhárítása](service-admin-troubleshooting-power-bi-personal-gateway.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

