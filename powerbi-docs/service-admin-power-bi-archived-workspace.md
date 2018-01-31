---
title: "A Power BI archivált munkaterülete"
description: "A Power BI archivált munkaterülete az Office 365-bérlő kezelése után"
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 06/28/2017
ms.author: maghan
ms.openlocfilehash: 7698a1207f19382430fb8e225543b32b6aebcd49
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/30/2018
---
# <a name="power-bi-archived-workspace"></a>A Power BI archivált munkaterülete
A Power BI-ra bárki perceken belül regisztrálhat, és megkezdheti a szolgáltatás használatát.  Később a vállalat IT-részlege dönthet úgy, hogy átveszi a Power BI-nak a vállalat felhasználói számára történő kezelését.  Ha ez az átvétel megtörténik, akkor élvezheti a vállalat felhasználóinak és engedélyeinek központi kezelését, és kihasználhatja az egyszerűbb bejelentkezés előnyeit ugyanazzal a felhasználónévvel és jelszóval, amelyet a vállalat más szolgáltatásaiban is használ. 

Azok a tartalmak, amelyeket még azelőtt hozott létre, hogy az IT-részleg megkezdte a Power BI kezelését, a Power BI archivált munkaterületére kerülnek, amely a [Power BI](https://app.powerbi.com) bal oldali navigációs paneljéről érhető el.  Az új Power BI-tartalom létrehozását a Saját munkaterületen kezdheti meg, melyet a vállalat IT-részlege biztosít és kezel.  Az archivált munkaterület továbbra is megmarad, de az abban tárolt tartalmon végezhető műveletek korlátozottak lesznek.  A korlátozások eltávolításához át kell telepítenie az archivált munkaterületről a tartalmat az IT-részleg által kezelt Saját munkaterületre.

## <a name="restrictions-in-your-archived-workspace"></a>Az archivált munkaterület korlátozásai
Az archivált munkaterületről nem lesz törölve tartalom.  Továbbra is letölthet adatokat, létrehozhat jelentéseket és irányítópultokat, és frissítheti az adatkészleteket.  Azok a meglévő felhasználók, akikkel már megosztott tartalmat, továbbra is megtekinthetik azt a saját archivált munkaterületükön.

Azonban az archivált munkaterületen található tartalomra néhány korlátozás is vonatkozik:

* **OneDrive Vállalati verzió.  **Az archivált munkaterületen található adatkészletek esetében többé nem fog tudni adatokat letölteni vagy frissíteni a OneDrive Vállalati verzióból.  Ha ehhez a forráshoz próbál kapcsolódni, figyelmeztetés fog kapni.
* **Irányítópultok megosztása.  **Az archivált munkaterületről nem oszthat meg irányítópultokat más felhasználókkal.  Azok a felhasználók, akik már rendelkeznek hozzáféréssel, továbbra is megtekinthetik a megosztott irányítópultokat az archivált munkaterületük elérésével.
* **Csoportok létrehozása.  **Az archivált munkaterületen nem hozhat létre csoportokat.
* **Hozzáférés a Power BI-mobilalkalmazásokban.  **Bár továbbra is megtekintheti a webes tartalmat az archivált munkaterületen, ez a tartalom többé nem fog megjelenni a Power BI-mobilalkalmazásokban.

## <a name="migrating-content-in-your-archived-workspace"></a>Tartalom migrálása az archivált munkaterületen
A Power BI további használatához az IT-részlege által kezelt Saját munkaterületen kell új tartalmat létrehoznia.   Meg kell terveznie az archivált munkaterületen lévő tartalom Saját munkaterületre való migrálását is.  A tartalom migrálásának módja a tartalom típusától függ:

* **Excel- vagy Power BI Desktop-adatkészletek.  **Ezeknek az adatkészleteknek a migrálásához váltson az archivált munkaterületről a Saját munkaterületre, és töltse fel újra az Excel- vagy Power BI Desktop-fájlt a „My Data” (Adataim) gombbal.  Ha állított be ütemezett frissítést, ezt a beállítást újra meg kell adnia a Saját munkaterületen található új adatkészlethez.
* **Egyéb adatkészletek.  **Váltson a Saját munkaterületre, és kattintson az Adatok lekérése gombra az archivált munkaterületen létrehozott egyéb adatkészletekhez való újrakapcsolódáshoz.  Lehet, hogy újra meg kell adnia a biztonsági vagy kapcsolódási adatokat.
* **Jelentések.  **Az Excel- vagy Power BI Desktop-fájlokban található jelentések vagy a tartalomcsomagok részeként telepített jelentések automatikusan újra létrejönnek, miután újra feltöltötte a megfelelő Excel- vagy Power BI Desktop-fájlt, vagy újrakapcsolódott a tartalomcsomaghoz.  Ha a Power BI szolgáltatásban hozta létre a jelentéseit, akkor ezeket újra létre kell hoznia a Saját munkaterületen.
* **Irányítópultok.  **A tartalomcsomagok részeként telepített irányítópultok automatikusan újra létrejönnek, amikor újrakapcsolódik a tartalomcsomaghoz a Saját munkaterületen.  Ha a Power BI szolgáltatásban hozta létre az irányítópultjait, akkor ezeket újra létre kell hoznia a Saját munkaterületen.

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

