---
title: "A Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítése"
description: "Tudnivalók a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítéséről"
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.author: maggies
ms.openlocfilehash: 589a77624169e9fb59999109668439c5f729c5f5
ms.sourcegitcommit: 7248b5e449b2495d6baef385470d18edfacec457
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2017
---
# <a name="install-power-bi-desktop-optimized-for-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítése
Tudnivalók a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítéséről.

Ha a Power BI jelentéskészítő kiszolgálóhoz szeretne Power BI-jelentéseket létrehozni, akkor le kell tölteni és telepíteni a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktopot. Ez különbözik a Power BI szolgáltatáshoz használt Power BI Desktop-kiadástól. A Power BI szolgáltatáshoz készült Power BI Desktopban például olyan előzetes funkciók érhetők el, amelyek a kiadásuk után a Power BI jelentéskészítő kiszolgáló részét fogják képezni. Ha ezt a verziót használja, akkor a jelentéskészítő kiszolgáló a jelentések és a modell ismert verzióját használhatja. 

> [!NOTE]
> A Power BI Desktop és a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop egymás mellett telepíthető.

## <a name="download-and-install-power-bi-desktop"></a>A Power BI Desktop letöltése és telepítése

Ha ellenőrizné, hogy a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop legújabb verzióját használja-e, akkor a jelentéskészítő kiszolgáló webportáljáról induljon.

1. A jelentéskészítő kiszolgáló webportálján kattintson a **Letöltés** nyíl > **Power BI Desktop** lehetőségre.

    ![A Power BI Desktop letöltése a webportálról](media/install-powerbi-desktop/report-server-download-web-portal.png)

    De azt is megteheti, hogy a Microsoft letöltőközpontjában közvetlenül a [Microsoft Power BI Desktop](https://go.microsoft.com/fwlink/?linkid=861076) [A Power BI jelentéskészítő kiszolgálóra (2017. október) optimalizált Microsoft Power BI Desktop] hivatkozást választja.

2. A letöltőközpontlapon kattintson a **Letöltés** gombra.

3. A számítógépétől függően válassza az alábbiak egyikét: 

    - **PBIDesktopRS.msi** (32 bites verzió) vagy

    - **PBIDesktopRS_x64.msi** (64 bites verzió).

1. A telepítő letöltése után indítsa el a Power BI Desktop (2017. október) telepítési varázslóját.
2. A telepítés végén kattintson a **Power BI Desktop azonnali indítása** lehetőségre.
   
    A folyamat automatikusan elindul, és máris hozzákezdhet.

## <a name="verify-you-are-using-the-correct-version"></a>Annak ellenőrzése, hogy a megfelelő verziót használja-e
Ellenőrizheti, hogy a Power BI Desktop megfelelő verzióját használja-e a Power BI Desktop indítóképernyőjének vagy címsorának megtekintésével. A címsor a kiadás hónapját és évét jelzi.

![A Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop címsora](media/quickstart-create-powerbi-report/report-server-desktop-october-2017-version.png)

A Power BI szolgáltatás Power BI Desktop verziójának címsorában nem szerepel a hónap és az év.

## <a name="file-extension-association"></a>Fájlkiterjesztés társítása
Ha a Power BI Desktopot és a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktopot ugyanarra a gépre telepítette, a Power BI Desktop legutóbbi telepítése rendelkezik a .pbix fájltársítással. Ez azt jelenti, hogy amikor duplán kattint egy pbix-fájlra, az a legutóbb telepített Power BI Desktopot indítja el.

Ha először a Power BI Desktopot telepítette, majd a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktopot, az összes pbix-fájl alapértelmezés szerint a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktopban nyílik meg. Ha azt szeretné, hogy inkább a Power BI Desktop induljon el alapértelmezés szerint a pbix-fájlok megnyitásakor, telepítse újra a Power BI Desktopot a Power BI szolgáltatásból.

Azt is megteheti, hogy először megnyitja a Power BI Desktop használni kívánt verzióját, majd megnyitja a fájlt a Power BI Desktopból.

Ha egy Power BI-jelentést szerkeszt a Power BI jelentéskészítő kiszolgálóból vagy új Power BI-jelentést hoz létre a webes portálról, mindig a Power BI Desktop megfelelő verziója nyílik meg.

## <a name="next-steps"></a>További lépések
Most, hogy telepítette a Power BI Desktopot, megkezdheti Power BI-jelentések létrehozását.

[Rövid útmutató: Power BI-jelentés létrehozása a Power BI jelentéskészítő kiszolgálóhoz](quickstart-create-powerbi-report.md)  
[Első lépések a Power BI Desktopban](../desktop-getting-started.md)  
Irányított útmutató: [Első lépések a Power BI Desktopban](../guided-learning/gettingdata.yml#step-2)  
[A felhasználói kézikönyv áttekintése, Power BI jelentéskészítő kiszolgáló](user-handbook-overview.md)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

