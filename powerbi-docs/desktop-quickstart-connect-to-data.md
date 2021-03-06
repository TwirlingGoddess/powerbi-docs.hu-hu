---
title: Gyors csatlakozás adatokhoz
description: Csatlakozás adatforráshoz a Power BI Desktopban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: quickstart
ms.date: 07/27/2018
ms.author: davidi
LocalizationGroup: quickstart
ms.openlocfilehash: f7266691573c0d02bafa7120b5d4a28ff0c03076
ms.sourcegitcommit: f01a88e583889bd77b712f11da4a379c88a22b76
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/27/2018
ms.locfileid: "39327661"
---
# <a name="quickstart-connect-to-data-in-power-bi-desktop"></a>Gyorsútmutató: Csatlakozás adatokhoz a Power BI Desktopban

Ebben az útmutatóban a **Power BI Desktop** használatával csatlakozunk adatokhoz, ami az adatmodellek és jelentések létrehozásának első lépése.

![Power BI Desktop](media/desktop-what-is-desktop/what-is-desktop_01.png)

Ha még nem regisztrált a Power BI-ra, a kezdés előtt [hozzon létre egy ingyenes próbaverziós fiókot](https://app.powerbi.com/signupredirect?pbi_source=web).

## <a name="prerequisites"></a>Előfeltételek

Az cikkben ismertetett lépések elvégzéséhez az alábbiakra lesz szüksége:
* Töltse le és telepítse a **Power BI Desktopot**, amely ingyenes alkalmazás, és helyi számítógépen fut. Közvetlenül is [letöltheti a **Power BI Desktopot**](https://powerbi.microsoft.com/desktop), vagy beszerezheti [a **Microsoft Store-ból**](http://aka.ms/pbidesktopstore) is.
* [Töltse le ezt az Excel-munkafüzet mintát](http://go.microsoft.com/fwlink/?LinkID=521962), és hozzon létre egy mappát *C:\PBID-qs* néven, ahol az Excel-fájlt tárolja majd. Az útmutató további lépéseinél feltételezzük, hogy a letöltött Excel-munkafüzet ebben a mappában található.

## <a name="launch-power-bi-desktop"></a>A Power BI Desktop elindítása

Telepítés után indítsa el a **Power BI Desktopot** a helyi számítógépén. Egy üres vászon nyílik meg: itt hozhat létre vizualizációkat és jelentéseket azokból az adatokból, amelyekhez csatlakozott. 

![Power BI Desktop – üres vászon](media/desktop-quickstart-connect-to-data/qs-connect-data_01.png)

## <a name="connect-to-data"></a>Csatlakozás adatokhoz

A **Power BI Desktoppal** számos különböző adattípushoz csatlakozhat. Csatlakozhat egyszerű adattípusokhoz, például Microsoft Excel-fájlokhoz is, vagy olyan online szolgáltatásokhoz is, amelyek sokféle adattípust tartalmaznak, például a Salesforce-hoz, a Microsoft Dynamicshez, az Azure Blob Storage-hoz és sok más forráshoz. 

Adatokhoz való csatlakozáshoz a **Kezdőlap** menüszalagon válassza az **Adatok lekérése** lehetőséget.

![Adatok lekérése](media/desktop-quickstart-connect-to-data/qs-connect-data_02.png)

Ekkor megjelenik az **Adatok lekérése** ablak, ahol választhat a különféle adatforrások közül, amelyekhez a **Power BI Desktop** csatlakozni képes. Ebben az útmutatóban azt az Excel-munkafüzetet használjuk, amelyet korábban már letöltött a cikk elején található *Előfeltételek* szakaszban leírtak szerint. 

![Adatok lekérése](media/desktop-quickstart-connect-to-data/qs-connect-data_03.png)

Mivel ez egy Excel-fájl, ezért az **Adatok lekérése** ablakban az **Excel** lehetőséget választjuk, majd pedig a **Csatlakozás** gombra kattintunk.

A rendszer kéri annak az Excel-fájlnak a helyét, amelyhez csatlakozni szeretnénk. A letöltött fájl neve *Financial Sample* (Pénzügyi elemzési minta), ezért ezt a fájlt választjuk ki, majd a **Megnyitás** lehetőséget választjuk.

![Adatok lekérése](media/desktop-quickstart-connect-to-data/qs-connect-data_04.png)

A **Power BI Desktop** ezt követően betölti a munkafüzetet, és beolvassa a tartalmát, majd megmutatja az elérhető adatokat is a **Navigátor** ablakban, ahol kiválaszthatja, mely adatokat szeretné betölteni a Power BI Desktopba. Az importálni kívánt táblákat a táblák melletti jelölőnégyzetek bejelölésével választhatja ki. Ebben az esetben mindkét elérhető táblát importálni fogjuk.

![Adatok lekérése](media/desktop-quickstart-connect-to-data/qs-connect-data_05.png)

Ha kiválasztotta az összes importálni kívánt táblát, válassza a **Betöltés** lehetőséget, ezzel importálja az adatokat a Power BI Desktopba.

## <a name="view-data-in-the-fields-pane"></a>Adatok megtekintése a Mezők panelen

A táblák betöltése után a **Mezők** táblán jelennek meg az adatok. A táblákat úgy bonthatja ki, ha a név melletti háromszögre kattint. Az alábbi képen a *financials* tábla van kibontva, amelynek így az összes mezője láthatóvá válik. 

![Adatok lekérése](media/desktop-quickstart-connect-to-data/qs-connect-data_06.png)

Ezzel készen is van! Csatlakozott az adatokhoz a **Power BI Desktoppal**, betöltötte az adatokat, és most már láthatja a táblákban elérhető mezőket is.


## <a name="next-steps"></a>Következő lépések
Az adatokhoz való csatlakozás után sokféle dolgot végezhet el a **Power BI Desktoppal**, többek között vizualizációkat és jelentéseket is létrehozhat. Az első lépésekhez tekintse meg az alábbi forrást:

* [Első lépések útmutató – Power BI Desktop](desktop-getting-started.md)


