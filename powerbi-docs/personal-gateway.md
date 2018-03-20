---
title: "Személyes Power BI-átjáró"
description: "Személyes Power BI-átjáró"
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
ms.date: 12/06/2017
ms.author: davidi
LocalizationGroup: Gateways
ms.openlocfilehash: 7a523284bd777d87b7ac42ba7e9ff82ee7bdf623
ms.sourcegitcommit: 4217430c3419046c3a90819c34f133ec7905b6e7
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/12/2018
---
# <a name="power-bi-gateway---personal"></a>Személyes Power BI-átjáró
> [!NOTE]
> A Power BI privát átjárójának van egy új verziója, melynek neve **helyszíni adatátjáró (privát mód)**. A következő cikk a privát átjáró korábbi verzióját, a **Power BI Gateway - Personalt** ismerteti, amely 2017. július 31-ével elavult, és nem használható tovább. A privát átjáró új verziójával kapcsolatos információkat, beleértve az új verzió telepítésének menetét, a [**helyszíni adatátjárót (privát mód)** ismertető cikkben](service-gateway-personal-mode.md) találhatja.
> 
> 

A **Power BI Gateway - Personal** hídként működik, amely gyors és biztonságos adatátvitelt biztosít a Power BI szolgáltatás és a [frissítést](refresh-data.md) támogató helyszíni adatforrások között. Ebben a cikkben közelebbről is megismerheti, hogyan működik az átjáró, és hogy Önnek szüksége van-e rá. A privát átjárókkal kapcsolatban egy [tájékoztató videót](https://www.youtube.com/watch?v=de58vROLqZI) is összeállítottunk. 

Az átjáró szolgáltatásként települ és fut a számítógépen. Szolgáltatásként a konfiguráció során megadott Windows-fiókkal fut, de néhány esetben alkalmazásként működik. Ezt később tárgyaljuk részletesebben.

Amikor a Power BI helyszíni adatforrásról frissít adatokat, az átjáró biztosítja, hogy a Power BI-fiókja megfelelő engedélyekkel rendelkezzen ahhoz, hogy csatlakozhasson a forráshoz, és adatokat kérdezhessen le róla.

A Power BI és az átjáró közötti adatátvitel [Azure Service Buson](http://azure.microsoft.com/documentation/services/service-bus/) keresztül történik. A Service Bus biztonságos csatornát hoz létre a Power BI szolgáltatás és a számítógép között. Mivel az átjáró biztosítja ezt a biztonságos kapcsolatot, általában nem kell portot nyitni a tűzfalon.

Mielőtt belemennénk az átjáróra vonatkozó ismeretek részleteibe, nézzünk meg a Power BI-ban használt néhány kifejezést:

Az *adatkészlet* a Power BI szolgáltatásba online vagy helyszíni adatforrásból betöltött adatokat jelenti. Akkor hoz létre adatkészletet, amikor a Lekérdezés elemmel csatlakozik és tölt fel adatokat. Az adatkészletek a böngésző Power BI-munkaterületének Saját munkaterület paneljén jelennek meg. Amikor jelentéseket hoz létre és csempéket rögzít az irányítópultokon, az adatkészletekből származó adatokat lát.

Az *adatforrásokból* származnak az adatkészletbe feltöltött adatok. Ezek bármik lehetnek; adatbázisok, Excel-táblázatok, webszolgáltatások stb. Az Excel-munkafüzetekkel egyszerű, adatsorokkal rendelkező munkalapokat hozhat létre, és ez is adatforrásnak minősül. Az Excelben a Power Query vagy a Power Pivot használatával is csatlakozhat és kérhet le adatokat online és helyszíni adatforrásokból is, mindezt egyetlen munkafüzeten belül. A Power BI Desktopban a Lekérdezés paranccsal online és helyszíni adatforrásokból származó adatokhoz is csatlakozhat, és mindkét típusú adatot lekérheti.

A privát átjáró helyszíni adatátjárón keresztül van telepítve, és a [Power BI Gateway oldalán](https://powerbi.microsoft.com/gateway/) töltheti le.

## <a name="do-i-need-a-gateway"></a>Szükségem van átjáróra?
Mielőtt nekilátna egy átjáró telepítésének, fontos megállapítani, hogy egyáltalán szüksége van-e rá. Ez leginkább az adatforrásoktól függ:

### <a name="on-premises-data-sources"></a>Helyszíni adatforrások
Privát átjáróra *van szükség* olyan adatkészletek frissítéséhez, amelyek egy, a vállalaton belüli, támogatott helyszíni adatforrásokból szereznek adatokat.

Az átjáróknál a REFRESH NOW (azonnali frissítés) és a SCHEDULE REFRESH (ütemezett frissítés) a következőkből feltöltött adatkészletek esetén támogatott:

* Microsoft Excel 2013-as (vagy újabb) munkafüzetek, amelyek Power Query vagy Power Pivot használatával csatlakoznak és kérnek le adatokat egy támogatott helyszíni adatforrásból. A Power Query vagy a Power Pivot Külső adatok beolvasása területén látható összes helyszíni adatforrás támogatja a frissítést, a Hadoop-fájl (HDFS) és a Microsoft Exchange kivételével.
* Microsoft Power BI Desktop-fájlok, amelyek a Lekérdezés használatával csatlakoznak és kérnek le adatokat támogatott helyszíni adatforrásokból. A Lekérdezés területen látható összes helyszíni adatforrás támogatja a frissítést, a Hadoop-fájl (HDFS) és a Microsoft Exchange kivételével.

### <a name="online-data-sources"></a>Online adatforrások
*Csak akkor van szükség* átjáróra, ha a [**Web.Page**](https://msdn.microsoft.com/library/mt260924.aspx) függvényt használja. Más esetben *nincs* szükség átjáróra olyan adatkészletek frissítéséhez, amelyek csak online adatforrásból szereznek be adatokat.

> [!NOTE]
> Ha a [**Web.Page**](https://msdn.microsoft.com/library/mt260924.aspx) függvényt használja, csak akkor van szüksége átjáróra, ha újból közzétette az adatkészletet vagy a jelentést 2016. november 18. után.
> 
> 

Átjáró nélkül a REFRESH NOW (azonnali frissítés) és a SCHEDULE REFRESH (ütemezett frissítés) a következőkből feltöltött adatkészletek esetén támogatott:

* Online adatforrásokból származó tartalomcsomagok (tartalomcsomagok\\szolgáltatások). Alapértelmezés szerint a tartalomcsomagokból származó adatkészletek naponta egyszer automatikusan frissülnek, de manuálisan is frissíthet, vagy frissítési ütemezést is beállíthat.
* Microsoft Excel 2013-as (vagy újabb) munkafüzetek, amelyek Power Query vagy Power Pivot használatával csatlakoznak és kérnek le adatokat egy online adatforrásból.
* Microsoft Power BI Desktop-fájlok, amelyek a Lekérdezés használatával csatlakoznak és kérnek le adatokat online adatforrásokból.

**Kérdés:** Mit tegyek, ha az Excel-munkafüzet vagy a Power BI Desktop-fájl online és helyszíni adatforrásokból is szerez be adatokat?

**Válasz:** *Szükség van* egy átjáróra. Telepítenie és konfigurálnia kell egy átjárót a helyszíni adatforrásokból lekérdezett adatok frissítéséhez.

**Kérdés:** Mit tegyek, ha az Excel-munkafüzetben csak általam beírt adatsorok vannak?**

**Válasz:** *Nincs* szükség átjáróra. Csak akkor kell átjárót telepítenie és konfigurálnia, ha a munkafüzet Power Query vagy Power Pivot használatával kérdez le és tölt be adatokat az adatmodellbe egy támogatott helyszíni adatforrásból.

## <a name="setting-up-a-gateway-for-the-first-time"></a>Átjáró első beállítása
Az átjáró első beállítása egy három lépésből álló folyamat:

1. Az átjáró letöltése és telepítése
2. Az átjáró konfigurálása
3. Bejelentkezés az adatforrásokba a Power BI-ban

Lássuk mindegyik lépést közelebbről.

### <a name="download-and-install-a-gateway"></a>Az átjáró letöltése és telepítése
> [!NOTE]
> A Power BI privát átjárójának van egy új verziója, melynek neve **helyszíni adatátjáró (privát mód)**. Ez a cikk a privát átjáró korábbi verzióját, a **Power BI Gateway - Personalt** ismerteti, amely 2017. július 31-ével elavult, és nem használható tovább. A privát átjáró új verziójával kapcsolatos információkat, beleértve az új verzió telepítésének menetét, a [**helyszíni adatátjárót (privát mód)** ismertető cikkben](service-gateway-personal-mode.md) találhatja.
> 
> 

A rendszer felszólítja egy átjáró telepítésére, amikor először a FRISSÍTÉS MOST vagy a FRISSÍTÉS ÜTEMEZÉSE gombra kattint egy támogatott adatkészletnél. Azt is megteheti, hogy az átjáró letöltéséhez kiválasztja a Letöltések menü **Adatátjáró** menüpontját. Töltse le a [helyszíni adatátjárót](http://go.microsoft.com/fwlink/?LinkID=820925).

Érdemes **privát átjárót** használni a **helyszíni adatátjáró** helyett, hogy saját átjárója legyen.

Az átjáró telepítése nem bonyolult folyamat. Ki kell választania a telepítés helyét, és el kell olvasnia és fogadnia a licencszerződést, mint minden már alkalmazás esetén. Van azonban néhány fontos dolog, amit érdemes tudni, különösen azt, hogy milyen típusú számítógépre telepíti az átjárót, és milyen típusú fiókkal van bejelentkezve a Windowsba a számítógépen.

> [!NOTE]
> Az átjárónak képesnek kell lennie rá, hogy elérje az adatforrást. Ha a saját gépe nem tud csatlakozni az adatforráshoz, érdemes lehet [helyszíni adatátjárót](service-gateway-onprem.md) telepíteni egy olyan gépre, amely hozzáfér. Ez lehet például az Azure-ban üzemeltetett virtuális gépre (VM) telepített SQL Server. Előfordulhat, hogy a saját gépe nem fér hozzá a virtuális géphez. Megteheti, hogy telepíti a helyszíni adatátjárót a virtuális gépre, és konfigurálja az adatforrást a Power BI szolgáltatásban.
> 
> 

### <a name="computer-type"></a>A számítógép típusa
Figyelembe kell venni, hogy milyen típusú számítógépre telepíti az átjárót.

> [!NOTE]
> A privát átjárók csak 64 bites Windows operációs rendszereken támogatottak.
> 
> 

Ha laptopot használ, azt is szem előtt kell tartani, hogy az ütemezett frissítéshez az átjárónak üzemelnie kell. A laptopok általában többször vannak kikapcsolva vagy alvó állapotban, mint amennyit futnak. Ha laptopon telepíti az átjárót, olyan időpontokra állítsa az ütemezett frissítéseket, amikor a laptop éppen működik. Ha nem fut, a rendszer nem kísérli meg ismét a frissítést a következő ütemezett frissítésig.

Asztali számítógépen túl sok problémával nem kell számolni. Csak ellenőrizze, hogy a számítógép és az átjáró fut-e az ütemezett frissítési időpontokban. Sok asztali számítógép úgy van beállítva, hogy alvó állapotba lépjen, és ebben az állapotban az ütemezett frissítésre nem kerül sor.

Egy átjáró telepítése után nem kell másikat telepítenie. Egy átjáró bármennyi támogatott adatkészlethez használható. Arra a számítógépre sem kell telepítenie az átjárót, amelyről feltölti a munkafüzetet és a Power BI Desktop-fájlokat. Lássunk egy példát. Tegyük fel, hogy olyan Excel-munkafüzete van, amely egy SQL Server-adatforráshoz csatlakozik a cégen belül. A Power BI Lekérdezés funkciójával töltötte fel a munkafüzetet a laptopjáról. Egy állandóan futó asztali számítógépe is van, amelyen telepített és konfigurált egy átjárót. A Power BI-ban bejelentkezett az adatforrásokba, és beállított egy frissítési ütemezést az adatkészlethez.  Amikor eljön egy ütemezett frissítés ideje, a Power BI biztonságos kapcsolatot létesít az asztali számítógépre telepített átjáróval. Ezután biztonságos módon csatlakozik az adatforrásokhoz a frissítések lekérése érdekében. A frissítés során a rendszer nem folytat kommunikációt a laptopról feltöltött eredeti munkafüzettel.

> [!NOTE]
> A privát és a vállalati átjárókat ugyanarra a számítógépre is telepítheti.
> 
> 

### <a name="windows-account"></a>Windows-fiók
Az átjáró telepítésekor a Windows-fiókjával jelentkezik be a számítógépre. A Windows-fiók engedélyeinek típusa hatással lesz arra, hogyan települ az átjáró, és hogyan fut a Windowsban.

A Windowsba történő bejelentkezés módja:

|  | Rendszergazdai engedélyekkel | Rendszergazdai engedélyek nélkül |
| --- | --- | --- |
| **A Power BI Gateway - Personal a következőként fut:** |Szolgáltatás |Alkalmazás |
| **Ütemezett frissítés** |Amíg a számítógép és az átjárószolgáltatás fut, nem kell bejelentkezve lennie az ütemezett frissítéskor. |Az ütemezett frissítéskor bejelentkezve kell lennie a számítógépre. |
| **Windows-fiók jelszavának módosítása** |Módosítania kell a jelszót az átjárószolgáltatásban. Ha az átjáró által használt fiókjelszó már nem érvényes, a frissítés meghiúsul. |Az átjáró mindig azzal a fiókkal és jelszóval fut, amellyel jelenleg be van jelentkezve. Ha nincs bejelentkezve a Windowsba, az átjáró nem fut, és a frissítés meghiúsul. |

### <a name="configure-the-gateway"></a>Az átjáró konfigurálása
Amikor a Telepítő varázsló befejeződik, a rendszer felszólítja a Konfigurációs varázsló elindítására. Az átjáró konfigurálása sem okozhat túl sok nehézséget. Be kell jelentkeznie a Power BI-ba a varázslóból. Erre azért van szükség, hogy a varázsló kapcsolatot létesíthessen a Power BI-fiókjával a Power BI szolgáltatásban.

Ha rendszergazdai engedélyekkel van bejelentkezve a Windowsba, a rendszer felszólítja a Windows-fiók hitelesítő adatainak megadására. Megadhat egy másik Windows-fiókot, de ne feledje, hogy az engedélyek határozzák meg az átjáró futtatásának módját. Az átjárószolgáltatás a megadott fiókkal fog futni.

### <a name="sign-in-to-data-sources"></a>Bejelentkezés adatforrásokba
Miután a Konfigurációs varázsló befejeződött és az átjáró működik, meg kell adnia egy hitelesítési típust, és be kell jelentkeznie az adatkészlet mindegyik adatforrásába. Ezt a lépést a Power BI-ban kell végrehajtani.

![](media/personal-gateway/pg_dataset_settings_signin.png)

Csak egyszer kell megadnia egy hitelesítési típust, és egy adatforrásba csak egyszer kell bejelentkeznie. Az adatkészlet Beállítások képernyőjének **Adatforrások kezelése** szakaszában tud bejelentkezni. Ha több adatforrása van, mindegyikbe be kell jelentkeznie. Az átjáró az adatforrástól függően meghatároz egy alapértelmezett hitelesítési típust. A legtöbb esetben ez Windows-hitelesítés, néhány esetben azonban előfordulhat, hogy az adatforráshoz más hitelesítésre van szükség. Ha nem biztos benne, hogy melyiket kéne használni, forduljon az adatforrás rendszergazdájához.

## <a name="up-and-running"></a>Minden működik!
Amikor az átjáró működik, rákattinthat a FRISSÍTÉS ÜTEMEZÉSE gombra az adatkészlet Beállítások panelén.

![](media/personal-gateway/pg_awintsales_settings.png)

Ez az oldal a következőket tartalmazza:

1. Frissítés állapota – A frissítés sikerét és a következő ütemezett frissítés idejét jeleníti meg.
2. **Átjáró** – Megjeleníti, hogy egy átjáró telepítve és online állapotban van-e. Ha egy átjáró telepítve van, de nincs online állapotban, az Adatforrások kezelése és a Frissítés ütemezése beállítások le vannak tiltva.
3. **Adatforrások kezelése** – Azokat az adatforrásokat jeleníti meg, amelyekhez az adatkészlet csatlakozik. Bejelentkezhet vagy módosíthatja a hitelesítés típusát. Egy adatforrásba csak egyszer kell bejelentkeznie.
4. **Frissítés ütemezése** – Itt konfigurálhatja a frissítések ütemezésének beállításait. Ha az átjáró nincs online, ezek a beállítások le vannak tiltva.
5. Frissítési hibaértesítések – Ez az alapértelmezés szerint kiválasztott beállítás e-mailt küld, ha egy ütemezett frissítés meghiúsul.

## <a name="updating-your-windows-account-password"></a>A Windows-fiók jelszavának frissítése
Ha rendszergazdai jogosultságokkal rendelkező Windows-fiókkal jelentkezett be egy számítógépre az átjáró telepítésekor, az szolgáltatásként fog futni a Konfigurációs varázslóban megadott Windows-fiókkal. Ez általában ugyanaz a Windows-fiók, amellyel a számítógépre bejelentkezik. Amikor módosítja a Windows-fiók jelszavát, az átjáróban is módosítania kell, különben előfordulhat, hogy a szolgáltatás nem fut, és a frissítés meghiúsul. Ha módosítani szeretné az átjáró Windows-fiókjelszavát, válassza ki a privát átjáró ikonját a Windows asztali tálcán vagy az Alkalmazások területen.

![](media/personal-gateway/pg_programicon.png)

Innen frissítheti a jelszót, és ellenőrizheti az átjáró kapcsolati állapotát.

![](media/personal-gateway/pg_credentials.png)

## <a name="ports"></a>Portok
Az átjáró a következő kimenő portokon kommunikál: TCP 443 (alapméretezett), 5671, 5672, 9350–9354.  Az átjáró nem igényel bejövő portokat.

| Tartománynevek | Kimenő portok | Leírás |
| --- | --- | --- |
| *.powerbi.com |443 |HTTPS |
| *.analysis.windows.net |443 |HTTPS |
| *.login.windows.net |443 |HTTPS |
| *.servicebus.windows.net |5671-5672 |Advanced Message Queueing Protocol (AMQP) |
| *.servicebus.windows.net |443, 9350-9354 |A Service Bus Relay figyelői a TCP-n (443-as portot igényel a hozzáférés-vezérlési token beszerzéséhez) |
| *.frontend.clouddatahub.net |443 |HTTPS |
| *.core.windows.net |443 |HTTPS |
| login.microsoftonline.com |443 |HTTPS |
| login.windows.net |443 |HTTPS |

Ha IP-címeket kell engedélyeznie a tartományok helyett, letöltheti és használhatja a Microsoft Azure Adatközpont IP-címtartományok listáját. [Letöltés](https://www.microsoft.com/download/details.aspx?id=41653)

## <a name="next-steps"></a>Következő lépések
[Helyszíni adatátjáró (privát mód) – a privát átjáró új verziója](service-gateway-personal-mode.md)
[Power BI-átjárók proxybeállításainak konfigurálása](service-gateway-proxy.md)  
[Power BI Premium](service-premium.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

