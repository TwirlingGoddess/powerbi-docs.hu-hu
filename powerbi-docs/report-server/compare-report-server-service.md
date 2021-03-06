---
title: A Power BI jelentéskészítő kiszolgáló és a Power BI szolgáltatás összehasonlítása
description: Ez a cikk a Power BI jelentéskészítő kiszolgáló és a Power BI szolgáltatás funkcióit hasonlítja össze.
keywords: ''
author: maggiesMSFT
ms.author: maggies
ms.date: 05/07/2018
ms.topic: overview
ms.service: powerbi
ms.component: powerbi-report-server
manager: kfile
ms.custom: mvc
ms.openlocfilehash: f78638097ea33f9954f3db78c117f1935a68530b
ms.sourcegitcommit: 52ac456bf2ac025b22ea634c28482f22e1cc19ac
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/10/2018
ms.locfileid: "48908531"
---
# <a name="comparing-power-bi-report-server-and-the-power-bi-service"></a>A Power BI jelentéskészítő kiszolgáló és a Power BI szolgáltatás összehasonlítása

A Power BI jelentéskészítő kiszolgálónak és a Power BI szolgáltatásnak sok hasonló és néhány jelentősen eltérő tulajdonsága van. Ez a táblázat ezeket mutatja be.

| Funkciók | Power BI jelentéskészítő kiszolgáló | A Power BI szolgáltatás | Megjegyzések
|---------|---------|---------|---------|
| Telepítés | Helyszíni vagy üzemeltetett felhőbeli | Felhőbeli | A Power BI jelentéskészítő kiszolgáló akkor helyezhető üzembe Azure-beli virtuális gépeken (üzemeltetett felhőbeli) ha licencelése a Power BI Premiummal történt
| Forrásadatok | Felhőbeli és/vagy helyszíni | Felhőbeli és/vagy helyszíni |  
| Licenc | Power BI Premium vagy SQL Server EE SA-val | Power BI Pro és/vagy Power BI Premium |  
| Életciklus | Modern életciklus-szabályzat | Teljes körűen felügyelt szolgáltatás |  
| Kiadási ciklus | 4 havonta | Havonta | A legújabb funkciók és javítások először a Power BI szolgáltatáshoz jelennek meg. Az alapfunkciók többsége a következő néhány kiadásban jelenik meg a Power BI jelentéskészítő kiszolgálóhoz; bizonyos funkciók csak a Power BI szolgáltatáshoz készülnek.
| Power BI-jelentések létrehozása a Power BI Desktopban | Igen | Igen |  
| Power BI-jelentések létrehozása a böngészőben | Nem | Igen |  
| Átjáró szükséges | Nem | Helyszíni adatforrásokhoz igen |  
| Valós idejű streamelés | Nem | Igen | [Valós idejű streamelés a Power BI-ban](../service-real-time-streaming.md)
| Irányítópultok | Nem | Igen | [Irányítópultok a Power BI szolgáltatásban](../consumer/end-user-dashboards.md) 
| Jelentéscsoportok terjesztése alkalmazások használatával | Nem | Igen | [Irányítópultokat és jelentéseket tartalmazó alkalmazások létrehozása és közzététele](../service-create-distribute-apps.md) 
| Tartalomcsomagok | Nem | Igen | [Céges tartalomcsomagok: bevezetés](../service-organizational-content-pack-introduction.md) 
| Csatlakozás olyan szolgáltatásokhoz, mint a Salesforce | Nem | Igen | [Csatlakozás a használt szolgáltatásokhoz](../consumer/end-user-connect-to-services.md) a Power BI szolgáltatással
| Q&A | Nem | Igen | [A Q&A a Power BI szolgáltatásban és a Power BI Desktopban](../consumer/end-user-q-and-a.md) 
| Gyors elemzések | Nem | Igen | [Adatelemzések automatikus generálása a Power BI-jal](../consumer/end-user-insights.md) 
| Elemzés az Excelben | Nem | Igen | [Elemzés az Excelben](../service-analyze-in-excel.md) 
| Oldalakra osztott jelentések | Igen | Nem | Többoldalas jelentések a Power BI szolgáltatásban nem elérhetők, de [többoldalasjelentés-elemek rögzíthetők a Power BI irányítópultokon](https://docs.microsoft.com/sql/reporting-services/pin-reporting-services-items-to-power-bi-dashboards)
| Power BI – mobilalkalmazások | Igen | Igen | [Power BI-mobilalkalmazások áttekintése](../consumer/mobile/mobile-apps-for-mobile-devices.md) 
| ArcGIS-térképek | Nem | Igen | [Esri ArcGIS-térképek a Power BI szolgáltatásban és a Power BI Desktopban](../power-bi-visualization-arcgis.md)
| E-mail-előfizetés Power BI-jelentésekre | Nem | Igen | [Feliratkozás jelentésre vagy irányítópultra](../consumer/end-user-subscribe.md) a Power BI szolgáltatásban 
| E-mail-előfizetés többoldalas jelentésekre | Igen | Nem | [E-mail-kézbesítés a jelentéskészítő szolgáltatásban](https://docs.microsoft.com/sql/reporting-services/subscriptions/e-mail-delivery-in-reporting-services)  
| Adatriasztások | Nem | Igen | [Adatriasztások](../service-set-data-alerts.md) a Power BI szolgáltatásban
| Sorszintű biztonság | DirectQuery-módban csak adatforráson keresztül | Elérhető DirectQuery- (adatforrással) és Import-módban is | [Sorszintű biztonság (RLS)](../service-admin-rls.md) a Power BI-ban 
| Teljes képernyős mód | Nem | Igen | [Teljes képernyős mód](../service-fullscreen-mode.md) a Power BI szolgáltatásban 
| Fejlett Office 365-együttműködés | Nem | Igen | [Együttműködés egy alkalmazás-munkaterületen](../service-collaborate-power-bi-workspace.md) az Office 365 használatával 
| R vizualizációk | Nem | Igen | [R-vizualizációk létrehozása](../visuals/service-r-visuals.md) a Power BI szolgáltatásban  
| Előzetes verziójú funkciók | Nem | Igen | [Feliratkozás a Power BI szolgáltatás előzetes verziójú](../consumer/end-user-preview-features.md) funkcióira 
| Egyéni vizualizációk | Igen | Igen | [Egyéni vizualizációk a Power BI-ban](../power-bi-custom-visuals.md) 
| Power BI Desktop | A Jelentéskészítő kiszolgálóhoz optimalizált verzió a Jelentéskészítő kiszolgálóval letölthető | A Power BI szolgáltatáshoz optimalizált verzió elérhető a Windows Áruházban | [Power BI Desktop a jelentéskészítő kiszolgálóhoz](https://powerbi.microsoft.com/report-server/) <br><br> [Power BI Desktop a Power BI szolgáltatáshoz](http://aka.ms/pbidesktopstore)

## <a name="next-steps"></a>Következő lépések
[A Power BI jelentéskészítő kiszolgáló telepítése](install-report-server.md)  



