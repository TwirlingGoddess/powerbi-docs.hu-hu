---
title: Csatlakozás Amazon Redshift-adatbázishoz a Power BI Desktopban
description: Könnyedén csatlakozhat Amazon Redshift-adatbázisokhoz, és használhatja a bennük tárolt adatokat a Power BI Desktopban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 06/05/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: c90d2ecf5c3722dfa3991d7001f7c5054e48e6a6
ms.sourcegitcommit: e8d924ca25e060f2e1bc753e8e762b88066a0344
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/29/2018
ms.locfileid: "37135122"
---
# <a name="connect-to-amazon-redshift-in-power-bi-desktop"></a>Csatlakozás Amazon Redshifthez a Power BI Desktopban
A **Power BI Desktopban** csatlakozhat egy **Amazon Redshift**-adatbázishoz, és úgy használhatja az alapul szolgáló adatokat, mint a Power BI Desktop bármely más adatforrását.

## <a name="connect-to-an-amazon-redshift-database"></a>Csatlakozás egy Amazon Redshift-adatbázishoz
Ha csatlakozni szeretne egy **Amazon Redshift**-adatbázishoz, válassza a Power BI Desktop **Kezdőlap** menüszalagján az **Adatok lekérése** lehetőséget. Válassza a bal oldali kategóriák közül az **Adatbázis** elemet, és egyéb lehetőségek mellett az **Amazon Redshift** is megjelenik.

![](media/desktop-connect-redshift/connect_redshift_3.png)

A megjelenő **Amazon Redshift** ablakban írja vagy illessze be az **Amazon Redshift**-kiszolgáló és -adatbázis nevét a mezőbe. A *Kiszolgáló* mezőben a felhasználók meghatározhatnak egy portot a következő formátumban: *ServerURL:Port*

![](media/desktop-connect-redshift/connect_redshift_4.png)

Ha a rendszer kéri, adja meg a felhasználónevét és a jelszavát. A hibák elkerülése érdekében az SSL-tanúsítványban található kiszolgálónévvel pontosan megegyező nevet használjon. 

![](media/desktop-connect-redshift/connect_redshift_5.png)

Ha sikeresen csatlakozott, megjelenik a **Kezelő** ablaka, és megjeleníti a kiszolgálón elérhető adatokat. Ezek közül kiválaszthat egy vagy több importálni kívánt elemet, és használhatja őket a **Power BI Desktopban**.

![](media/desktop-connect-redshift/connect_redshift_6.png)

Ha kiválasztott valamit a **Kezelő** ablakban, **betöltheti** vagy **szerkesztheti** az adatokat.

* Ha úgy dönt, hogy **betölti** az adatokat, a rendszer rákérdez, hogy az *Importálás* vagy a *DirectQuery* üzemmódot szeretné-e használni. További információért tekintse meg ezt a [cikket, amely a DirectQuery használatát ismerteti](desktop-use-directquery.md).
* Ha a **Szerkesztés** mellett dönt, megjelenik a **Lekérdezésszerkesztő**, ahol sokféle módon átalakíthatja és szűrheti az adatokat, és a műveletek némelyike magára az alapul szolgáló **Amazon Redshift**-adatbázisra is hatással van (ha ez támogatott).

## <a name="next-steps"></a>Következő lépések
A Power BI Desktop használatával számos adatforráshoz csatlakozhat. Az adatforrásokkal kapcsolatos információkért lásd az alábbi forrásanyagokat:

* [Mi az a Power BI Desktop?](desktop-what-is-desktop.md)
* [Adatforrások a Power BI Desktopban](desktop-data-sources.md)
* [Adatok formázása és kombinálása a Power BI Desktoppal](desktop-shape-and-combine-data.md)
* [Kapcsolódás az Excelhez a Power BI Desktopban](desktop-connect-excel.md)   
* [Adatok közvetlen bevitele a Power BI Desktopba](desktop-enter-data-directly-into-desktop.md)   

