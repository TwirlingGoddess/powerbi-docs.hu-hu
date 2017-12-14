---
title: "A Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítése"
description: "Tudnivalók a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítéséről"
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
ms.date: 06/20/2017
ms.author: asaxton
ms.openlocfilehash: 5fd5f41523ffcba03eb4749a9560922bcff42a7c
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="install-power-bi-desktop-optimized-for-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítése
Tudnivalók a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop telepítéséről.

Le kell töltenie és telepítenie kell a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktopot. Ez különbözik a Power BI szolgáltatáshoz használt Power BI Desktop-kiadástól. Erre azért van szükség, hogy a jelentéskészítő kiszolgáló a jelentések és a modell ismert verzióját használhassa. 

> [!NOTE]
> A Power BI Desktop és a Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktop egymás mellett telepíthető.
> 
> 

## <a name="download-and-install"></a>Letöltés és telepítés
A Power BI jelentéskészítő kiszolgálóhoz optimalizált Power BI Desktopot a [Microsoft letöltőközpontból](https://go.microsoft.com/fwlink/?linkid=837581) vagy a jelentéskészítő kiszolgáló webes portáljáról töltheti le.

A telepítő letöltése után telepítheti a Power BI Desktopot.

## <a name="verify-you-are-using-the-correct-version"></a>Annak ellenőrzése, hogy a megfelelő verziót használja-e
Ellenőrizheti, hogy a Power BI Desktop megfelelő verzióját használja-e a Power BI Desktop indítóképernyőjének vagy címsorának megtekintésével. A címsor a kiadás hónapját és évét jelzi.

![](media/install-powerbi-desktop/powerbi-desktop-rs-title-bar.png "A Power BI Desktop címsora")

A Power BI szolgáltatás Power BI Desktop-verziójának nem szerepel a címsorában a hónap és az év.

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

