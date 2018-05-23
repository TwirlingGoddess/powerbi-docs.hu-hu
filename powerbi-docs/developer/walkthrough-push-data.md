---
title: Adatok elküldése adatkészletbe
description: Adatok elküldése Power BI-adatkészletbe
author: markingmyname
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-developer
ms.topic: conceptual
ms.date: 01/05/2017
ms.author: maghan
ms.openlocfilehash: 76d07c8384123a303c8801a45ecd05b9e6ed0321
ms.sourcegitcommit: 638de55f996d177063561b36d95c8c71ea7af3ed
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/17/2018
---
# <a name="push-data-into-a-power-bi-dataset"></a>Adatok elküldése Power BI-adatkészletbe
A Power BI API-val adatokat küldhet egy Power BI-adatkészletbe. Tegyük fel például, hogy ki szeretne bővíteni egy már meglévő üzleti munkafolyamatot kulcsfontosságú adatoknak az adatkészletbe történő elküldésével. Ebben az esetben egy Termék táblát tartalmazó Értékesítési marketing adatkészletet kíván elküldeni egy adatkészletbe.

Mielőtt elkezdené az adatok adatkészletbe való elküldését, szüksége lesz egy Azure Active Directoryra (Azure AD) és egy [Power BI-fiókra](create-an-azure-active-directory-tenant.md).

## <a name="steps-to-push-data-into-a-dataset"></a>Adatok adatkészletbe történő elküldésének lépései
* 1. lépés: [Alkalmazás regisztrálása az Azure AD-ben](walkthrough-push-data-register-app-with-azure-ad.md)
* 2. lépés: [Hitelesítéshez szükséges hozzáférési token beszerzése](walkthrough-push-data-get-token.md)
* 3. lépés: [Adatkészlet létrehozása a Power BI-ban](walkthrough-push-data-create-dataset.md)
* 4. lépés: [Adatkészlet lekérése, és sorok hozzáadása egy Power BI-táblához](walkthrough-push-data-get-datasets.md)
* 5. lépés: [Sorok hozzáadása egy Power BI-táblához](walkthrough-push-data-add-rows.md)

A következő szakasz egy általános ismertetés az adatok küldésére használható Power BI API-műveletekről.

## <a name="power-bi-api-operations-to-push-data"></a>Adatok küldésére használt Power BI API-műveletek
A Power BI REST API-val adatforrásokat küldhet a Power BI-ba. Amikor egy alkalmazás sorokat ad hozzá egy adatkészlethez, az irányítópulton lévő csempék automatikusan frissülnek az új adatokkal. Adatokat az [Adatkészlet létrehozása](https://msdn.microsoft.com/library/mt203562.aspx), illetve a [Sorok hozzáadása](https://msdn.microsoft.com/library/mt203561.aspx) művelettel küldhet. Egy adatkészlet kereséséhez használja az [Adatkészletek lekérése](https://msdn.microsoft.com/library/mt203567.aspx) műveletet. A fenti műveletek bármelyike esetében átadhat egy csoportazonosítót a csoporttal való munkavégzéshez. A [Csoportok lekérése](https://msdn.microsoft.com/library/mt243842.aspx) művelettel lekérheti a csoportazonosítók listáját.

Az adatok adatkészletbe történő elküldéséhez használható műveletek az alábbiak:

* [Adatkészlet létrehozása](https://msdn.microsoft.com/library/mt203562.aspx)
* [Adatkészletek lekérése](https://msdn.microsoft.com/library/mt203567.aspx)
* [Sorok hozzáadása](https://msdn.microsoft.com/library/mt203561.aspx)
* [Csoportok lekérése](https://msdn.microsoft.com/library/mt243842.aspx)

Adatkészletet úgy hozhat létre a Power BI-ban, hogy átad egy JavaScript Object Notation- (JSON-) karakterláncot a Power BI szolgáltatásnak. További információt a JSON-karakterláncokról [a JSON ismertetésében](http://json.org/) talál.

Az adatkészletek JSON-karakterláncának formátuma a következő:

**Power BI-adatkészlet JSON-objektuma**

    {"name": "dataset_name", "tables":
        [{"name": "", "columns":
            [{ "name": "column_name1", "dataType": "data_type"},
             { "name": "column_name2", "dataType": "data_type"},
             { ... }
            ]
          }
        ]
    }

Az Értékesítési marketing-adatkészlet példájában tehát az alábbihoz hasonló JSON-karakterláncot kellene átadnia. Ebben a példában a **SalesMarketing** az adatkészlet, a **Product** (Termék) pedig a tábla neve. A tábla meghatározása után a táblasémát kell meghatározni. A **SalesMarketing** adatkészlet esetében a táblaséma az alábbi oszlopokat tartalmazza ProductID (Termékazonosító), Manufacturer (Gyártó), Category (Kategória), Segment (Szegmens), Product (Termék) és IsComplete (Kész állapot).

**Példa adatkészlet-objektum JSON-ra**

    {
        "name": "SalesMarketing",
        "tables": [
            {
                "name": "Product",
                "columns": [
                {
                    "name": "ProductID",
                    "dataType": "int"
                },
                {
                    "name": "Manufacturer",
                    "dataType": "string"
                },
                {
                    "name": "Category",
                    "dataType": "string"
                },
                {
                    "name": "Segment",
                    "dataType": "string"
                },
                {
                    "name": "Product",
                    "dataType": "string"
                },
                {
                    "name": "IsCompete",
                    "dataType": "bool"
                }
                ]
            }
        ]
    }

Power BI-táblaséma esetén az alábbi adattípusok használhatók.

## <a name="power-bi-table-data-types"></a>Power BI-tábla adattípusai
| **Adattípus** | **Korlátozások** |
| --- | --- |
| Int64 |Az Int64.MaxValue és Int64.MinValue érték nem engedélyezett. |
| Double |A Double.MaxValue és Double.MinValue érték nem engedélyezett. A számtól eltérő értékek (NaN) nem támogatottak. +Infinity és -Infinity értékek nem támogatottak egyes függvényekben (pl.: Min, Max). |
| Boolean |Nincsenek |
| Datetime |Az adatok betöltése során kvantáljuk az értékeket a napok törtrészével az 1/300 másodperc (3,33 ms) egész többszörösévé. |
| String |Jelenleg legfeljebb 128 ezer karakter hosszú lehet. |

## <a name="learn-more-about-pushing-data-into-power-bi"></a>További információk az adatoknak a Power BI-ba leküldésével kapcsolatban
Az adatok adatkészletekbe történő küldésének első lépéseihez tekintse meg a bal oldali navigációs ablaktábla [1. lépés: Alkalmazás regisztrálása az Azure AD-ben](walkthrough-push-data-register-app-with-azure-ad.md) című szakaszát.

[Következő lépés >](walkthrough-push-data-register-app-with-azure-ad.md)

## <a name="next-steps"></a>Következő lépések
[Regisztráció a Power BI-ra](create-an-azure-active-directory-tenant.md)  
[Adatkészlet létrehozása](https://msdn.microsoft.com/library/mt203562.aspx)  
[Adatkészletek lekérése](https://msdn.microsoft.com/library/mt203567.aspx)  
[Sorok hozzáadása](https://msdn.microsoft.com/library/mt203561.aspx)  
[Csoportok lekérése](https://msdn.microsoft.com/library/mt243842.aspx)  
[A JSON ismertetése](http://json.org/)  
[A Power BI REST API áttekintése](overview-of-power-bi-rest-api.md)  
További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

