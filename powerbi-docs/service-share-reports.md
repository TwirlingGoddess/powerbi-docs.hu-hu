---
title: "Power BI-jelentések megosztása munkatársakkal"
description: "Tudnivalók arról, hogyan oszthat meg munkatársaival Power BI-jelentéseket vagy szűrt jelentéseket a cégen belül."
services: powerbi
documentationcenter: 
author: maggiesMSFT
manager: kfile
backup: ajayan
editor: 
tags: 
featuredvideoid: 0tUwn8DHo3s
qualityfocus: complete
qualitydate: 06/22/2016
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 11/14/2017
ms.author: maggies
ms.openlocfilehash: 022f085d12d7dc872052ca9205deca264b1c0418
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="share-power-bi-reports-with-your-coworkers"></a>Power BI-jelentések megosztása munkatársakkal
A *Megosztással* egyszerűen biztosíthatja néhány személy hozzáférését az irányítópultjaihoz és jelentéseihez. A Power BI-ban [többféle módon valósítható meg a jelentések közös használata és terjesztése](service-how-to-collaborate-distribute-dashboards-reports.md), amelyek közül a megosztás csak az egyik lehetőség.

A megosztáshoz Önnek és az összes címzetteknek is [Power BI Pro-licencre](service-free-vs-pro.md) van szüksége, vagy pedig a tartalomnak kell egy [Prémium-kapacitásban](service-premium.md) lennie. Javaslatai vannak? A Power BI csapata mindig érdeklődve fogadja visszajelzését, amelyet a [Power BI-közösség webhelyén](https://community.powerbi.com/) küldhet el.

A Saját munkaterületéről vagy egy alkalmazás munkaterületéről azokkal a munkatársaival oszthat meg jelentéseket, akik ugyanazt az e-mail-címtartomány használják, mint Ön. A megosztott jelentés címzettjei használhatják, de nem szerkeszthetik a jelentést. Az adatokat ugyanúgy látják, ahogyan Ön is látja a jelentésben, hacsak nem alkalmaz [sorszintű biztonságot (RLS-t)](service-admin-rls.md). 

## <a name="share-a-power-bi-report"></a>Power BI-jelentés megosztása
1. A Power BI szolgáltatásban [hozzon létre egy irányítópultot](service-dashboard-create.md) legalább egy olyan csempével, amely a megosztani kívánt jelentésre hivatkozik. 
   
    Ha csak a jelentést szeretné megosztani, akkor is előbb létre kell hoznia és meg kell osztania egy olyan irányítópultot, amely a jelentésre hivatkozik. 

1. A jobb felső sarokban válassza a **Megosztás** lehetőséget.

     ![Megosztás választása](media/service-share-reports/power-bi-share-upper-right.png)
  
2. Adja meg a címzettek e-mail-címeit. Ha nem szeretne e-mail-értesítést küldeni nekik az irányítópultról, akkor távolítsa el a pipát az **E-mail értesítés küldése a címzetteknek** jelölőnégyzetből.

     ![Az E-mail-értesítés küldése a címzetteknek jelölőnégyzet törlése](media/service-share-reports/power-bi-share-dont-send-mail.png)

4. Válassza a **Megosztás** gombot.

      Ekkor azok, akikkel az irányítópultot megosztotta, megkapják az engedélyt az irányítópult alapjául szolgáló jelentés megtekintésére. 

1. Nyissa meg a jelentést a Power BI szolgáltatásban, másolja a jelentésoldal URL-címét, majd küldje el munkatársainak. 
   
    Amikor kiválasztják a hivatkozást, a Power BI egy írásvédett verzióban nyitja meg a jelentést.

## <a name="share-a-filtered-version-of-a-report"></a>Jelentés szűrt verziójának megosztása
Mi történik olyankor, ha egy jelentésnek egy szűrt verzióját szeretné megosztani? Például egy olyan jelentést, amely csak egy adott város, év vagy értékesítő adatait jeleníti meg. Ezt egy egyedi URL-cím létrehozásával teheti meg.

1. Nyissa meg a jelentést [Szerkesztő nézetben](service-reading-view-and-editing-view.md), alkalmazza a szűrőt, majd mentse a jelentést.
   
   Ebben a példában a [Kiskereskedelmi elemzési mintát](sample-tutorial-connect-to-the-samples.md) szűrjük, hogy csak azokat az értékeket mutassa, ahol a **Territory** (Terület) **NC** (Észak-Karolnia) értékű.
   
   ![Jelentés Szűrés ablaktáblája](media/service-share-reports/power-bi-filter-report2.png)
2. Adja hozzá a jelentésoldal URL-címéhez a következőt:
   
   ?filter=*táblanév*/*mezőnév* eq *érték*
   
    A mező **sztring** típusú kell hogy legyen, és sem a *táblanév*, sem pedig a *mezőnév* nem tartalmazhat szóközöket.
   
   A példánkban **Store** (Üzlet) a tábla neve, **Territory** (Terület) a mező neve, és **NC** (Észak-Karolnia) az érték, amelyre szűrni szeretnénk:
   
    ?filter=Store/Territory eq NC
   
   ![Szűrt jelentés URL-címe](media/service-share-reports/power-bi-filter-url3.png)
   
   A böngésző ehhez még hozzáad néhány speciális karaktert a szóközök és a perjelek helyettesítésére, így az eredmény a következő lesz:
   
   app.powerbi.com/groups/me/reports/010ae9ad-a9ab-4904-a7a1-10a61f70f2f5/ReportSection2?filter=Store%252FTerritory%20eq%20NC
3. Küldje el az URL-címet munkatársainak. 
   
   Amikor kiválasztják a hivatkozást, a Power BI egy írásvédett verzióban nyitja meg a szűrt jelentést.

## <a name="next-steps"></a>Következő lépések
* Visszajelzés küldene? Mondja el javaslatait a [Power BI-közösség webhelyén](https://community.powerbi.com/).
* [Irányítópultok és jelentések közös használata és megosztása](service-how-to-collaborate-distribute-dashboards-reports.md)
* [Irányítópult megosztása](service-share-dashboards.md)
* További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/).

