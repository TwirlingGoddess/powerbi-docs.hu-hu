---
title: "Excel-munkafüzetből létrehozott adatkészlet frissítése (helyi)"
description: "Excel-munkafüzetből létrehozott adatkészlet frissítése helyi meghajtón"
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
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: fc061d2f8c85a53028e6de82e4a1e21057be6c75
ms.sourcegitcommit: b3ee37e1587f1269ee7dd9daf1685a06dea3b50c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/23/2017
---
# <a name="refresh-a-dataset-created-from-an-excel-workbook-on-a-local-drive"></a>Excel-munkafüzetből létrehozott adatkészlet frissítése helyi meghajtón
## <a name="whats-supported"></a>Mi támogatott?
A Power BI-ban a Frissítés most és a Frissítés ütemezése támogatott az olyan helyi meghajtóról importált Excel-munkafüzetekből létrehozott adatkészleteknél, ahol a Power Queryt (az Excel 2016-ban Adatok beolvasása és átalakítása) vagy a Power Pivotot használják a következő adatforrások valamelyikéhez való kapcsolódásra, és az adatok Excel-adatmodellbe való betöltésére:  

### <a name="power-bi-gateway---personal"></a>Power BI Gateway – Personal
* Minden online adatforrás megjelenik az Excelhez készült Microsoft Power Queryben.
* Minden helyszíni adatforrás megjelenik a Power Queryben a Hadoop-fájlokat (HDFS) és a Microsoft Exchange-t kivéve.
* Minden online adatforrás megjelenik a Power Pivotban.\*
* Minden helyszíni adatforrás megjelenik a Power Pivotban a Hadoop-fájlokat (HDFS) és a Microsoft Exchange-t kivéve.

<!-- Refresh Data sources-->
[!INCLUDE [refresh-datasources](./includes/refresh-datasources.md)]

> **Megjegyzések:**  
> 
> * Ahhoz, hogy a Power BI helyszíni adatforrásokhoz kapcsolódhasson és frissíthesse az adatkészletet telepítve kell lennie és futnia kell egy átjárónak.
> * Az Excel 2013 használatakor győződjön meg róla, hogy frissítette-e a Power Queryt a legújabb verzióra.
> * A frissítés nem támogatott azokból az Excel-munkafüzetekből, amelyeket olyan helyi meghajtóról importáltak, ahol az adatok csak munkafüzetekben vagy kapcsolt táblákban léteznek. A OneDrive-on tárolt és onnan importált munkafüzetek adatainak frissítése támogatott. További információért lásd: [A OneDrive-on vagy a SharePoint Online-ban található Excel-munkafüzetből létrehozott adatkészlet frissítése](refresh-excel-file-onedrive.md).
> * Amikor helyi meghajtóról importált Excel-munkafüzetből létrehozott adatkészletet frissít, csak az adatforrásokból lekérdezett adatok frissülnek. Ha módosítja az adatszerkezetet az Excelben vagy a Power Pivotban, például létrehoz egy új mértéket, vagy megváltoztatja egy oszlop nevét, ezek a módosítások nem másolódnak át az adatkészletbe. Ha ilyen módosításokat végez, akkor újra fel kell töltenie vagy újra közzé kell tennie a munkafüzetet. Ha várhatóan rendszeresen módosítja a munkafüzet szerkezetét, és szeretné, ha ezek a módosítások tükröződnének a Power BI adatkészletében anélkül, hogy újra fel kellene azokat tölteni, fontolja meg a munkafüzet OneDrive-ra való áthelyezését. A Power BI automatikusan frissíti a OneDrive-ról importált és tárolt munkafüzetek szerkezetét és munkalapadatait.
> 
> 

## <a name="how-do-i-make-sure-data-is-loaded-to-the-excel-data-model"></a>Hogyan ellenőrizhetem, hogy betöltődtek-e az adatok az Excel-adatmodellbe?
Ha a Power Queryt (az Excel 2016-ban Adatok beolvasása és átalakítása) használja, hogy egy adatforráshoz kapcsolódjon, több lehetőség is a rendelkezésére áll ahová az adatokat betöltheti. Ahhoz, hogy biztosan betöltse az adatokat az adatmodellbe, válassza az **Adat felvétele az adatmodellbe** lehetőséget a **Betöltés a megadott helyre** párbeszédpanelen.

> [!NOTE]
> Az itt látható képeken az Excel 2016 látható.
> 
> 

A **Navigátorban** kattintson a **Betöltés a megadott helyre...** menüpontra.  
    ![](media/refresh-excel-file-local-drive/refresh_loadtodm_1.png)

Vagy, ha a **Szerkesztés** elemre kattint a Navigátorban, megnyílik a Lekérdezésszerkesztő. Itt rákattinthat a **Bezárás és betöltés adott helyre...** menüpontra.  
    ![](media/refresh-excel-file-local-drive/refresh_loadtodm_2.png)

Ekkor ne felejtse el bejelölni a **Betöltés a megadott helyre** párbeszédpanelen az **Adat felvétele az adatmodellbe** jelölőnégyzetet.  
    ![](media/refresh-excel-file-local-drive/refresh_loadtodm_3.png)

### <a name="what-if-i-use-get-external-data-in-power-pivot"></a>Mi történik, ha a Power Pivotban használom a Külső adatok beolvasása lehetőséget?
Ezt is megteheti. Ha bármikor a Power Pivotot használja helyszíni vagy online adatforráshoz való kapcsolódásra és az adatok lekérdezésére, az adatok automatikusan betöltődnek az adatmodellbe.

## <a name="how-do-i-schedule-refresh"></a>Hogyan ütemezhetek frissítést?
Ha frissítési ütemezést állít be, a Power BI közvetlenül az adatforrásokhoz csatlakozik az adatkészletben található kapcsolati adatokkal és hitelesítő adatokkal a frissített adatok lekérdezéséhez, majd betölti a frissített adatokat az adatkészletbe. A Power BI szolgáltatásban az ezen az adatkészleten alapuló vizualizációk a jelentésekben és irányítópultokon szintén frissülnek.

Az ütemezett frissítés beállításáról részletesen lásd: [Ütemezett frissítés beállítása](refresh-scheduled-refresh.md).

## <a name="when-things-go-wrong"></a>Ha rosszul mennek a dolgok
Ha rosszul mennek a dolgok, az általában azért van, mert a Power BI nem tud bejelentkezni az adatforrásokba, vagy ha az adatkészlet helyszíni adatforráshoz csatlakozik, akkor nem érhető el az átjáró. Győződjön meg róla, hogy a Power BI be tud jelentkezni az adatforrásokba. Ha megváltozik az adatforrásba való bejelentkezésre használt jelszó, vagy a Power BI-t kijelentkezteti egy adatforrás, próbáljon újra bejelentkezni az adatforrásokba az Adatforrás azonosító adatai használatával.

Hagyja bejelölve az **Értesítést kérek e-mailben, ha sikertelen a frissítés** jelelölőnégyzetet. Hasznos, ha azonnal tudomást szerez róla, ha egy ütemezett frissítés nem sikerül.

>[!IMPORTANT]
>A Power Pivothoz csatlakozó és onnan lekérdezett OData-csatornák frissítése nem támogatott. Ha OData-csatornát használ adatforrásként, használja a Power Queryt.

## <a name="troubleshooting"></a>Hibaelhárítás
Néha előfordulhat, hogy az adatok frissítése nem a várt módon történik. Ez általában az átjáróval kapcsolatos probléma. Vessen egy pillantást az átjáró hibaelhárításával foglalkozó cikkekre, amelyekben eszközöket talál és ismert problémákkal találkozhat.

[A helyszíni adatátjáró hibaelhárítása](service-gateway-onprem-tshoot.md)

[A Power BI Gateway – Personal hibáinak elhárítása](service-admin-troubleshooting-power-bi-personal-gateway.md)

## <a name="next-steps"></a>Következő lépések
További kérdései vannak? [Felteheti őket a Power BI-közösségnek](http://community.powerbi.com/)

