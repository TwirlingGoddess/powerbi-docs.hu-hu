---
title: "Hiba: Nem található adat az Excel-munkafüzetben"
description: "Hiba: Nem található adat az Excel-munkafüzetben"
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.author: davidi
LocalizationGroup: Troubleshooting
ms.openlocfilehash: a58af88d23c04c0afd2fa71cab7824b657451b33
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/24/2018
---
# <a name="error-we-couldnt-find-any-data-in-your-excel-workbook"></a>Hiba: Nem található adat az Excel-munkafüzetben

>[!NOTE]
>Ez a cikk az Excel 2007-es vagy újabb verzióira vonatkozik.

Excel-munkafüzet Power BI-ba történő importálásakor a következő hiba jelenhet meg:

*Hiba: Nem található adat az Excel-munkafüzetben. Lehet, hogy az adatok nem megfelelő formátumúak. A munkafüzetet szerkesztenie kell az Excelben, majd újra kell importálnia.*

![](media/service-admin-troubleshoot-excel-workbook-data/pbi_wecouldntfindanydata.png)

## <a name="quick-solution"></a>Gyors megoldás
1. Szerkessze a munkafüzetet az Excelben.
2. Válassza ki az adatokat tartalmazó cellatartományt. Az első sornak az oszlopfejléceket (oszlopneveket) kell tartalmaznia.
3. Táblázat létrehozásához nyomja le a **Ctrl + T** billentyűket.
4. Mentse a munkafüzetet.
5. Térjen vissza a Power BI-ba, és importálja ismét a munkafüzetet, vagy ha az Excel 2016-ban dolgozik, és a OneDrive Vállalati verzióban mentette a munkafüzetet, kattintson a Fájl > Közzététel lehetőségre az Excelben.

## <a name="details"></a>Részletek
### <a name="cause"></a>Ok
Az Excelben cellatartományokból hozhat létre **táblázatot**, ami megkönnyíti az adatok rendezését, szűrését és formázását.

Excel-munkafüzet importálásakor a Power BI ezeket a táblázatokat keresi, majd egy adatkészletbe importálja őket, ha pedig nem talál táblázatot, akkor ez a hibaüzenet jelenik meg.

### <a name="solution"></a>Megoldás
1. Nyissa meg a munkafüzetet az Excelben. 
    >[!NOTE]
    >Ezek a képek az Excel 2013-ból valók. Ha más verziót használ, a megjelenés eltérő lehet, de a lépések ugyanazok.
    
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xlwksht1.png)
2. Válassza ki az adatokat tartalmazó cellatartományt. Az első sornak az oszlopfejléceket (oszlopneveket) kell tartalmaznia:
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xlwksht2.png)
3. A **BESZÚRÁS** lap menüszalagján kattintson a **Táblázat** elemre. (Vagy használja a **Ctrl + T** billentyűparancsot.)
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xlwksht3.png)
4. A következő párbeszédpanel jelenik meg. Ellenőrizze, hogy a **Táblázatban vannak fejlécek** lehetőség ki van jelölve, majd nyomja le az **OK** gombot:
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xlcreatetbl.png)
5. Az adatok most már táblázatként vannak formázva:
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_trb_xltbl.png)
6. Mentse a munkafüzetet.
7. Térjen vissza a Power BI-ba. Kattintson az Adatok lekérése elemre a bal oldali navigációs ablaktábla alján.
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_getdata.png)
8. A **Fájlok** mezőben válassza a **Beolvasás** lehetőséget.
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_getfiles.png)
9. Importálja újra az Excel-munkafüzetet. Az importálási folyamatnak most már sikeresen meg kell találnia a táblázatot.
   
    Ha az importálás még mindig sikertelen, hozza a tudomásunkra a Súgó menü **Közösség ** lehetőségére kattintva:
   
    ![](media/service-admin-troubleshoot-excel-workbook-data/pbi_questionmenucommunity.png)
