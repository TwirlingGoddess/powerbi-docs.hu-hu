---
title: A Power BI jelentéskészítő kiszolgáló változásnaplója
description: Ez a változásnapló a Power BI jelentéskészítő kiszolgálóra vonatkozik, és minden kiadott buildhez felsorolja az új elemeket és hibajavításokat.
author: jtarquino
manager: kfile
ms.reviewer: maggies
ms.service: powerbi
ms.component: powerbi-report-server
ms.topic: conceptual
ms.date: 03/31/2018
ms.author: jtarquino
ms.openlocfilehash: bfc9b054f9a34757361bf4ab1803aa6904471167
ms.sourcegitcommit: fb29c4bf7e598f962b453ac68091ca2189d6ae3b
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/31/2018
ms.locfileid: "43380313"
---
# <a name="changelog-for-power-bi-report-server"></a>A Power BI jelentéskészítő kiszolgáló változásnaplója

Ez a változásnapló a Power BI jelentéskészítő kiszolgálóra vonatkozik, és minden kiadott buildhez felsorolja az új elemeket és hibajavításokat.

Az új funkciókról az [A Power BI jelentéskészítő kiszolgáló újdonságai](whats-new.md) című cikkből tájékozódhat. 

## <a name="august-2018"></a>2018. augusztus
- **Power BI jelentéskészítő kiszolgáló**
    - *Verzió: 1.3.6816.37243 (Build 15.0.2.557), Kiadás dátuma: 2018. augusztus 30.*
        - Hibajavítások
            - Javítva lett egy probléma, ha a kiszolgáló a PBI jelentéskészítő kiszolgáló egy régebbi verziójáról lett frissítve, és a kötés átirányítási URL-címe nem frissült, az ügyfél a következőt látta:      
            *`
            Failed to load expression host assembly. Details: Could not load file or assembly 'Microsoft.ReportingServices.ProcessingObjectModel, Version=2018.7.0.0, Culture=neutral, PublicKeyToken=89845dcd8080cc91' or one of its dependencies. The located assembly's manifest definition does not match the assembly reference. (Exception from HRESULT: 0x80131040) (rsErrorLoadingExprHostAssembly)
             `*
             
            - Az adatfelirat átlátszósági hibája már ki van javítva.
            
    - *Verzió: 1.3.6801.38816 (Build 15.0.2.540), Kiadás dátuma: 2018. augusztus 15.*
        - Funkciók
            - Már elérhető a Power BI-jelentésekhez a SAP HANA SSO Direct Query Kerberosszal támogatása
            - Ebben a kiadásban megtalálható a Custom Visual API – 1.13.0-s verzió
            - Az egyéni vizualizációk visszaváltanak a kiszolgálói API jelenlegi verziójával kompatibilis előző verzióra (ha rendelkezésre áll)

- **Power BI Desktop (a Power BI jelentéskészítő kiszolgálóra optimalizálva)**
    - *Verzió: 2.61.5192.64 (2018. augusztus), kiadás dátuma: 2018. augusztus 15.*
        - A Power BI jelentéskészítő kiszolgálóval (2018. augusztus) való kapcsolathoz szükséges módosításokat tartalmaz         
        
## <a name="march-2018"></a>2018. március
- **Power BI jelentéskészítő kiszolgáló**
    - *Verzió: 1.2.6690.34729 (Build 15.0.2.402), Kiadás dátuma: 2018. április 27.*
        - Hibajavítások
            - Az SQL Server Reporting Services 2017-gyűjtemények migrálásának engedélyezése
            - Power BI-jelentések (PBIX)
                - A jelentéseket frissíteni lehet, ha a szerver egyéni hitelesítés használatára van konfigurálva
                - A jelentés tulajdonságainak módosítása nem állítja alaphelyzetbe az adatforrás hitelesítő adatait
            - Oldalakra osztott jelentések (RDL)
                - A `Lookup()` vagy más származtatott függvények (például a `LookupSet()` vagy a `MultiLookup()`) már nem `#Error` eredménnyel térnek vissza
                - A csatolt jelentések nyomtatáskor figyelembe veszik a céljelentés oldalméretét
                - Létrehozhatók feliratkozások hierarchikus paramétereket használó csatolt jelentésekre
                - A több értéket felvevő paraméterek alapértelmezett értékei módosíthatóak az IE11 használatakor
                - Az adatvezérelt feliratkozás-kézbesítési lehetőségek szerkeszthetők
                - A feliratkozások megnézhetők és szerkeszthetők a feliratkozás végrehajtása közben
                - Az adatforrás hitelesítő adatainak beállítása nem távolítja el a kifejezésalapú kapcsolati sztringeket
            - KPI-k
                - A trendvonalak frissülnek az adatok frissítésekor
            - Általános stabilitási fejlesztések

    - *Verzió: 1.2.6660.39920 (Build: 15.0.2.389), Kiadás dátuma: 2018. március 28.*
        - Hibajavítások
            - A Power BI-jelentéseknél (PBIX) javítás a Power BI-vizualizációkból indított nem működő adatexportáláshoz
            - A Power BI-jelentéseknél (PBIX) javítás a nem működő URL-szűrőkhöz
            - A többoldalas jelentéseknél (RDL) javítás az IE11-ben a Power BI jelentéskészítő kiszolgáló márciusi kiadására való frissítés után nem megfelelően megjelenő képekhez

    - *Verzió: 1.2.6648.38132 (Build: 15.0.2.378), Kiadás dátuma: 2018. március 19.*
        - Biztonsági frissítések
        - Javított kisegítő lehetőségek
        - Hibajavítások
            - Javítás a többoldalas jelentésekhez, melyekben a csatolt jelentés paramétereinek láthatósága hibásan működött a tulajdonságok szerkesztését követő visszaállítás után
            - Javítás az egyéni űrlapokkal hitelesítést végző webportálokhoz, melyek figyelmen kívül hagyták a csúszóablakos lejáratú cookie-kat
            - Javítás a Wordbe exportálási funkcióhoz, mely egyenetlen sormagasságot okozott az üres soroknál
            - Javítás a többoldalas jelentésekhez, melyekben a kifejezésalapú kapcsolati sztring törlődött az adatforrás hitelesítő adatainak módosításakor
            - Javítás a KPI-k szöveges értékekkel való használatához
            - Javítás a többoldalas jelentésekhez, melyekben nem működött az új adatkészlet társításának funkciója
            - Stabilitással és használattal kapcsolatos egyéb javítások

- **Power BI Desktop (a Power BI jelentéskészítő kiszolgálóra optimalizálva)**
    - Verzió: 2.56.5023.1043 (2018. március), Kiadás dátuma: 2018. március 19.
        - A Power BI jelentéskészítő kiszolgálóval (2018. március) való kapcsolathoz szükséges módosításokat tartalmaz

## <a name="october-2017"></a>2017. október

- **Power BI jelentéskészítő kiszolgáló**
    - *Verzió: 1.1.6582.41691 (Build 14.0.600.442), Kiadás dátuma: 2018. január 10.*
        - Biztonsági frissítések
        - Hibajavítások
            - Hibajavítás a Model.GetParameters 400-es hibakódjára
            - Hibajavítás megosztott adathalmazok meglévő többoldalas jelentésekhez való beállításához (RDL)
            - Hibajavítás a ExecutionNotFoundException hibához jelentés PDF-be exportálásánál különböző paraméterértékekkel

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
    - *Verzió: 2.51.4885.3981 (2017. október), Kiadás dátuma: 2018. április 10.*
        - Biztonsági frissítések

    - *Verzió: 2.51.4885.2501 (2017. október), Kiadás dátuma: 2018. január 10.*
        - Biztonsági frissítések

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
    - *Build 14.0.600.309, Kiadás dátuma: 2018. január 10.*
        - Biztonsági frissítések

    - *Build 14.0.600.305, Kiadás dátuma: 2017. szeptember 19.*  
        - Hibajavítások
            - A [Bing Térképek webes vezérlőinek](https://msdn.microsoft.com/library/mt712542.aspx) frissítése a legújabb verzióra

    - *Build 14.0.600.301, Kiadás dátuma: 2017. július 11.*
        - Hibajavítások
            - A `{{UserId}}` címke a tárolt hitelesítő adatokra áll be a Power BI Reportsban a jelentést futtató felhasználó helyett
            - Bizonyos képek nem jelennek meg a Power BI jelentéskészítő kiszolgáló jelentéseiben
            - Power BI-jelentések nevét nem lehet megváltoztatni Power BI jelentéskészítő kiszolgálóban
            - Nem lehet egyedi vizualizációkat betölteni a Power BI-mobilalkalmazásban (a helyi gyorsítótár kiürítéséhez újra kell telepíteni a mobilalkalmazást)

    - *Build 14.0.600.271, Kiadás dátuma: 2017. június 12.*
        - Power BI jelentéskészítő kiszolgáló megjelenése

- **Power BI Desktop (a Power BI jelentéskészítő kiszolgálóra optimalizálva)**
    - *Verzió: 2.47.4766.4901 (2017. június), Kiadás dátuma: 2018. január 10.*
        - Biztonsági frissítések

## <a name="next-steps"></a>Következő lépések

[A Power BI Jelentéskészítő kiszolgáló bemutatása](get-started.md)
[Rendszergazdai áttekintés](admin-handbook-overview.md)  
[A Power BI jelentéskészítő kiszolgáló telepítése](install-report-server.md)  
[A Jelentéskészítő telepítése](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[Az SQL Server Data Tools (SSDT) letöltése](http://go.microsoft.com/fwlink/?LinkID=616714)

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)
