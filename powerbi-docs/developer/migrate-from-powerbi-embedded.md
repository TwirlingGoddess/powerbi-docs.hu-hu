---
title: "Power BI Embedded munkaterület-csoport tartalmainak migrálása a Power BI-ba"
description: "Itt elsajátíthatja, hogyan migrálhatja az adatokat a Power BI Embeddedből a Power BI szolgáltatásba, és hogyan aknázhatja ki az alkalmazásokba való beágyazás nyújtotta fejlett lehetőségeket."
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
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 07/21/2017
ms.author: asaxton
ms.openlocfilehash: 430f1d1a49e510bac66c448b2dceaad1f2537073
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="how-to-migrate-power-bi-embedded-workspace-collection-content-to-power-bi"></a>Power BI Embedded munkaterület-csoport tartalmainak migrálása a Power BI-ba
Itt elsajátíthatja, hogyan migrálhatja az adatokat a Power BI Embeddedből a Power BI szolgáltatásba, és hogyan aknázhatja ki az alkalmazásokba való beágyazás nyújtotta fejlett lehetőségeket.

A Microsoft nemrégiben [bejelentette az új kapacitásalapú Power BI Premium licencelési modellt](https://powerbi.microsoft.com/blog/microsoft-accelerates-modern-bi-adoption-with-power-bi-premium/), amelynek segítségével a felhasználók rugalmasabban érhetik el, oszthatják meg és terjeszthetik a tartalmakat. Az ajánlat emellett növeli a Power BI szolgáltatás méretezhetőségét és teljesítményét.

A Power BI Premium bevezetésével a Power BI Embedded és a Power BI szolgáltatás egyre közelebb kerül egymáshoz, ezáltal is megkönnyítve a Power BI tartalmak beágyazását az alkalmazásokba. Ez azt jelenti, hogy a tartalmak (például irányítópultok, átjárók és alkalmazás-munkaterületek) beágyazásához egyetlen egységes API-felület, konzisztens funkciókészlet és a Power BI legújabb szolgáltatásai használhatók. A jövőben a Power BI Desktoppal létrehozott telepítések áthelyezhetőek lesznek majd a Power BI Premium üzemi környezetébe, amely 2017 második negyedévének végén lesz majd elérhető.

A jelenlegi Power BI Embedded szolgáltatás az egybevont szolgáltatás általános kiadását követően korlátozott ideig továbbra is elérhető lesz: a Nagyvállalati Szerződéssel rendelkező ügyfelek a fennálló szerződésük lejártáig továbbra is használhatják, a Power BI Embedded megoldást a közvetlenül vagy CSP csatornákon beszerző ügyfelek pedig a Power BI Premium általános kiadásától számított egy évig használhatják.  A cikk útmutatást ad az Azure szolgáltatásról a Power BI szolgáltatásra való átálláshoz, valamint tájékoztatást nyújt az alkalmazás várható változásairól.

> [!IMPORTANT]
> Bár a migrálás függőséget jelent a Power BI szolgáltatástól, az alkalmazást használó ügyfelekre **beágyazási token** használata esetén nem vonatkozik függőség. Nem kell bejelentkezniük a Power BI szolgáltatásba a beágyazott tartalmak megtekintéséhez az alkalmazásban. Ezzel a beágyazási megközelítéssel kiszolgálhatja a nem Power BI-felhasználókat.
> 
> 

![](media/migrate-from-powerbi-embedded/powerbi-embed-flow.png)

## <a name="prepare-for-the-migration"></a>Előkészületek a migráláshoz
A Power BI Embedded Azure szolgáltatásból a Power BI szolgáltatásba való migrálásának előkészítéséhez néhány dolgot végre kell hajtania. Szükség lesz egy elérhető bérlőre, valamint egy Power BI Pro licenccel rendelkező felhasználóra.

1. Bizonyosodjon meg róla, hogy rendelkezésre áll egy Azure Active Directory (Azure AD) bérlő.
   
    Meg kell határoznia, hogy milyen bérlőbeállítást használ.
   
   * A meglévő vállalati Power BI-bérlőt használja?
   * Külön bérlőt használ az alkalmazáshoz?
   * Külön bérlőt használ mindegyik ügyfélhez?
     
     Ha új bérlőt hozna létre az alkalmazáshoz vagy egyenként az ügyfelekhez, tekintse meg az [Azure Active Directory-bérlő létrehozásával](create-an-azure-active-directory-tenant.md) vagy [Azure AD-bérlő beszerzésével](https://docs.microsoft.com/azure/active-directory/develop/active-directory-howto-tenant) kapcsolatos cikket.
2. Hozzon létre egy felhasználót ezen az új bérlőn, amely a alkalmazás „fő” fiókjaként fog szolgálni. A fióknak fel kell iratkoznia a Power BI-ra, és rendelkeznie kell egy Power BI Pro licenccel.

## <a name="accounts-within-azure-ad"></a>Az Azure AD-ben lévő fiókok
A következő fiókoknak létezniük kell a bérlőn.

> [!NOTE]
> Ezeknek a fiókoknak Power BI Pro licenccel kell rendelkezniük, hogy használhassák az alkalmazás-munkaterületet.
> 
> 

1. Egy bérlői rendszergazda felhasználó.
   
    Javasoljuk, hogy ez a felhasználó a beágyazás céljával létrehozott összes alkalmazás-munkaterület tagja legyen.
2. A tartalmat létrehozó elemzők fiókjai.
   
    Ezeket a felhasználókat igény szerint hozzá kell rendelni az alkalmazás-munkaterületekhez.
3. Az alkalmazás *fő* felhasználói vagy szolgáltatásfiókja.
   
    A fiók hitelesítő adatait az alkalmazások háttérrendszere tárolja majd és használja az Azure AD-token beszerzéséhez a Power BI API-k használatához. A rendszer ennek a fióknak a használatával hozza létre a beágyazási tokent az alkalmazáshoz. A fióknak a beágyazáshoz létrehozott alkalmazás-munkaterületeken is rendszergazdai jogosultsággal kell rendelkeznie.
   
   > [!NOTE]
   > Ez csak a szervezet egy normál felhasználói fiókja, amely beágyazási célokra lesz használva.
   > 
   > 

## <a name="app-registration-and-permissions"></a>Alkalmazásregisztráció és -engedélyek
Az alkalmazásokat regisztrálni kell az Azure AD-ben, és bizonyos engedélyeket kell biztosítani a számukra.

### <a name="register-an-application"></a>Egy alkalmazás regisztrálása
A REST API-hívások indításához az alkalmazásokat regisztrálni kell az Azure AD-ben. Ehhez be kell jelentkeznie az Azure Portalra, és további konfigurációs beállításokat kell tennie a Power BI alkalmazásregisztrációs oldalán megadottak mellett. További információkért lásd: [Azure AD alkalmazás regisztrálása Power BI-tartalmak beágyazásához](register-app.md).

Az alkalmazást annak **fő** fiókjával kell regisztrálni.

## <a name="create-app-workspaces-required"></a>Alkalmazás-munkaterületek létrehozása (kötelező)
Az alkalmazás-munkaterületek használatával nagyobb fokú elszigetelés érhető el, ha az alkalmazás több ügyfelet is kiszolgál. Az irányítópultok és a jelentések így ügyfelenként elkülöníthetőek. Ekkor alkalmazás-munkaterületenként külön Power BI-fiók használatával még jobban elszigetelheti az alkalmazásfelületeket az ügyfelek közt.

> [!IMPORTANT]
> Személyes munkaterületek használatával nem aknázhatja ki a nem Power BI-felhasználók számára való beágyazás kínálta előnyöket.
> 
> 

A Power BI alkalmazás-munkaterületek létrehozásához szükség van egy Pro licenccel rendelkező felhasználóra. Az alkalmazás-munkaterületet létrehozó Power BI-felhasználó alapértelmezés szerint az adott munkaterület rendszergazdájává válik.

> [!NOTE]
> Az alkalmazás *fő* fiókjának rendszergazdai jogosultsággal kell rendelkeznie a munkaterületen.
> 
> 

## <a name="content-migration"></a>Tartalommigrálás
A tartalmak migrálása a munkaterület-csoportokból a Power BI szolgáltatásba az aktuális megoldással párhuzamosan végezhető, így nem okoz állásidőt.

A **migrálási eszköz** szabadon használható a Power BI Embedded-tartalmak a Power BI szolgáltatásba másolásához. Ez különösen akkor hasznos, ha sok tartalommal rendelkezik. További információ: [Power BI Embedded migrálási eszköz](migrate-tool.md).

A tartalommigrálás leginkább két API-n keresztül történik.

1. Download PBIX: ez az API a Power BI-ba 2016 októbere után feltöltött PBIX-fájlok letöltéséhez használható.
2. Import PBIX: ez az API bármilyen PBIX-fájl a Power BI-ba való feltöltéséhez használható.

Néhány kapcsolódó kódrészletért lásd: [Tartalmak a Power BI Embeddedbe való migrálásához használható kódrészletek](migrate-code-snippets.md).

### <a name="report-types"></a>Jelentéstípusok
A jelentéseknek több típusa létezik, és mindegyikhez valamelyest eltérő migrálási folyamat szükséges.

#### <a name="cached-dataset--report"></a>Gyorsítótárazott adatkészlet és jelentés
Gyorsítótárazott adatkészletek alatt olyan PBIX-fájlokat értünk, amelyek élő vagy DirectQuery-kapcsolatok helyett importált adatokat tartalmaznak.

**Folyamat**

1. Hívja meg az Import PBIX API-t a PaaS-munkaterületről.
2. Mentse a PBIX-fájlt.
3. Hívja meg az Import PBIX API-t a SaaS-munkaterületre.

#### <a name="directquery-dataset--report"></a>DirectQuery-adatkészlet és -jelentés
**Folyamat**

1. Hívja meg a GET https://api.powerbi.com/v1.0/collections/{csoport_azonosítója}/workspaces/{munkaterület_azonosítója}/datasets/{adatkészlet_azonosítója}/Default.GetBoundGatewayDataSources metódust, és mentse a visszakapott kapcsolati karakterláncot.
2. Hívja meg az Import PBIX API-t a PaaS-munkaterületről.
3. Mentse a PBIX-fájlt.
4. Hívja meg az Import PBIX API-t a SaaS-munkaterületre.
5. A kapcsolati karakterlánc frissítéséhez hívja meg a következőt: POST  https://api.powerbi.com/v1.0/myorg/datasets/{adatkészlet_azonosítója}/Default.SetAllConnections
6. Az átjáró- és az adatforrás-azonosító lekéréséhez hívja meg a következőt: GET https://api.powerbi.com/v1.0/myorg/datasets/{adatkészlet_azonosítója}/Default.GetBoundGatewayDataSources
7. A felhasználói hitelesítő adatok frissítéséhez hívja meg a következőt: PATCH https://api.powerbi.com/v1.0/myorg/gateways/{átjáró_azonosítója}/datasources/{adatforrás_azonosítója}

#### <a name="old-dataset--reports"></a>Régi adatkészlet és jelentések
Ezek a 2016 októbere előtt létrehozott adatkészletek/jelentések. A PBIX-letöltés API nem támogatja a 2016 októbere előtt feltöltött PBIX-fájlokat

**Folyamat**

1. Töltse le a PBIX-fájlokat a fejlesztői környezetből (a belső forráskezelő környezetből).
2. Hívja meg az Import PBIX API-t a SaaS-munkaterületre.

#### <a name="push-dataset--report"></a>Leküldéses adatkészlet és jelentés
A PBIX-letöltés nem támogatja a *Push API* adatkészleteit. A Push API adatkészleteinek adatai nem portolhatóak PaaS-munkaterületekről SaaS-munkaterületekre.

**Folyamat**

1. Hívja meg a „Create dataset” (Adatkészlet létrehozása) API-t az adatkészlet JSON-fájljával az adatkészlet létrehozásához a SaaS-munkaterületen.
2. Állítsa újra össze a jelentést a létrehozott adatkészlethez*.

Bizonyos kerülő megoldásokkal lehetséges migrálni a Push API-val készített jelentéseket a PaaS- és a SaaS-munkaterületek közt. Ehhez próbálkozzon a következőkkel.

1. Töltsön fel néhány helyőrző PBIX-fájlt a PaaS-munkaterületre.
2. Klónozza a Push API-val készített jelentést, és kösse az 1. lépésben feltöltött helyőrző PBIX-fájlhoz.
3. Töltse le a Push API-val készített jelentést a helyőrző PBIX-fájllal.
4. Töltse fel a helyőrző PBIX-fájlt a SaaS-munkaterületre.
5. Hozza létre a leküldéses adatkészletet a SaaS-munkaterületen.
6. Kösse újra a jelentést a Push API-val készített adatkészlethez.

## <a name="create-and-upload-new-reports"></a>Új jelentések létrehozása és feltöltése
A Power BI Embedded Azure-szolgáltatásból migrált tartalmak mellett a Power BI Desktop használatával is létrehozhatja a jelentéseket és adatkészleteket, majd közzéteheti ezeket a jelentéseket egy alkalmazás-munkaterületen. A jelentéseket közzétevő végfelhasználónak Power BI Pro-licencre van szüksége az alkalmazás-munkaterületen történő közzétételhez.

## <a name="rebuild-your-application"></a>Az alkalmazás újrabuildelése
1. Power BI REST API-k használatához és a powerbi.com szolgáltatáson belüli jelentéshely megadásához módosítania kell az alkalmazást.
2. Buildelje újra az AuthN/AuthZ hitelesítést az alkalmazás *fő* fiókjának használatával. [Beágyazási token](https://msdn.microsoft.com/library/mt784614.aspx) használatával kiaknázhatja azt a lehetőséget, hogy ez a felhasználó a többi felhasználó nevében cselekedhet.
3. Ágyazza be a jelentéseket a powerbi.com helyről az alkalmazásba.

## <a name="map-your-users-to-a-power-bi-user"></a>A felhasználók leképezése Power BI-felhasználókra
Az alkalmazásban az abban kezelt felhasználókat leképezi egy, az alkalmazáshoz használható *fő* Power BI fiókra. A Power BI *fő* fiók hitelesítő adatait az alkalmazás tárolja, és beágyazási tokenek létrehozásához használja.

## <a name="what-to-do-when-you-are-ready-for-production"></a>Mi a teendő, ha készen áll az éles üzemeltetésre
Amikor kész átállni éles üzemre, a következőket kell tennie.

* Ha külön bérlőt használ a fejlesztéshez, gondoskodnia kell róla, hogy az alkalmazás-munkaterületek, valamint az irányítópultok és a jelentések elérhetők az éles környezetben. Arra is figyelnie kell, hogy az alkalmazást az Azure AD-ben az éles környezeti bérlőhöz hozza létre, és hozzárendelje a megfelelő alkalmazásjogosultságokat, amint azt az 1. lépés tárgyalja.
* Vásároljon az igényeinek megfelelő kapacitást. A követelmények megértéséhez segítséget találhat a következő szakaszban: [Kapacitástervezés a beágyazott elemzésekhez – tanulmány](https://aka.ms/pbiewhitepaper). Amikor készen áll a kapacitások megvásárlására, ezt az [Office 365 Felügyeleti központban](https://portal.office.com/adminportal/home#/catalog) teheti meg.
  
  > [AZURE.INFORMATION] A Power BI Premium beszerzésével kapcsolatos további információkért lásd: [A Power BI Premium beszerzése](../service-admin-premium-purchase.md).
  > 
  > 
* Az alkalmazás-munkaterületet a Speciális felületen módosíthatja és rendelheti hozzá a Premium kapacitásokhoz.
  
    ![](media/migrate-from-powerbi-embedded/powerbi-embedded-premium-capacity.png)
* Helyezze üzembe a frissített alkalmazást az éles környezetben, és kezdje beágyazni a jelentéseket a Power BI szolgáltatásból.

## <a name="after-migration"></a>A migrálás után
Takarítson az Azure-ban.

* Távolítsa el a telepített megoldás összes már nem használt munkaterületét a Power BI Embedded Azure-szolgáltatásában.
* Törölje az Azure-ból az összes munkaterület-csoportot.

## <a name="next-steps"></a>További lépések
[Beágyazás a Power BI-jal](embedding.md)  
[Power BI Embedded migrálási eszköz](migrate-tool.md)  
[Kódrészletek a tartalmak Power BI Embeddedből való migrálásához](migrate-code-snippets.md)  
[Power BI-irányítópultok, -jelentések és -csempék beágyazása](embedding-content.md)  
[Power BI Premium – pontosan mi is ez?](../service-premium.md)  
[JavaScript API Git-adattár](https://github.com/Microsoft/PowerBI-JavaScript)  
[Power BI C# Git-adattár](https://github.com/Microsoft/PowerBI-CSharp)  
[JavaScript beágyazási minta](https://microsoft.github.io/PowerBI-JavaScript/demo/)  
[Embedded elemzési kapacitásának tervezésével kapcsolatos tanulmány](https://aka.ms/pbiewhitepaper)  
[Power BI Premium-tanulmány](https://aka.ms/pbipremiumwhitepaper)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)
