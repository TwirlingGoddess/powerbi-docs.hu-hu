---
title: "A Power BI jelentéskészítő kiszolgáló változásnaplója"
description: "Ez a változásnapló a Power BI jelentéskészítő kiszolgálóra vonatkozik, és minden kiadott buildhez felsorolja az új elemeket és hibajavításokat."
services: powerbi
documentationcenter: 
author: jtarquino
manager: jonhp
backup: maggies
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 12/11/2017
ms.author: tankas
ms.openlocfilehash: ced415662c2dc39b6491cb79d121f3cd77719fe4
ms.sourcegitcommit: be55922d7f43f458aea0160ec8fdfb1a0b5a0c00
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/12/2017
---
# <a name="changelog-for-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgáló változásnaplója

Ez a változásnapló a Power BI jelentéskészítő kiszolgálóra vonatkozik, és minden kiadott buildhez felsorolja az új elemeket és hibajavításokat.

Az új funkciókról az [A Power BI jelentéskészítő kiszolgáló újdonságai](whats-new.md) című cikkből tájékozódhat.

## <a name="october-2017"></a>2017. október

- **Power BI jelentéskészítő kiszolgáló**
    - *Verzió: 1.1.6551.5155 (Build 14.0.600.438), Kiadás dátuma: 2017. december 11.*
        - Hibajavítások
            - A frissítés után egyes Power BI Desktop-jelentések adatai nem menthetők.

    - *Verzió: 1.1.6530.30789 (Build 14.0.600.437), Kiadás dátuma: 2017. november 17.*
        - Hibajavítások
            - Hibajavítás az alapszintű hitelesítéshez 
            - Hibajavítás: A hétköznapok nem voltak kijelölhetők a Portál ütemezési oldalán az előfizetésekhez, gyorsítótár-frissítési tervekhez és előzmény-pillanatképekhez
            - Hibajavítás: Többoldalas jelentésekben (RDL) az olyan szövegmezőkben lévő kifejezéseknél, amelyeknek CanGrow tulajdonsága hamisra volt állítva, az értékek színe nem jelent meg, és a betűtípus nem volt megfelelő
            - Hibajavítás: Power BI-jelentésekben (PBIX) a jelmagyarázattal ellátott vonaldiagramok üres vizualizáció előállítását eredményezték

    - *Verzió: 1.1.6514.9163 (Build 14.0.600.434), Kiadás dátuma: 2017. november 1.*
        - Hibajavítások
            - Hibajavítás 500 MB-nál nagyobb PBIX-jelentések feltöltésének megbízhatósági problémáira
            - Hibajavítás 1 GB-nál nagyobb PBIX-jelentések adatbetöltési problémáira

    - *Verzió: 1.1.6513.3500 (Build 14.0.600.433), Kiadás dátuma: 2017. október 31.*
        - Funkciók
            - Beágyazott adatmodell-támogatás
            - Excel-munkafüzet megtekintése (az Office Online Server integráció engedélyezésével)
            - Ütemezett adatfrissítés (PBIX)
            - Közvetlen lekérdezés támogatása
            - Nagy fájlok támogatása (2 GB-ig)
            - Nyilvános REST API
            - Megosztott adatkészlet támogatása a Power BI Desktopban (oData szolgáltatáson keresztül)
            - URL-cím paraméter támogatása PBIX-fájlokhoz
            - Javított kisegítő lehetőségek

- **Power BI Desktop (a Power BI jelentéskészítő kiszolgálóra optimalizálva)**
    - *Verzió: 2.51.4885.1423 (2017. október), Kiadás dátuma: 2017. november 17.*
        - Hibajavítások
            - Hibajavítás: A 32 bites Power BI Desktop nem futott x86-os operációs rendszeren
            - Hibajavítás: A vízszintes rácsvonalak megjelenítése Power BI-jelentésekben (PBIX)
            - További kisebb hibajavítások

    - *Verzió: 2.51.4885.1041 (2017. október), Kiadás dátuma: 2017. október 31.*
        - Funkciók
            - A Power BI jelentéskészítő kiszolgálóval (2017. október) való kapcsolathoz szükséges módosításokat tartalmaz

## <a name="june-2017"></a>2017. június

- **Power BI jelentéskészítő kiszolgáló**
    - *Build 14.0.600.305, Kiadás dátuma: 2017. szeptember 19.*  
        - Hibajavítások
            - A [Bing Térképek webes vezérlőinek](https://msdn.microsoft.com/library/mt712542.aspx) frissítése a legújabb verzióra

    - *Build 14.0.600.301, Kiadás dátuma: 2017. július 11.*
        - Hibajavítások
            - A {{UserId}} címke a tárolt hitelesítő adatokra áll be a Power BI Reportsban a jelentést futtató felhasználó helyett
            - Bizonyos képek nem jelennek meg a Power BI jelentéskészítő kiszolgáló jelentéseiben
            - Power BI-jelentések nevét nem lehet megváltoztatni Power BI jelentéskészítő kiszolgálóban
            - Nem lehet egyedi vizualizációkat betölteni a Power BI-mobilalkalmazásban (a helyi gyorsítótár kiürítéséhez újra kell telepíteni a mobilalkalmazást)

    - *Build 14.0.600.271, Kiadás dátuma: 2017. június 12.*
        - Power BI jelentéskészítő kiszolgáló megjelenése

## <a name="next-steps"></a>További lépések

[Felhasználói kézikönyv](user-handbook-overview.md)  
[Rendszergazdai kézikönyv](admin-handbook-overview.md)  
[Rövid útmutató: A Power BI jelentéskészítő kiszolgáló telepítése](quickstart-install-report-server.md)  
[A Jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)