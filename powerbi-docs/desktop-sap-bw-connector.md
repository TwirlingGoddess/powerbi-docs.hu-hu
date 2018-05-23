---
title: Az SAP BW Connector használata a Power BI Desktopban
description: Az SAP BW Connector használata a Power BI Desktopban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 04/09/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 79fcd556827c0c5c34615021e45e3abfadfd50e2
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
---
# <a name="use-the-sap-bw-connector-in-power-bi-desktop"></a>Az SAP BW Connector használata a Power BI Desktopban
A Power BI Desktopban hozzáférhet az **SAP Business Warehouse (BW)** adataihoz.

Ha szeretné megismerni, milyen előnyökkel jár, ha az ügyfelek a Power BI-t a meglévő SAP Business Warehouse (BW) rendszerükhöz csatlakoztatják, olvassa el a [Power BI-t és az SAP BW-t bemutató tanulmányt](https://aka.ms/powerbiandsapbw).

## <a name="installation-of-sap-bw-connector"></a>Az SAP BW Connector telepítése
Az **SAP BW Connector** használatához hajtsa végre az alábbi telepítési lépéseket:

1. Telepítse az **SAP NetWeaver** kódtárat a helyi számítógépen. Az **SAP Netweaver** kódtárat az SAP-rendszergazdától vagy közvetlenül az [SAP Software Download Center letöltőközpontból](https://support.sap.com/swdc) szerezheti be. Mivel az **SAP Software Download Center** szerkezete gyakran változik, a helyet nem tudjuk pontosabban meghatározni. Az **SAP NetWeaver** kódtárat általában az SAP Client Tools telepítése is tartalmazza.
   
   A legfrissebb verzió letöltései helyének megtalálásához érdemes rákeresnie a *SAP Note #1025361* jegyzetre. Bizonyosodjon meg róla, hogy az **SAP NetWeaver** kódtár architektúrája (32 vagy 64 bites) megegyezik a **Power BI Desktop** telepítésével, majd telepítse az **SAP NetWeaver RFC SDK-t** az SAP-jegyzetnek megfelelően.
2. Az **Adatok lekérése** párbeszédpanelen az **Adatbázis** kategóriában megjelenik egy **SAP Business Warehouse-alkalmazáskiszolgáló** és egy **SAP Business Warehouse üzenetkezelési kiszolgáló** bejegyzés.
   
   ![](media/desktop-sap-bw-connector/sap_bw_2a.png)

## <a name="sap-bw-connector-features"></a>Az SAP BW Connector funkciói
A Power BI Desktopban az **SAP BW-összekötők** használatával importálhatók adatok az **SAP Business Warehouse-kiszolgáló** típusú kockákból, de a DirectQuery is használható. 

Az **SAP BW Connectorról** és annak a DirectQueryvel való használatáról [A DirectQuery és az SAP Business Warehouse (BW)](desktop-directquery-sap-bw.md) című cikkből tájékozódhat.

A kapcsolat kiépítéséhez kapcsolódáskor ki kell töltenie a *Kiszolgáló*, a *Rendszer száma* és az *Ügyfélazonosító* mezőt.

![](media/desktop-sap-bw-connector/sap_bw_3a.png)

Két további **Speciális beállítást** is megadhat: a nyelvkódot, valamint a megadott kiszolgálón futtatható egyéni MDX-utasítást.

![](media/desktop-sap-bw-connector/sap_bw_4a.png)

Ha nincs MDX-utasítás megadva, a **Kezelő** ablak jelenik meg, amely a kiszolgálón elérhető kockák listáját mutatja, valamint az elérhető kockák részletes elemzését és elemeit, köztük a dimenziók és mértékek kiválasztását lehetővé tevő beállításokat. A Power BI-ban elérhetőek a [BW Open Analysis Interface OLAP BAPI-kban](https://help.sap.com/saphelp_nw70/helpdata/en/d9/ed8c3c59021315e10000000a114084/content.htm) elérhető lekérdezések és kockák.

Amikor kijelöl egy vagy több elemet a kiszolgálón, a rendszer a kijelölés alapján létrehozza a kimeneti tábla előnézetét.

![](media/desktop-sap-bw-connector/sap_bw_5.png)

A **Kezelő** ablakban néhány **megjelenítési beállítás** is elérhető, amelyekkel a következőket állíthatja be:

* **Megjelenítés – *Csak a kijelölt elemek* vagy *Összes elem* (alapértelmezett nézet):** Ezzel a beállítással ellenőrizheti a kiválasztott elemek végleges halmazát. Ezt az *Előnézet* területen az *Oszlopnevek* kiválasztásával is megtekintheti.
* **Adatok előnézetének engedélyezése (alapértelmezett viselkedés):** Szabályozhatja azt is, hogy a párbeszédablakban megjelenjenek-e az adatelőnézetek. Az adatelőnézetek letiltása csökkenti a kiszolgálói hívások mennyiségét, mivel a rendszer nem kér le adatokat az előnézetekhez.
* **Technikai nevek:** Az SAP BW támogatja a kockákban lévő objektumokra vonatkozó *technikai nevek* koncepciót. A technikai nevek segítségével a kocka tulajdonosa *felhasználóbarát* nevekkel jelenítheti meg a kockában lévő objektumokat, nem csupán azok *fizikai neveivel*.

![](media/desktop-sap-bw-connector/sap_bw_6.png)

Miután kijelölte az összes szükséges objektumot a **Kezelőben** a **Kezelő** ablak alján lévő alábbi gombokkal meghatározhatja a következő lépéseket:

* A **Betöltés** gombbal a rendszer betölti a kimeneti tábla teljes sorkészletét a Power BI Desktop-adatmodellbe, majd átvált a **Jelentés** nézetbe, ahol elkezdheti összeállítani az adatok vizualizációját, és további módosításokat végezhet az **Adatok** és **Kapcsolatok** nézetek használatával.
* A **Szerkesztés** gomb megnyitja a **Lekérdezésszerkesztőt**, ahol további adatátalakítási és -szűrési lépéseket hajthat végre, mielőtt a rendszer a teljes sorkészletet behúzza a Power BI Desktop-adatmodellbe.

Ne feledje, hogy az **SAP BW**-kockákból importálható adatok mellett adatforrások széles választékából importálhat még adatokat a Power BI Desktopba, és ezeket egyetlen jelentésbe kombinálhatja. Ez számos különféle izgalmas jelentéskészítési és elemzési forgatókönyvet tesz lehetővé az **SAP BW**-adatokra épülően.

## <a name="troubleshooting"></a>Hibaelhárítás
Ez a szakasz hibaelhárítási forgatókönyveket (és megoldásokat) mutat be az **SAP BW** Connector előzetes verziójának használatához.

1. Az **SAP BW** numerikus adataiban az ezreselválasztó vessző helyett pont szerepel. Például az 1,000,000 helyett 1.000.000 áll.
   
   Az **SAP BW** a tizedes értékeket *,* (vessző) vagy *.* (pont) karakterrel tördelve jeleníti meg. Annak meghatározásához, hogy a kettő közül melyiket használja az **SAP BW** tizedesjelként, a **Power BI Desktop** által használt illesztő meghívja a *BAPI_USER_GET_DETAIL* függvényt. Ez a hívás a **DEFAULTS** (Alapértékek) szerkezetet adja vissza, amelynek a *DCPFM* mezője tárolja a *tizedes formátum jelölését*. A következő három érték egyikét veheti fel:
   
       ‘ ‘ (space) = Decimal point is comma: N.NNN,NN
       'X' = Decimal point is period: N,NNN.NN
       'Y' = Decimal point is N NNN NNN,NN
   
   A hibát jelző ügyfelek azt tapasztalták, hogy a *BAPI_USER_GET_DETAIL* meghívásának hibája esetén az adott felhasználó (akinél az adatok nem megfelelően jelennek meg) a következőhöz hasonló hibaüzenetet kap:
   
       You are not authorized to display users in group TI:
           <item>
               <TYPE>E</TYPE>
               <ID>01</ID>
               <NUMBER>512</NUMBER>
               <MESSAGE>You are not authorized to display users in group TI</MESSAGE>
               <LOG_NO/>
               <LOG_MSG_NO>000000</LOG_MSG_NO>
               <MESSAGE_V1>TI</MESSAGE_V1>
               <MESSAGE_V2/>
               <MESSAGE_V3/>
               <MESSAGE_V4/>
               <PARAMETER/>
               <ROW>0</ROW>
               <FIELD>BNAME</FIELD>
               <SYSTEM>CLNTPW1400</SYSTEM>
           </item>
   
   A hiba megoldásához a felhasználónak meg kell kérnie az SAP-rendszergazdát, hogy engedélyezze a Power BI-ban használt SAPBW felhasználó számára a *BAPI_USER_GET_DETAIL* végrehajtását. Azt is érdemes ellenőrizni, hogy a felhasználónál a megfelelő *DCPFM* érték van-e beállítva a jelen hibaelhárítási forgatókönyvben korábban leírtaknak megfelelően.
2. **Az SAP BEx lekérdezések kapcsolódási beállításai**
   
   A **BEx** lekérdezések végrehajtásához a Power BI Desktopban engedélyezni kell egy adott tulajdonságot, amint az a következő képen látható:
   
   ![](media/desktop-sap-bw-connector/sap_bw_8.png)

## <a name="next-steps"></a>Következő lépések
Az SAP HANA-val és a DirectQueryvel kapcsolatos további információkért tekintse meg az alábbi forrásanyagokat:

* [DirectQuery és SAP HANA](desktop-directquery-sap-hana.md)
* [A DirectQuery használata a Power BI-ban](desktop-directquery-about.md)
* [A DirectQuery által támogatott adatforrások](desktop-directquery-data-sources.md)
* [Power BI és SAP BW - tanulmány](https://aka.ms/powerbiandsapbw)
