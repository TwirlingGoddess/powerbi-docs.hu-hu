---
title: Csatlakozás a Salesforce-hoz a Power BI-ban
description: Salesforce a Power BI-ban
services: powerbi
documentationcenter: ''
author: SarinaJoan
manager: kfile
backup: maggiesMSFT
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: 8089c796441fd4200b146da6330dd5c208bf8b30
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="connect-to-salesforce-with-power-bi"></a>Csatlakozás a Salesforce-hoz a Power BI-ban
A Power BI használatával könnyedén csatlakozhat a Salesforce.com-fiókjához. A létrehozott kapcsolat lekéri az adatokat, és automatikusan a rendelkezésére bocsátja az adatokhoz kapcsolódó irányítópultot és jelentéseket.

Kapcsolódjon a Power BI-hoz készült [Salesforce tartalomcsomaghoz](https://app.powerbi.com/getdata/services/salesforce), vagy tájékozódjon tovább a [Salesforce és a Power BI integrációjáról](https://powerbi.microsoft.com/integrations/salesforce).

## <a name="how-to-connect"></a>A kapcsolódás menete
1. Kattintson az **Adatok lekérdezése** elemre a bal oldalon lévő navigációs ablaktábla alján.
   
   ![](media/service-connect-to-salesforce/pbi_getdata.png) 
2. A **Szolgáltatások** dobozban kattintson a **Beolvasás** elemre.
   
   ![](media/service-connect-to-salesforce/pbi_getservices.png) 
3. Válassza a **Salesforce** lehetőséget, majd kattintson a **Beolvasás** elemre.  
   
   ![](media/service-connect-to-salesforce/salesforce.png)
4. A **Bejelentkezés** gombra kattintva kezdeményezze a bejelentkezési folyamatot.
   
    ![](media/service-connect-to-salesforce/dialog.png)
5. Amikor a rendszer kéri, adja meg a Salesforce-fiókja hitelesítő adatait. Az **Engedélyezés** gombra kattintva tegye elérhetővé az alapvető Salesforce-információkat és -adatokat a Power BI számára.
   
   ![](media/service-connect-to-salesforce/sf_authorize.png)
6. A legördülő menü alábbi beállításával adja meg, hogy mit szeretne importálni a Power BI-ba:
   
   * **Irányítópult**
     
     Válasszon ki egy személyen (például **Értékesítési igazgató**) alapuló, előre meghatározott irányítópultot. Az ilyen irányítópultok a Salesforce adott szabvány-adatkészletét jelenítik meg, és nem tartalmaznak egyéni mezőket.
     
     ![](media/service-connect-to-salesforce/pbi_salesforcechooserole.png)
   * **Jelentések**
     
     Válasszon ki egy vagy több egyéni jelentést a Salesforce-fiókjából. Ezek a jelentések megegyeznek a Salesforce-beli saját nézetekkel, és tartalmazhatnak egyéni mezőkből és objektumokból származó adatokat.
     
     ![](media/service-connect-to-salesforce/pbi_salesforcereports.png)
     
     Ha nem lát jelentést, vegye fel vagy hozza létre a Salesforce-fiókban, majd kísérelje meg újra a csatlakozást.
7. Az importálás megkezdéséhez kattintson a **Csatlakozás** lehetőségre. Az importálás során megjelenik egy értesítés, hogy az importálás folyamatban van. Ha az importálás befejeződött, a bal oldali navigációs ablaktáblán megjelenik a Salesforce-adatokat tartalmazó irányítópult, jelentés és adatkészlet.
   
   ![](media/service-connect-to-salesforce/pbi_getdatasalesforcedash.png)

Az adatok igény szerinti megjelenítéséhez tetszés szerint módosíthatja az irányítópultot. Kérdéseket tehet fel a Q&A használatával – Vagy kattintson egy csempére [az alapjául szolgáló jelentés megnyitásához](service-dashboard-tiles.md), és [módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton.

**Hogyan tovább?**

* [Tegyen fel egy kérdést a Q&A mezőben](power-bi-q-and-a.md), amely az irányítópult tetején található
* [Módosítsa a csempéket](service-dashboard-edit-tile.md) az irányítópulton
* [Kattintson egy csempére](service-dashboard-tiles.md) az alapjául szolgáló jelentés megnyitásához
* Az adatkészlet az ütemezés szerint naponta frissül, de módosíthatja is a frissítési ütemezést, vagy igény szerint frissíthet bármikor az **Azonnali frissítés** lehetőségre kattintva.

## <a name="system-requirements"></a>Rendszerkövetelmények
* Kapcsolódás egy éles környezetben lévő Salesforce-fiókhoz, amelyen engedélyezve van az API-hozzáférés
* Engedély a Power BI alkalmazásnak a bejelentkezéskor
* Elegendő elérhető API-hívás a fiók számára az adatok lekéréséhez és frissítéséhez
* A frissítéshez érvényes hitelesítési jogkivonatra van szükség. Ellenőrizze, hogy 5, vagy annál kevesebb Salesforce-adatkészletet importált-e, mert a Salesforce legfeljebb 5 hitelesítési jogkivonatot engedélyez alkalmazásonként

## <a name="troubleshooting"></a>Hibaelhárítás
Ha hibát észlel, tekintse át a fenti követelményeket. Azt is vegye figyelembe, hogy az egyéni vagy tesztkörnyezeti tartományba való bejelentkezés jelenleg nem támogatott.

## <a name="next-steps"></a>Következő lépések
[Első lépések a Power BI használatával](service-get-started.md)

[Adatok lekérése](service-get-data.md)

