---
title: "Kapcsolódás a Windows fejlesztői központhoz a Power BI-jal"
description: "Windows fejlesztői központ a Power BI-hoz"
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: d88e10b4ee2e76444fccec0edabddd2a123d6b62
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-windows-dev-center-with-power-bi"></a>Kapcsolódás a Windows fejlesztői központhoz a Power BI-jal
A Power BI-tartalomcsomag használatával a Power BI-ban vizsgálhatja és figyelheti a Windows fejlesztői központ alkalmazáselemzési adatait. Az adatok naponta egyszer automatikusan frissülnek.

Kapcsolódjon a [Windows fejlesztői központ Power BI-tartalomcsomagjához](https://app.powerbi.com/getdata/services/devcenter).

## <a name="how-to-connect"></a>A kapcsolódás menete
1. Kattintson az **Adatok lekérése** elemre a bal oldalon lévő navigációs panel alján.
   
   ![](media/service-connect-to-windows-dev-center/getdata.png)
2. A **Szolgáltatások** mezőben válassza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-windows-dev-center/services.png)
3. Válassza a **Windows fejlesztői központ** \> **Beolvasás** lehetőséget.
   
   ![](media/service-connect-to-windows-dev-center/windowsdev.png)
4. Adja meg egy, a tulajdonában lévő alkalmazás azonosítóját és kattintson a Következő gombra. A [paraméterek megkereséséről](#FindingParams) alább olvashat részletesebben.
   
   ![](media/service-connect-to-windows-dev-center/params.png)
5. A **Hitelesítési módszer** beállításnál válassza az **oAuth2** \> **Bejelentkezés** elemet. Amikor a rendszer kéri, adja meg a Windows fejlesztői központ-fiókjához tartozó Azure Active Directory-hitelesítő adatokat (további részletek a [Rendszerkövetelmények](#Requirements) között).
   
    ![](media/service-connect-to-windows-dev-center/creds.png)
   
    ![](media/service-connect-to-windows-dev-center/creds2.png)
6. A jóváhagyás után az importálás automatikusan megkezdődik. Amikor befejeződik, új irányítópult, jelentés és modell jelenik meg a navigációs panelen. Válassza ki az irányítópultot az importált adatok megtekintéséhez, majd nyissa meg az alapul szolgáló jelentéseket egy csempe választásával.
   
    ![](media/service-connect-to-windows-dev-center/dashboard.png)
   
    ![](media/service-connect-to-windows-dev-center/report.png)

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A-mezőben](service-q-and-a.md), amely az irányítópult tetején található.
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.
* [Kattintson egy csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához.
* Az adatkészlet naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor, a **Frissítés** lehetőségre kattintva.

## <a name="whats-included"></a>A csomag tartalma
A fejlesztői központ Power BI-tartalomcsomag az alkalmazása elemzési adatait és IAP-beszerzéseit, minősítéseit, értékeléseit, és az alkalmazás állapotát tartalmazza. Az adatok csak az utolsó 3 hónapra terjednek ki. Az időintervallum változik, a dátumok az adatkészlet frissítésekor módosulnak.

<a name="Requirements"></a>

## <a name="system-requirements"></a>Rendszerkövetelmények
Ez a tartalomcsomag megkövetel legalább egy, a Windows Áruházban közzétett alkalmazást és egy Windows fejlesztői központ-fiókot (további részletek [itt](https://msdn.microsoft.com/windows/uwp/publish/manage-account-users)).

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
Egy alkalmazás azonosítóját az Alkalmazáskezelés alatti Alkalmazásidentitás lap megnyitásával találhatja meg.

Az alkalmazás azonosítója a Windows 10 Áruház-beli URL-cím végén található (https://www.microsoft.com/store/apps/ **{alkalmazásazonosító}**)

## <a name="next-steps"></a>További lépések
[Első lépések a Power BI-ban](service-get-started.md)

[Adatok beolvasása a Power BI-ban](service-get-data.md)

