---
title: A Power BI felügyelete – gyakori kérdések (GYIK)
description: Ismerje meg a Power BI-előfizetéssel, bérlőkezeléssel és más adminisztratív feladatokkal kapcsolatos gyakori kérdésekre adott válaszokat.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 11/28/2017
ms.author: mblythe
LocalizationGroup: Administration
ms.openlocfilehash: 60ac0a944b1eb54ab998fbf25cb5fb79d6dddbe6
ms.sourcegitcommit: 833cf1252807721fb1b3000487bd032bfd6c8c98
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/04/2018
ms.locfileid: "48271900"
---
# <a name="administering-power-bi---frequently-asked-questions-faq"></a>A Power BI felügyelete – gyakori kérdések (GYIK)

A cikk a Power BI felügyeletével kapcsolatos gyakori kérdéseket ismerteti. A Power BI felügyeletének áttekintését a [Mi a Power BI-felügyelet?](service-admin-administering-power-bi-in-your-organization.md) című cikkben találja meg.

## <a name="whats-in-this-article"></a>A cikk tartalma
**Regisztráció a Power BI-ra**

* [Hogyan regisztrálnak a felhasználók a Power BI-ra?](#how-do-users-sign-up-for-power-bi)
* [Hogyan regisztrálnak a cég egyéni felhasználói?](#how-do-individual-users-in-my-organization-sign-up)
* [Hogyan gátolható meg, hogy a felhasználók csatlakozzanak a meglévő Office 365-bérlőhöz?](#how-can-i-prevent-users-from-joining-my-existing-office-365-tenant)
* [Hogyan engedélyezhető, hogy a felhasználók csatlakozzanak a meglévő Office 365-bérlőhöz?](#how-can-i-allow-users-to-join-my-existing-office-365-tenant)
* [Hogyan ellenőrizhető, hogy blokkoltam-e a bérlőt?](#how-do-i-verify-if-i-have-the-block-on-in-the-tenant)
* [Hogyan gátolható meg, hogy a meglévő felhasználók elkezdjék használni a Power BI-t?](#how-can-i-prevent-my-existing-users-from-starting-to-use-power-bi)
* [Hogyan engedélyezhető, hogy a meglévő felhasználók regisztráljanak a Power BI-ra?](#how-can-i-allow-my-existing-users-to-sign-up-for-power-bi)

**A Power BI felügyelete**

* [Hogyan változtatja meg a Power BI használata a felhasználók identitásának kezelését a cégen belül?](#how-will-this-change-the-way-i-manage-identities-for-users-in-my-organization-today)
* [Hogyan lehet kezelni a Power BI-t?](#how-do-we-manage-power-bi)
* [Mi a Microsoft által a felhasználók számára létrehozott bérlők kezelésének folyamata?](#what-is-the-process-to-manage-a-tenant-created-by-Microsoft-for-my-users)
* [Ha több tartományom van, felügyelhetem azt az Office 365-bérlőt, amelyhez a felhasználók hozzáadódnak?](#if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-are-added-to)
* [Hogyan távolítható el a Power BI a már regisztrált felhasználóktól?](#how-do-i-remove-power-bi-for-users-that-already-signed-up)
* [Honnan szerzek arról tudomást, ha új felhasználók csatlakoztak a bérlőhöz?](#how-do-i-know-when-new-users-have-joined-my-tenant)
* [Van még bármi egyéb, amire fel kell készülnöm?](#are-there-any-additional-things-i-should-be-prepared-for)
* [Hol található a Power BI-bérlőm?](#where-is-my-power-bi-tenant-located)
* [A Power BI SLA (szolgáltatásiszint-szerződés)](#what-is-the-power-bi-sla)

**Biztonság a Power BI-ban**

* [Eleget tesz a Power BI az országos, regionális, illetve iparágra jellemző megfelelőségi követelményeknek?](#does-power-bi-meet-national-regional-and-industry-specific-compliance-requirements)
* [Hogyan működik a biztonság a Power BI-ban?](#how-does-security-work-in-power-bi)

## <a name="sign-up-for-power-bi"></a>Regisztráció a Power BI-ra
### <a name="how-do-users-sign-up-for-power-bi"></a>Hogyan regisztrálnak a felhasználók a Power BI-ra?
A Power BI használatára a [Power BI webhelyén](https://powerbi.microsoft.com), illetve az Office 365 Felügyeleti központ szolgáltatások megvásárlására szolgáló oldalán is regisztrálhat. Amikor egy rendszergazda regisztrál a Power BI-ra, felhasználói licenceket rendelhet azokhoz a felhasználókhoz, akiknek hozzáférésre van szükségük.

A cég egyes felhasználói külön-külön is regisztrálhatnak a [Power BI webhelyen](https://powerbi.microsoft.com) a Power BI-ra. Amikor a vállalat egy felhasználója regisztrál a Power BI-ra, a felhasználóhoz automatikusan Power BI-licenc lesz rendelve. [További információ](service-self-service-signup-for-power-bi.md)

### <a name="how-do-individual-users-in-my-organization-sign-up"></a>Hogyan regisztrálnak a cég egyéni felhasználói?
Három forgatókönyv vonatkozhat a cégen belüli felhasználókra:

1. forgatókönyv: A cég már rendelkezik egy meglévő Office 365-környezettel, és a Power BI-ra regisztráló felhasználónak már van Office 365-fiókja.
Ha ebben a forgatókönyvben egy felhasználó már rendelkezik a bérlőn (például contoso.com) munkahelyi vagy iskolai fiókkal, de még nincs Power BI-fiókja, a Microsoft egyszerűen aktiválja a csomagot a fiókhoz, és a felhasználó automatikusan értesítést kap a Power BI szolgáltatás használatának módjáról.

2. forgatókönyv: A cég már rendelkezik egy meglévő Office 365-környezettel, de a Power BI-ra regisztráló felhasználónak nincs Office 365-fiókja.
Ebben a forgatókönyvben a felhasználónak van egy, a vállalati tartományba eső e-mail-címe (például contoso.com), de még nincs Office 365-fiókja. Ebben az esetben a felhasználó regisztrálhat a Power BI-ra, és automatikusan kap egy fiókot, így hozzáférhet a Power BI szolgáltatáshoz. Ha például egy Nancy nevű alkalmazott a munkahelyi e-mail-címét (például Nancy@contoso.com) használja a regisztráláshoz, a Microsoft automatikusan hozzáadja Nancyt felhasználóként a Contoso Office 365-környezetéhez, és aktiválja a Power BI-t ehhez a fiókhoz.

3. forgatókönyv: A vállalatban nincs az e-mail-tartományhoz csatlakoztatott Office 365-környezet.
A vállalatnak nem kell adminisztratív műveleteket elvégeznie a Power BI használatához. A felhasználók egy új, csak felhőalapú felhasználói címtárba kerülnek, és Ön felvállalhatja a bérlő rendszergazdai szerepkörét, hogy kezelni tudja őket.

> [!IMPORTANT]
> Ha a cég több e-mail-tartománnyal rendelkezik, és azt szeretné, hogy az összes e-mail-cím bővítmény ugyanabban a bérlőben legyen, adja az e-mail-címek összes tartományát egy Azure Active Directory-bérlőhöz, mielőtt bármelyik felhasználó regisztrálna. Nem áll rendelkezésre automatikus mechanizmus a felhasználók bérlők közötti mozgatásához, miután létrejöttek. A folyamatról további információt a cikk későbbi, [Ha több tartományom van, felügyelhetem azt az Office 365 bérlőt, amelyhez a felhasználók kerülnek?](#if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-are-added-to) című szakaszában és online, a [Tartomány és felhasználók hozzáadása az Office 365-höz](https://support.office.com/article/Add-your-users-and-domain-to-Office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611) című cikkben talál.
> 
> 

### <a name="how-can-i-prevent-users-from-joining-my-existing-office-365-tenant"></a>Hogyan gátolható meg, hogy a felhasználók csatlakozzanak a meglévő Office 365-bérlőhöz?
Rendszergazdaként tehet olyan lépéseket, amelyek meggátolják, hogy a felhasználók csatlakozzanak a meglévő Office 365-bérlőhöz. Ha blokkolja ezt a lehetőséget, a regisztrációs kísérletek meghiúsulnak, és a cég rendszergazdájával való kapcsolatfelvételhez vezetnek. Nem kell megismételnie ezt a folyamatot, ha már letiltotta az automatikus licencterjesztést (például az Office 365 for Education for Students, Faculty és Staff esetén).

Ezek a lépések a Windows PowerShell használatát igénylik. A Windows PowerShell használatának megkezdéséhez lásd a [PowerShell használatának első lépéseit ismertető útmutatót](http://go.microsoft.com/fwlink/p/?LinkID=286814).

A következő lépések elvégzése érdekében telepítenie kell a [Windows PowerShellhez készült Azure Active Directory-modul](http://go.microsoft.com/fwlink/p/?LinkID=236297) 64 bites verzióját.

Miután a hivatkozásra kattint, válassza a **Futtatás** parancsot a telepítőcsomag futtatásához.

**Automatikus bérlőhöz csatlakozás letiltása**: Ezzel a Windows PowerShell-paranccsal gátolhatja meg, hogy az új felhasználók a felügyelt bérlőhöz csatlakozzanak:

* Új felhasználók automatikus bérlőhöz csatlakozásának megakadályozása:
  
    $msolcred = get-credential   connect-msolservice -credential $msolcred
  
    Set-MsolCompanySettings -AllowEmailVerifiedUsers $false
* Új felhasználók automatikus bérlőhöz csatlakozásának engedélyezése:
  
    $msolcred = get-credential   connect-msolservice -credential $msolcred
  
    Set-MsolCompanySettings -AllowEmailVerifiedUsers $true

> [!NOTE]
> Ez a blokkolás meggátolja, hogy a cég lévő új felhasználói regisztráljanak a Power BI-ra. Azon felhasználók licence, akik a vállalat új regisztrációinak letiltása előtt regisztráltak a Power BI-ra, továbbra is megmarad. A [Hogyan távolíthatók el a licencek?] szakaszban talál útmutatást ahhoz, hogyan távolíthatja el a Power BI hozzáférését azon felhasználók esetén, akik korábban regisztráltak a szolgáltatásra.
> 
> 

### <a name="how-can-i-allow-users-to-join-my-existing-office-365-tenant"></a>Hogyan engedélyezhető, hogy a felhasználók csatlakozzanak a meglévő Office 365-bérlőhöz?
Ha engedélyezni szeretné, hogy a felhasználók csatlakozzanak a bérlőhöz, futtassa a fenti kérdésben ismertetett második parancsot.

A következő lépések elvégzése érdekében telepítenie kell a [Windows PowerShellhez készült Azure Active Directory-modul](http://go.microsoft.com/fwlink/p/?LinkID=236297) 64 bites verzióját.

    $msolcred = get-credential
    connect-msolservice -credential $msolcred

    Set-MsolCompanySettings -AllowEmailVerifiedUsers $true

### <a name="how-do-i-verify-if-i-have-the-block-on-in-the-tenant"></a>Hogyan ellenőrizhető, hogy blokkoltam-e a bérlőt?
Használja a következő PowerShell-szkriptet.

A következő lépések elvégzése érdekében telepítenie kell a [Windows PowerShellhez készült Azure Active Directory-modul](http://go.microsoft.com/fwlink/p/?LinkID=236297) 64 bites verzióját.

    $msolcred = get-credential
    connect-msolservice -credential $msolcred

    Get-MsolCompanyInformation | fl allow*

### <a name="how-can-i-prevent-my-existing-users-from-starting-to-use-power-bi"></a>Hogyan gátolható meg, hogy a meglévő felhasználók elkezdjék használni a Power BI-t?
Rendszergazdaként tehet olyan lépéseket, amelyek meggátolják, hogy a felhasználók regisztráljanak a Power BI-ra. Ha blokkolja ezt a lehetőséget, a regisztrációs kísérletek meghiúsulnak, és a cég rendszergazdájával való kapcsolatfelvételhez vezetnek. Nem kell megismételnie ezt a folyamatot, ha már letiltotta az automatikus licencterjesztést (például az Office 365 for Education for Students, Faculty és Staff esetén). [További információ](service-admin-licensing-organization.md#enable-or-disable-individual-user-sign-up-in-azure-active-directory)

A jelen **AllowAdHocSubscriptions** paramétert vezérlő AAD-beállítás. A legtöbb bérlő esetén ez a beállítás igaz értékre van állítva, vagyis engedélyezett. Ha a Power BI-t egy partneren keresztül szerezte be, elképzelhető, hogy ez alapértelmezés szerint hamis értékű, vagyis le van tiltva.

A következő lépések elvégzése érdekében telepítenie kell a [Windows PowerShellhez készült Azure Active Directory-modul](http://go.microsoft.com/fwlink/p/?LinkID=236297) 64 bites verzióját.

1. Először be kell jelentkeznie az Azure Active Directoryba az Office 365 hitelesítő adataival. Az első sor bekéri a hitelesítő adatokat. A második sor csatlakozik az Azure Active Directoryhoz.
   
     $msolcred = get-credential   connect-msolservice -credential $msolcred
2. Miután bejelentkezett, a következő parancs kiadásával láthatja, hogy jelenleg mihez van konfigurálva a bérlő.
   
     Get-MsolCompanyInformation | fl AllowAdHocSubscriptions
3. Ezzel a paranccsal engedélyezheti ($true) vagy letilthatja ($false) az AllowAdHocSubscriptions paramétert.
   
     Set-MsolCompanySettings -AllowAdHocSubscriptions $true

> [!NOTE]
> Az AllowAdHocSubscriptions jelzővel irányítható a vállalat számos felhasználói képessége, beleértve a felhasználók azon képességét, hogy regisztráljanak az Azure Rights Management szolgáltatásra. A jelző módosítása hatással van az összes képességre.
> 
> 

### <a name="how-can-i-allow-my-existing-users-to-sign-up-for-power-bi"></a>Hogyan engedélyezhető, hogy a meglévő felhasználók regisztráljanak a Power BI-ra?
Ha engedélyezni szeretné, hogy a meglévő felhasználók regisztráljanak a Power BI-ra, futtassa a fenti kérdésben szereplő parancsot, de false (hamis) helyett true (igaz) értékkel

A következő lépések elvégzése érdekében telepítenie kell a [Windows PowerShellhez készült Azure Active Directory-modul](http://go.microsoft.com/fwlink/p/?LinkID=236297) 64 bites verzióját.

1. Először be kell jelentkeznie az Azure Active Directoryba az Office 365 hitelesítő adataival. Az első sor bekéri a hitelesítő adatokat. A második sor csatlakozik az Azure Active Directoryhoz.
   
     $msolcred = get-credential   connect-msolservice -credential $msolcred
2. Miután bejelentkezett, a következő parancs kiadásával láthatja, hogy jelenleg mihez van konfigurálva a bérlő.
   
     Get-MsolCompanyInformation | fl AllowAdHocSubscriptions
3. Ezzel a paranccsal engedélyezheti ($true) vagy letilthatja ($false) az AllowAdHocSubscriptions paramétert.
   
     Set-MsolCompanySettings -AllowAdHocSubscriptions $true

> [!NOTE]
> Az AllowAdHocSubscriptions jelzővel irányítható a vállalat számos felhasználói képessége, beleértve a felhasználók azon képességét, hogy regisztráljanak az Azure Rights Management szolgáltatásra. A jelző módosítása hatással van az összes képességre.
> 
> 

## <a name="administration-of-power-bi"></a>A Power BI felügyelete
### <a name="how-will-this-change-the-way-i-manage-identities-for-users-in-my-organization-today"></a>Hogyan változtatja meg a Power BI használata a felhasználók identitásának kezelését a cégen belül?
Ha a vállalata már rendelkezik egy meglévő Office 365 környezettel, és a vállalatában lévő összes felhasználó rendelkezik Office 365-fiókkal, az identitáskezelés nem változik.

Ha a vállalata már rendelkezik egy meglévő Office 365 környezettel, de a vállalatában nem minden felhasználó rendelkezik Office 365-fiókkal, létrehozunk egy felhasználót a bérlőben, és licenceket rendelünk hozzá a felhasználó munkája, vagy iskolája, e-mail-címe alapján. Ez azt jelenti, hogy az Ön által bármely adott időpontban felügyelt felhasználók száma növekszik, ahogy a vállalatában lévő felhasználók regisztrálnak a szolgáltatásra.

Ha a vállalatában nincs az e-mail-tartományhoz Office 365 környezet csatlakoztatva, nem változik az identitáskezelés módja. A felhasználók egy új, csak felhőalapú felhasználói címtárba kerülnek, és Ön felvállalhatja a bérlő rendszergazdai szerepkörét, hogy kezelni tudja őket.

### <a name="how-do-we-manage-power-bi"></a>Hogyan lehet kezelni a Power BI-t?
A Power BI olyan rendszergazdai portált biztosít, amellyel megtekintheti a használattal kapcsolatos statisztikákat, kapcsolatot nyújt az Office 365 felügyeleti központhoz a felhasználók és csoportok kezeléséhez, illetve lehető teszi a bérlők közötti beállítások kezelését. 

> [!NOTE]
> A fiókját **Globális rendszergazda** fiókként kell megjelölni az Office 365 vagy az Azure Active Directory szolgáltatáson belül, vagy a Power BI szolgáltatás rendszergazdai szerepkörét kell hozzárendelni, hogy hozzá tudjon férni a Power BI felügyeleti portáljához. A Power BI szolgáltatás rendszergazdai szerepkörére vonatkozó további információkat [a Power BI rendszergazdai szerepkörét ismertető](service-admin-role.md) témakör tartalmaz.
> 
> 

További információkat a [Power BI felügyeleti portálon](service-admin-portal.md) talál.

### <a name="what-is-the-process-to-manage-a-tenant-created-by-microsoft-for-my-users"></a>Mi a Microsoft által a felhasználók számára létrehozott bérlők kezelésének folyamata?
Ha egy bérlőt a Microsoft hozott létre, a következő lépésekkel igényelheti és kezelheti a bérlőt:

1. A Power BI-ra való regisztrációval csatlakozzon a bérlőhöz, a kezelni kívánt bérlőtartománynak megfelelő e-mail-címtartománnyal. Ha a Microsoft például a contoso.com bérlőt hozta létre, a következő utótaggal rendelkező e-mail-címmel kell a bérlőhöz csatlakoznia: @contoso.com.
2. Igényeljen rendszergazdai irányítást a tartomány tulajdonosának ellenőrzésével: miután a bérlőbe került, a tartomány tulajdonosának ellenőrzésével *Globális rendszergazda* szerepbe léptetheti elő magát. Ehhez kövesse az alábbi lépéseket:
   
   1. Látogasson el a [https://portal.office.com](https://portal.office.com) címre.
   2. Kattintson az alkalmazás indítóikonjára a bal felső sarokban, és válassza a **Rendszergazda** elemet.
   3. Olvassa el a **Váljon rendszergazdává** oldalon lévő utasításokat, majd válassza az **Igen, rendszergazda szeretnék lenni** lehetőséget.
      
      > [!NOTE]
      > Ha ez a lehetőség nem jelenik meg, már van egy Office 365 rendszergazda.
      > 
      > 

### <a name="if-i-have-multiple-domains-can-i-control-the-office-365-tenant-that-users-are-added-to"></a>Ha több tartományom van, felügyelhetem azt az Office 365-bérlőt, amelyhez a felhasználók hozzáadódnak?
Ha nem tesz semmit, minden egyes felhasználói e-mail-tartományhoz és -altartományhoz létrejön egy-egy bérlő.

Ha azt szeretné, hogy az e-mail-cím bővítményétől függetlenül mindegyik felhasználó ugyanabban a bérlőben legyen:

* Előre hozzon létre egy célbérlőt, vagy használjon egy meglévő bérlőt, és adja hozzá a bérlőben konszolidálni kívánt összes meglévő tartományt és altartományt. Ekkor az ezekre a tartományokra vagy altartományokra végződő e-mail-címekkel rendelkező összes felhasználó automatikusan csatlakozik a célbérlőhöz a regisztráláskor.

> [!IMPORTANT]
> Nincs támogatott automatikus mechanizmus a felhasználók bérlők közötti mozgatásához, miután létrejöttek. A tartományok egyetlen Office 365-bérlőhöz való hozzáadásáról a [felhasználók és tartományok Office 365 szolgáltatáshoz adásával](https://support.office.com/article/Add-your-users-and-domain-to-Office-365-6383f56d-3d09-4dcb-9b41-b5f5a5efd611) kapcsolatos témakörben olvashat.
> 
> 

### <a name="how-do-i-remove-power-bi-for-users-that-already-signed-up"></a>Hogyan távolítható el a Power BI a már regisztrált felhasználóktól?
Ha egy felhasználó regisztrált a Power BI-ra, de Ön már nem szeretné, hogy hozzáférjen a Power BI-hoz, eltávolíthatja a felhasználó Power BI-licencét.

1. Keresse fel az Office 365 felügyeleti központot.
2. A bal oldali navigációs sávban válassza a **Felhasználók** > **Aktív felhasználók** lehetőséget.
3. Keresse meg azt a felhasználót, akinek el szeretné távolítani a licencét, majd válassza a név > **Szerkesztés** lehetőséget.
4. A részletek oldalon válassza a bal oldali navigációs sávban lévő **Licencek** lehetőséget.
5. Törölje a **Power BI (ingyenes)** vagy a **Power BI Pro** jelölőnégyzetet attól függően, hogy milyen licenc van alkalmazva a fiókra.
6. Kattintson a **Mentés** gombra.

> [!NOTE]
> A felhasználók kötegelt licenckezelését is elvégezheti. Ehhez válasszon ki több felhasználót, és válassza a **Szerkesztés** lehetőséget.
> 
> 

### <a name="how-do-i-know-when-new-users-have-joined-my-tenant"></a>Honnan szerzek arról tudomást, ha új felhasználók csatlakoztak a bérlőhöz?
A jelen program részeként a bérlőhöz csatlakozó felhasználókhoz egyedi licenc van rendelve, amely alapján szűrhet a felügyeleti irányítópult aktív felhasználó panelén.

Ezen új nézet létrehozásához az Office 365 felügyeleti központban lépjen a **Felhasználók** > **Aktív felhasználók** területre, és a **Nézet kiválasztása** menüben válassza az **Új nézet** lehetőséget. Nevezze el az új nézetet, és a **Hozzárendelt licenc** területen válassza a **Power BI (ingyenes)** vagy a **Power BI Pro** lehetőséget. Egy nézethez csak egy licencet választhat ki. Ha **Power BI (ingyenes)** és **Power BI Pro** licencek is vannak a vállalatában, két nézetet kell létrehoznia. Az új nézet létrehozása után láthatja a bérlőben lévő összes olyan felhasználót, aki regisztrált erre a programra.

### <a name="are-there-any-additional-things-i-should-be-prepared-for"></a>Van még bármi egyéb, amire fel kell készülnöm?
Az új jelszavak létrehozásával kapcsolatos kérések növekedését tapasztalhatja. További információk erről a folyamatról: [Új jelszó kérése egy felhasználóhoz](https://support.office.com/article/Reset-a-users-password-7a5d073b-7fae-4aa5-8f96-9ecd041aba9c).

A szokásos eljárással távolíthat el felhasználókat a bérlőből az Office 365 felügyeleti központban. Ha azonban egy felhasználónak még mindig a vállalattól származó e-mail-címe van, újra tud csatlakozni, amíg le nem tiltja az összes felhasználó csatlakozását.

### <a name="where-is-my-power-bi-tenant-located"></a>Hol található a Power BI-bérlőm?
A Power BI-bérlő (másnéven az adatrégió) helyének megismeréséhez tekintse meg a [Hol található a Power BI-bérlőm?](service-admin-where-is-my-tenant-located.md) témakört.

### <a name="what-is-the-power-bi-sla"></a>Mi az a Power BI SLA?
A Power BI SLA-ról (szolgáltatásiszint-szerződésről) további információt a Microsoft licencelést bemutató webhelyének **Licencelés** szakaszában található [Licencelési feltételek és dokumentáció](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37) című témakörben talál.

## <a name="security-in-power-bi"></a>Biztonság a Power BI-ban
### <a name="does-power-bi-meet-national-regional-and-industry-specific-compliance-requirements"></a>Eleget tesz a Power BI az országos, regionális, illetve iparágra jellemző megfelelőségi követelményeknek?
A Power BI megfelelésével kapcsolatban további információért látogasson el a [Microsoft biztonsági és adatkezelési központba](http://go.microsoft.com/fwlink/?LinkId=785324).

### <a name="how-does-security-work-in-power-bi"></a>Hogyan működik a biztonság a Power BI-ban?
A Power BI az Office 365 alapjára épül, amely viszont Azure-szolgáltatásokon, például az Azure Active Directoryn alapul. A Power BI-architektúra áttekintését a [Power BI biztonságával](service-admin-power-bi-security.md) kapcsolatos témakörben találja. 

## <a name="next-steps"></a>Következő lépések
[Power BI felügyeleti portál](service-admin-portal.md)  
[A Power BI rendszergazdai szerep ismertetése](service-admin-role.md)  
[Önkiszolgáló regisztráció a Power BI-ra](service-self-service-signup-for-power-bi.md)  
[A Power BI Pro megvásárlása](service-admin-purchasing-power-bi-pro.md)  
[Power BI Premium – pontosan mi is ez?](service-premium.md)  
[A Power BI Premium megvásárlása](service-admin-premium-purchase.md)  
[Office 365 felhasználói fiókok kezelése](https://technet.microsoft.com/library/office-365-user-account-management.aspx)  
[Office 365 csoportfelügyelet](https://support.office.com/Article/Find-help-about-Groups-in-Office-365-7a9b321f-b76a-4d53-b98b-a2b0b7946de1)  
[Csoportok kezelése a Power BI és az Office 365 szolgáltatásban](service-manage-app-workspace-in-power-bi-and-office-365.md)  
[Power BI Premium-tanulmány](https://aka.ms/pbipremiumwhitepaper)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)