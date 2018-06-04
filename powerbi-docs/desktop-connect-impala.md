---
title: Csatlakozás Impala-adatbázishoz a Power BI Desktopban
description: Könnyedén csatlakozhat Impala-adatbázisokhoz, és használhatja a bennük tárolt adatokat a Power BI Desktopban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 04/24/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 9b00120a0c4c22ba8f031663ab19d94d2c482d3b
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34287693"
---
# <a name="connect-to-an-impala-database-in-power-bi-desktop"></a>Csatlakozás Impala-adatbázishoz a Power BI Desktopban
A Power BI Desktopban csatlakozhat egy **Impala**-adatbázishoz, és úgy használhatja az alapul szolgáló adatokat, mint a Power BI Desktop bármely más adatforrását.

## <a name="connect-to-an-impala-database"></a>Kapcsolódás Impala-adatbázishoz
Ha csatlakozni kíván egy **Impala**-adatbázishoz, válassza az **Adatok lekérése** lehetőséget a Power BI Desktop **Kezdőlap** menüszalagján. A bal oldali kategóriák közül válassza az **Adatbázis** lehetőséget, ekkor megjelenik az **Impala**.

![](media/desktop-connect-impala/connect_impala_2.png)

A megjelenő **Impala** ablakban írja vagy illessze be az Impala-kiszolgáló nevét a mezőbe, és válassza az **OK** gombot. Vegye figyelembe, hogy az adatokat közvetlenül is **importálhatja** a Power BI-ba, vagy használhatja a **DirectQueryt**. További információ a DirectQueryről: [A DirectQuery használata](desktop-use-directquery.md).

![](media/desktop-connect-impala/connect_impala_3a.png)

Amikor a rendszer kéri, adja meg a hitelesítő adatait, vagy válassza a névtelen csatlakozást. Az Impala-összekötő támogatja a névtelen, az egyszerű (felhasználónév + jelszó) és a Windows-hitelesítést.

![](media/desktop-connect-impala/connect_impala_4.png)

> [!NOTE]
> Ha egy adott **Impala**-kiszolgálóhoz megadta a felhasználónévét és a jelszavát, a Power BI Desktop ugyanazon hitelesítő adatokat fogja használni a későbbi csatlakozási kísérletekhez is. A hitelesítő adatokat a **Fájl > Lehetőségek és beállítások > Adatforrás-beállítások** szakaszában módosíthatja.
> 
> 

Ha sikeresen csatlakozott, megjelenik a **Kezelő** ablaka, és megjeleníti a kiszolgálón elérhető adatokat. Ezek közül kiválaszthat egy vagy több importálni kívánt elemet, és használhatja őket a **Power BI Desktopban**.

![](media/desktop-connect-impala/connect_impala_5.png)

## <a name="considerations-and-limitations"></a>Megfontolandó szempontok és korlátozások
Az **Impala**-összekötő használatára vonatkozik néhány korlátozást és egyéb szempont.

* Az Impala-összekötőt támogatják a helyszíni adatátjárók, bármelyik hitelesítési módot is válassza a három támogatott közül.

## <a name="next-steps"></a>Következő lépések
A Power BI Desktop használatával számos adatforráshoz csatlakozhat. Az adatforrásokkal kapcsolatos információkért lásd az alábbi forrásanyagokat:

* [Első lépések a Power BI Desktopban](desktop-getting-started.md)
* [Adatforrások a Power BI Desktopban](desktop-data-sources.md)
* [Adatok formázása és kombinálása a Power BI Desktoppal](desktop-shape-and-combine-data.md)
* [Kapcsolódás az Excelhez a Power BI Desktopban](desktop-connect-excel.md)   
* [Adatok közvetlen bevitele a Power BI Desktopba](desktop-enter-data-directly-into-desktop.md)   

