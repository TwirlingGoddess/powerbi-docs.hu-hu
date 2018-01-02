---
title: "Power BI-engedélyek"
description: "Power BI-engedélyek"
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
ms.date: 09/05/2017
ms.author: asaxton
ms.openlocfilehash: 27f62cf8ecce812d96c3984522e7f6c7d9e0605a
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="power-bi-permissions"></a>Power BI-engedélyek
## <a name="permission-scopes"></a>Engedélyek hatókörei
A Power BI-engedélyek lehetővé teszik az alkalmazások számára, hogy bizonyos műveleteket végezzenek a felhasználók nevében. Minden engedélyt jóvá kell hagynia egy felhasználónak, hogy érvényesek legyenek.

| Megjelenített név | Leírás | Hatókör értéke |
| --- | --- | --- |
| Az összes adatkészlet megtekintése |Az alkalmazás megtekintheti a bejelentkezett felhasználó összes adatkészletét, illetve azokat az adatkészleteket, amelyekhez a felhasználónak hozzáférése van. |Dataset.Read.All |
| Az összes adatkészlet olvasása és írása |Az alkalmazás megtekintheti a bejelentkezett felhasználó összes adatkészletét, illetve azokat az adatkészleteket, amelyekhez a felhasználónak hozzáférése van, továbbá írhat ezekbe az adatkészletekbe. |Dataset.ReadWrite.All |
| Adatok hozzáadása egy felhasználó adatkészletéhez (előzetes) |Hozzáférést nyújt egy alkalmazásnak egy felhasználó adatkészletbeli sorainak hozzáadásához vagy törléséhez. Ez az engedély nem nyújt hozzáférést az alkalmazásnak a felhasználó adataihoz. |Data.Alter_Any |
| Tartalom létrehozása (előzetes) |Az alkalmazás automatikusan tud létrehozni tartalmat és adatkészleteket egy felhasználóhoz. |Content.Create |
| Felhasználói csoportok megtekintése |Az alkalmazás megtekintheti az összes olyan csoportot, amelyeknek a bejelentkezett felhasználó a tagja. |Group.Read |
| Az összes csoport megtekintése |Az alkalmazás megtekintheti az összes olyan csoportot, amelyeknek a bejelentkezett felhasználó a tagja. |Group.Read.All |
| Az összes irányítópult megtekintése (előnézet) |Az alkalmazás megtekintheti a bejelentkezett felhasználó összes irányítópultját, illetve azokat az irányítópultokat, amelyekhez a felhasználónak hozzáférése van. |Dashboard.Read.All |
| Az összes jelentés megtekintése (előnézet) |Az alkalmazás megtekintheti a bejelentkezett felhasználó összes jelentését, illetve azokat a jelentéseket, amelyekhez a felhasználónak hozzáférése van. Az alkalmazás továbbá megtekintheti a jelentések adatait és struktúráját is. |Report.Read.All |
| Az összes jelentés olvasása és írása |Az alkalmazás megtekintheti a bejelentkezett felhasználó összes jelentését, illetve azokat a jelentéseket, amelyekhez a felhasználónak hozzáférése van, továbbá írhat ezekbe a jelentésekbe. Ez nem nyújt jogosultságot új jelentés létrehozására. |Report.ReadWrite.All |

Egy alkalmazás engedélyeket kérhet, amikor először kísérel meg bejelentkezni egy felhasználó oldalára a hívás hatókör-paraméterében a kért engedélyek megadásával. Ha megkapja az engedélyeket, a rendszer egy hozzáférési tokent ad vissza az alkalmazásnak, amely a későbbi API-hívásokon használható. A hozzáférést csak adott alkalmazás használhatja.

> [!NOTE]
> A Power BI API-k továbbra is csoportokként hivatkoznak az alkalmazás-munkaterületekre. Bármely csoportokra való utalás alkalmazás-munkaterületek használatát jelöli.
> 
> 

## <a name="requesting-permissions"></a>Engedélyek kérése
Bár behívhatja az API-t felhasználónévvel és jelszóval való hitelesítéshez, ha másik felhasználó nevében szeretne műveleteket végezni, olyan engedélyeket kell kérnie, amelyeket a felhasználó jóváhagy, majd az eredményül kapott hozzáférési tokent el kell küldenie az összes későbbi hívással. Ehhez a folyamathoz a standard [OAuth 2.0](http://oauth.net/2/) protokollt követjük. Bár a tényleges megvalósítás változó lehet, a Power BI OAuth folyamata a következő elemekből áll:

* **Bejelentkezési felhasználói felület** – Ez az a felhasználói felület, amelyet a fejlesztő engedélyek kérésére hívhat meg. A felület kéri a felhasználót a bejelentkezésre, ha még nem tette meg. A felhasználónak az alkalmazás által kért engedélyeket is jóvá kell hagynia. A bejelentkezési ablak visszaküld egy hozzáférési kódot vagy egy hibaüzenetet a megadott átirányítási URL-címre.
  * A Power BI-nak egy standard átirányítási URL-címet kell megadnia a natív alkalmazásokhoz.
* **Engedélyezési kód** – A rendszer engedélyezési kódokat ad vissza a webalkalmazásoknak az átirányítási URL-címen szereplő URL-paraméterekkel való bejelentkezés után. Mivel ezek paraméterekben szerepelnek, ez bizonyos biztonsági kockázattal jár. A webalkalmazásoknak engedélyezési tokenre kell cserélniük az engedélyezési kódot
* **Engedélyezési token** – Az API-hívások másik felhasználó nevében való hitelesítésére szolgál. Adott alkalmazásra lesz érvényes. A tokenek adott élettartammal rendelkeznek, és amikor lejárnak, frissítést igényelnek.
* **Token frissítése** – Amikor a jogkivonatok lejárnak, frissítési folyamat használható hozzájuk.

További kérdései vannak? [Forduljon a Power BI közösségéhez](http://community.powerbi.com/)

