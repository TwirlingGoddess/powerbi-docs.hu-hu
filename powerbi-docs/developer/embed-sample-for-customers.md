---
title: Power BI tartalom beágyazása egy alkalmazásba az ügyfelek számára
description: 'Útmutató: hogyan integrálhat vagy ágyazhat be jelentést, irányítópultot vagy csempét ügyfelei számára egy webalkalmazásba a Power BI API-kkal.'
services: powerbi
author: markingmyname
ms.author: maghan
ms.date: 05/07/2018
ms.topic: tutorial
ms.service: powerbi
ms.custom: mvc
manager: kfile
ms.openlocfilehash: 2d4fdee8d3e4cca60294acd0a9167da1f048afa5
ms.sourcegitcommit: 9fa954608e78dcdb8d8a503c3c9b01c43ca728ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/11/2018
ms.locfileid: "34051933"
---
# <a name="tutorial-embed-a-power-bi-report-dashboard-or-tile-into-an-application-for-your-customers"></a>Oktatóanyag: Power BI-jelentés, -irányítópult vagy -csempe beágyazása egy alkalmazásba a saját ügyfelek részére
Az **Azure-beli Power BI Embedded** segítségével jelentéseket, irányítópultokat és csempéket ágyazhat be az alkalmazásokba, így lehetővé teheti ügyfeleinek az adatmegosztást. Ez egy jellegzetes **független szoftverszállítói fejlesztői** feladat, amely az **adatok az alkalmazáshoz tartoznak** szerkezeten alapul. Az **adatok az alkalmazáshoz tartoznak** szerkezetből következik, hogy a Power BI-tartalmat be kell ágyazni az ügyfelek részére. Így a Power BI-tartalom felhasználója például a **Power BI-ba** való bejelentkezés nélkül is megtekintheti a jelentéseket, az irányítópultokat és a csempéket. Ez az oktatóanyag bemutatja, hogyan integrálhat vagy ágyazhat be egy jelentést az ügyfelei által használt alkalmazásokba a **Power BI** .NET SDK és a **Power BI** JavaScript API segítségével, az **adatok az alkalmazáshoz tartoznak** elven, az **Azure-beli Power BI Embedded** használatával.

Az oktatóanyag a következőket ismerteti:
>[!div class="checklist"]
>* Alkalmazás regisztrálása az Azure-ban.
>* Jelentés, irányítópult vagy csempe beágyazása az alkalmazásba az Azure-beli Power BI Embedded használatával.

## <a name="prerequisites"></a>Előfeltételek
A kezdéshez szüksége van egy **Power BI Pro**- és egy **Microsoft Azure**-fiókra.

* Ha még nem regisztrált a **Power BI Pro** szolgáltatásra, a kezdés előtt [hozzon létre egy ingyenes próbaverziós fiókot](https://powerbi.microsoft.com/en-us/pricing/).
* Ha még nincs Azure-előfizetése, kezdés előtt hozzon létre egy [ingyenes fiókot](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* Állítson be egy saját [Azure Active Directory-bérlőt](create-an-azure-active-directory-tenant.md).
* Telepítse a [Visual Studio](https://www.visualstudio.com/) 2013-as vagy későbbi verzióját.

## <a name="setup-your-embedded-analytics-development-environment"></a>A beágyazott elemzési fejlesztési környezet beállítása

Mielőtt jelentéseket, irányítópultokat és csempéket ágyazna be az alkalmazásba, győződjön meg arról, hogy a környezete be van állítva a beágyazás engedélyezéséhez. A beállítás részeként a következőket kell elvégeznie.

### <a name="register-an-application-in-azure-active-directory-azure-ad"></a>Alkalmazás regisztrálása az Azure Active Directoryban (Azure AD)

Az alkalmazás Azure Active Directoryban történő regisztrálása lehetővé teszi az alkalmazás számára a Power BI REST API-k elérését. Így identitást hozhat létre az alkalmazás számára, és meghatározhatja a Power BI REST-erőforrásokhoz való engedélyeket.

1. Fogadja el a [Microsoft Power BI API használati feltételeit](https://powerbi.microsoft.com/api-terms).

2. Jelentkezzen be az [Azure Portalon](https://portal.azure.com).
 
    ![Az Azure Portal főoldala](media/embed-sample-for-customers/embed-sample-for-customers-002.png)

3. A bal oldali navigációs ablakban válassza ki az **Összes szolgáltatás** lehetőséget, és kattintson az **Alkalmazásregisztráció**, majd az **Új alkalmazás regisztrálása** elemre.
   
    ![Alkalmazásregisztráció keresése](media/embed-sample-for-customers/embed-sample-for-customers-003.png)</br>
    ![Új alkalmazás regisztrálása](media/embed-sample-for-customers/embed-sample-for-customers-004.png)

4. Kövesse az utasításokat az új alkalmazás létrehozásához. Az adatok az alkalmazáshoz tartoznak szerkezethez a **Natív** alkalmazástípust kell használnia. Adja meg azt az **Átirányítási URI-t**, amelyet az **Azure AD** a jogkivonatválaszok visszaadására használ. Adjon meg egy alkalmazáshoz tartozó értéket (például: http://localhost:13526/redirect)).

    ![Alkalmazás létrehozása](media/embed-sample-for-customers/embed-sample-for-customers-005.png)

### <a name="apply-permissions-to-your-application-within-azure-active-directory"></a>Engedélyek alkalmazása a saját alkalmazásra az Azure AD-ben

Az alkalmazás részére további engedélyeket is meg kell adnia az alkalmazásregisztrációs oldalon már megadottakon felül. Jelentkezzen be a beágyazáshoz használt *fő* fiókkal, amelynek globális rendszergazdafióknak kell lennie.

### <a name="use-the-azure-active-directory-portal"></a>Az Azure Active Directory portál használata

1. Az Azure Portal [Alkalmazásregisztrációk](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ApplicationsListBlade) szakaszában keresse meg azt az alkalmazást, amelyet a beágyazáshoz kíván használni.
   
    ![Az alkalmazás kiválasztása](media/embed-sample-for-customers/embed-sample-for-customers-006.png)

2. Kattintson a **Beállítások** elemre, majd az **API-hozzáférés** területen válassza az **Szükséges engedélyek** lehetőséget.
   
    ![Szükséges engedélyek](media/embed-sample-for-customers/embed-sample-for-customers-008.png)

3. Válassza a **Windows Azure Active Directory** elemet, majd győződjön meg arról, hogy a **Hozzáférés a címtárhoz a bejelentkezett felhasználóként** beállítás be van jelölve. Kattintson a **Mentés** gombra.
   
    ![Windows Azure AD-engedélyek](media/embed-sample-for-customers/embed-sample-for-customers-011.png)

4. Válassza a **Hozzáadás** elemet.

    ![Engedélyek hozzáadása](media/embed-sample-for-customers/embed-sample-for-customers-012.png)

5. Kattintson az **API kiválasztása** lehetőségre.

    ![API-hozzáférés hozzáadása](media/embed-sample-for-customers/embed-sample-for-customers-013.png)

6. Kattintson a **Power BI szolgáltatás**, majd a **Kiválasztás** lehetőségre.

    ![PBI szolgáltatás kiválasztása](media/embed-sample-for-customers/embed-sample-for-customers-014.png)

7. Jelölje be az összes engedélyt a **Delegált engedélyek** szakaszban. Ezeket egyenként kell kijelölnie, hogy menteni tudja a kijelöléseket. Ha végzett, kattintson a **Mentés** gombra.
   
    ![Delegált engedélyek kiválasztása](media/embed-sample-for-customers/embed-sample-for-customers-015.png)

8. A **Szükséges engedélyek** listában kattintson az **Engedélyek megadása** elemre.
   
    Az **Engedélyek megadása** műveletre azért van szükség, hogy a *fő fióknál* ne kelljen Azure AD-hozzájárulást kérni. Amennyiben globális rendszergazdai fiókkal végzi el a műveletet, a cég összes felhasználója megkapja az engedélyeket ehhez az alkalmazáshoz. Amennyiben a *fő fiókkal*, és nem a globális rendszergazdai fiókkal hajtja végre a műveletet, csak a *fő fiók* számára adja meg az engedélyeket ehhez az alkalmazáshoz.
   
    ![Engedélyek megadása a Szükséges engedélyek párbeszédpanelen](media/embed-sample-for-customers/embed-sample-for-customers-016.png)

### <a name="create-your-power-bi-embedded-dedicated-capacity-in-azure"></a>Power BI Embedded dedikált kapacitás létrehozása az Azure-ban

1. Jelentkezzen be az [Azure Portalon](https://portal.azure.com).

    ![Az Azure Portal főoldala](media/embed-sample-for-customers/embed-sample-for-customers-002.png)

2. A bal oldali navigációs ablaktáblán kattintson az **Összes szolgáltatás**, majd a **Power BI Embedded** lehetőségre.

    ![A PBIE megkeresése](media/embed-sample-for-customers/embed-sample-for-customers-017.png)

3. Kövesse az utasításokat, és adja meg a megfelelő információkat az új **Power BI Embedded** dedikált kapacitás létrehozásához, majd kattintson a **Létrehozás** lehetőségre. A **Tarifacsomag** kiválasztásánál az alábbi táblázatban tájékozódhat az igényeinek leginkább megfelelő csomagról. Ezt követően kattintson a **Létrehozás** elemre, és várja meg, amíg az erőforrás elkészül.

    ![A PBIE beállítása](media/embed-sample-for-customers/embed-sample-for-customers-018.png)

| Kapacitáscsomópont | Magok száma összesen<br/>*(Háttérrendszer + előtérrendszer)* | Háttérrendszerbeli magok | Előtérrendszerbeli magok | DirectQuery-/élő kapcsolat korlátai | Maximális oldalmegjelenítések óránként csúcsidőszakban |
| --- | --- | --- | --- | --- | --- |
| A1 |1 virtuális mag |0,5 mag, 3 GB RAM |0,5 mag | Másodpercenként 5 |1-300 |
| A2 |2 virtuális mag |1 mag, 5 GB RAM |1 mag | Másodpercenként 10 |301-600 |
| A3 |4 virtuális mag |2 mag, 10 GB RAM |2 mag | Másodpercenként 15 |601-1200 |
| A4 |8 virtuális mag |4 mag, 25 GB RAM |4 mag |Másodpercenként 30 |1,201-2,400 |
| A5 |16 virtuális mag |8 mag, 50 GB RAM |8 mag |Másodpercenként 60 |2,401-4,800 |
| A6 |32 virtuális mag |16 mag, 100 GB RAM |16 mag |Másodpercenként 120 |4801-9600 |

Most már megtekintheti az új **Power BI Embedded dedikált kapacitást**.

   ![PBIE dedikált kapacitás](media/embed-sample-for-customers/embed-sample-for-customers-019.png)

## <a name="setup-your-power-bi-environment"></a>A Power BI-környezet beállítása

### <a name="create-an-app-workspace"></a>Alkalmazás munkaterületének létrehozása

Amikor beágyazza a jelentéseket, irányítópultokat vagy csempéket az ügyfelei számára, akkor egy alkalmazás-munkaterületen kell elhelyeznie a tartalmakat. A *fő* fióknak az alkalmazás-munkaterület rendszergazdai fiókjának kell lennie.

1. Kezdjük a munkaterület létrehozásával. Kattintson a **munkaterületek** > **Alkalmazás-munkaterületek létrehozása** lehetőségre. A tartalmat itt kell elhelyeznie, hogy elérhető legyen az alkalmazás számára.

    ![Munkaterület létrehozása](media/embed-sample-for-customers/embed-sample-for-customers-020.png)

2. Nevezze el a munkaterületet. Ha a megfelelő **munkaterület-azonosító** nem használható, szerkesztéssel hozzon létre egy egyedi azonosítót. Ez lesz az alkalmazás neve is.

    ![Munkaterület elnevezése](media/embed-sample-for-customers/embed-sample-for-customers-021.png)

3. Néhány beállítást meg kell adnia. Ha **nyilvánosra** állítja a munkaterületet, a szervezet bármely tagja megtekintheti annak tartalmát. A **Privát** beállítás ezzel szemben azt jelenti, hogy a munkaterület tartalmát csak a tagok láthatják.

    ![Privát/Nyilvános](media/embed-sample-for-customers/embed-sample-for-customers-022.png)

    A Nyilvános/Privát beállítás a csoport létrehozását követően nem módosítható.

4. Azt is beállíthatja, hogy a tagok **szerkeszthetik-e** a tartalmakat vagy **csak megtekintési** jogosultságuk van.

    ![Tagok felvétele](media/embed-sample-for-customers/embed-sample-for-customers-023.png)

5. Vegye fel az adott személyek e-mail-címét, akiknek hozzáférést kíván adni a munkaterülethez, majd kattintson a **Hozzáadás** gombra. Csoportaliasokat nem adhat hozzá, csak egyéneket.

6. Döntse le, hogy az egyes személyek egyszerű tagok vagy adminisztrátorok legyenek-e. Az adminisztrátorok szerkeszthetik magát a munkaterületet is, és tagokat is felvehetnek. A tagok a munkaterület tartalmát szerkeszthetik, amennyiben nem csak megtekintési jogosultsággal rendelkeznek. Az alkalmazást az adminisztrátorok és a tagok egyaránt közzétehetik.

7. Bontsa ki a **Speciális** elemet, engedélyezze a **Dedikált kapacitást**, majd kattintson a létrehozott **Power BI Embedded dedikált kapacitásra**. Kattintson a **Mentés** gombra.

    ![Tagok felvétele](media/embed-sample-for-customers/embed-sample-for-customers-024.png)

Most megtekintheti az új munkaterületet. A Power BI létrehozza és megnyitja a munkaterületet. Ekkor megjelenik az olyan munkaterületek listájában, amelyeknek Ön a tagja. Mivel adminisztrátori jogosultsággal rendelkezik, a három pontra (...) kattintva visszaléphet, és szerkesztheti a munkaterületet, például új tagokat adhat hozzá vagy módosíthatja a tagok jogosultságait.

   ![Új munkaterület](media/embed-sample-for-customers/embed-sample-for-customers-025.png)

### <a name="create-and-publish-your-reports"></a>Saját jelentések létrehozása és közzététele

A Power BI Desktop segítségével létrehozhatja jelentéseit és adatkészleteit, majd közzéteheti ezeket a jelentéseket egy alkalmazás-munkaterületen. A jelentéseket közzétevő végfelhasználónak Power BI Pro-licencre van szüksége az alkalmazás-munkaterületen történő közzétételhez.

1. Töltse le a [Blog Demo](https://github.com/Microsoft/powerbi-desktop-samples) mintát a GitHubról.

    ![jelentésminta](media/embed-sample-for-customers/embed-sample-for-customers-026-1.png)

2. PBIX-mintajelentés megnyitása a **Power BI Desktopban**

   ![PBI desktop jelentés](media/embed-sample-for-customers/embed-sample-for-customers-027.png)

3. Közzététel az **alkalmazás-munkaterületen**

   ![PBI desktop jelentés](media/embed-sample-for-customers/embed-sample-for-customers-028.png)

    A jelentést mostantól online megtekintheti a Power BI szolgáltatásban

   ![PBI desktop jelentés](media/embed-sample-for-customers/embed-sample-for-customers-029.png)

## <a name="embed-your-content"></a>Tartalom beágyazása

1. A kezdéshez töltse le az [App Owns Data mintát](https://github.com/Microsoft/PowerBI-Developer-Samples) a GitHubról.

    ![App Owns Data alkalmazásminta](media/embed-sample-for-customers/embed-sample-for-customers-026.png)

2. Nyissa meg a Web.config fájlt ugyanebben az alkalmazásban. Az alkalmazás sikeres futtatásához 5 mezőt kell kitöltenie. Az **ügyfél-azonosító**, a **csoportazonosító**, a **jelentésazonosító**, a **pbiUsername** (PBI-felhasználónév) és a **pbiPassword** (PBI-jelszó) mezőket.

      ![Web Config fájl](media/embed-sample-for-customers/embed-sample-for-customers-030.png)

    * Az **ügyfél-azonosító** mezőbe az **Azure-beli** **Alkalmazásazonosítót** kell beírni. Az alkalmazás az **ügyfél-azonosítóval** azonosítja magát azon felhasználók esetén, akiktől Ön engedélyeket kér. Az **ügyfél-azonosítót** a következőképpen olvashatja be:

        1. Jelentkezzen be az [Azure Portalon](https://portal.azure.com).

        ![Az Azure Portal főoldala](media/embed-sample-for-customers/embed-sample-for-customers-002.png)

        2. A bal oldali navigációs ablaktáblán válassza az **Összes szolgáltatást**, és kattintson az **Alkalmazásregisztrációk** lehetőségre.

        ![Alkalmazásregisztráció keresése](media/embed-sample-for-customers/embed-sample-for-customers-003.png)
        3. Válassza ki azt az alkalmazást, amelynek az **ügyfél-azonosítóját** be kívánja olvasni.

        ![Az alkalmazás kiválasztása](media/embed-sample-for-customers/embed-sample-for-customers-006.png)

      4. Megjelenik egy GUID-ként listázott **alkalmazásazonosító**. Használja ezt az **alkalmazásazonosítót** az alkalmazás **ügyfél-azonosítójaként**.

        ![ügyfél-azonosító](media/embed-sample-for-customers/embed-sample-for-customers-007.png)     

    * A **csoportazonosító** mezőbe írja be a Power BI-ban szereplő **alkalmazás-munkaterület GUID-azonosítóját**.

        ![csoportazonosító](media/embed-sample-for-customers/embed-sample-for-customers-031.png)

    * A **jelentésazonosító** mezőbe írja be a Power BI-ban szereplő **jelentés GUID-azonosítóját**.

        ![jelentésazonosító](media/embed-sample-for-customers/embed-sample-for-customers-032.png)    

    * A **pbiUsername** mezőbe írja be a főfelhasználói Power BI-fiókot.
    * A **pbiPassword** mezőbe írja be a főfelhasználói Power BI-fiók jelszavát.

3. Futtassa az alkalmazást!

    Először is kattintson a **Futtatás** elemre a **Visual Studióban**.

    ![Alkalmazás futtatása](media/embed-sample-for-customers/embed-sample-for-customers-033.png)

    Kattintson a **Jelentés beágyazása** lehetőségre. Válassza ki az alkalmazásban a jelentést, az irányítópultot vagy a csempét annak megfelelően, hogy melyiket szeretné kipróbálni.

    ![Tartalom kiválasztása](media/embed-sample-for-customers/embed-sample-for-customers-034.png)
 
    Most megtekintheti a jelentést a mintaalkalmazásban.

    ![Alkalmazás megtekintése](media/embed-sample-for-customers/embed-sample-for-customers-035.png)

A JavaScript API teljes körű mintáját a [Playground eszköz](https://microsoft.github.io/PowerBI-JavaScript/demo) segítségével használhatja. Ez az eszköz lehetőséget ad a Power BI Embedded különböző mintáinak gyors kipróbálására. A JavaScript API-ról a [PowerBI-JavaScript wiki](https://github.com/Microsoft/powerbi-javascript/wiki) oldalon talál további információkat.

A Power BI Embedded használatáról a [Gyakori kérdések](embedded-faq.md) oldalon tájékozódhat.  Ha az alkalmazáson belül hibát észlel a Power BI Embedded használata során, látogassa meg a [hibaelhárítás](embedded-troubleshoot.md) oldalt.

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/) 