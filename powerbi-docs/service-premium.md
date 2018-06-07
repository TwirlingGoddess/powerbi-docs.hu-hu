---
title: Mit jelent a Power BI Premium?
description: A Power BI Premium dedikált kapacitást biztosít cége vagy csapata számára, így felhasználónkénti licencek vásárlása nélkül is megbízható teljesítményre számíthat nagyobb mennyiségű adat estén is.
author: mgblythe
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-admin
ms.topic: conceptual
ms.date: 02/05/2018
ms.author: mblythe
LocalizationGroup: Premium
ms.openlocfilehash: 980aa830e38e49613b54ad473ef23eb7eac78ed2
ms.sourcegitcommit: 80d6b45eb84243e801b60b9038b9bff77c30d5c8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2018
ms.locfileid: "34722793"
---
# <a name="power-bi-premium---what-is-it"></a>Mit jelent a Power BI Premium?
A Power BI Premium dedikált erőforrásokat biztosít cége vagy csapata számára a Power BI szolgáltatás futtatásához, megbízhatóbb teljesítményt biztosítva nagyobb mennyiségű adat kezeléséhez is. A Prémium szint lehetővé teszi a tartalom széles körű megosztását anélkül, hogy a megtekintők számára felhasználónkénti licenceket kellene vásárolnia.

A Power BI Premium előnyeit úgy használhatja ki, hogy a munkaterületeket Prémium szintű kapacitáshoz rendeli. A *Prémium szintű kapacitás* egy dedikált erőforrás a szervezet számára. Azok a munkaterületek, melyek nincsenek prémium szintű kapacitáshoz rendelve, egy megosztott kapacitásban fognak szerepelni.

A *Megosztott kapacitás* a Power BI megszokott felhasználási módja, amelyben a számítási feladatok olyan számítási erőforrásokon futnak, amelyek más felhasználókkal vannak megosztva. Megosztott kapacitás használata esetén az egyéni felhasználók tevékenysége bizonyos mértékben korlátozott az összes felhasználó részére biztosítandó felhasználói élmény érdekében.

[!INCLUDE [powerbi-premium-illustration](./includes/powerbi-premium-illustration.md)]

<iframe width="560" height="315" src="https://www.youtube.com/embed/lNQDkN0GXzU?rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

## <a name="capacity-tiers"></a>Kapacitásszintek
A Power BI-ban két típusú kapacitás létezik. Az egyik a Megosztott kapacitás, a másik a Power BI Prémium-kapacitás. Az alábbiakban áttekintheti a közöttük levő különbséget.

|  | Megosztott kapacitás | Power BI Prémium-kapacitás |
| --- | --- | --- |
| **Frissítési időköz** |8/nap |Nincs korlátozva |
| **Dedikált hardverrel elkülönítve** |![](media/service-premium/not-available.png "Nem érhető el") |![](media/service-premium/available.png "Elérhető") |
| ***Minden felhasználó*** **számára elérhető vállalati terjesztés** | | |
| Alkalmazások |![](media/service-premium/not-available.png "Nem érhető el") |![](media/service-premium/available.png "Elérhető")<sup>1</sup> |
| Beágyazott API-k és vezérlők |![](media/service-premium/not-available.png "Nem érhető el") |![](media/service-premium/available.png "Elérhető")<sup>2</sup> |
| **Power BI-jelentések helyszíni közzététele** |![](media/service-premium/not-available.png "Nem érhető el") |![](media/service-premium/available.png "Elérhető") |

*<sup>1</sup> A felhasználók szabadon használhatják az alkalmazásokat, így lehetőségük van többek között a tartalmak megtekintésére weben vagy mobileszközön, a Q&A használatára, gyors elemzések végrehajtására, a Cortana használatára, valamint az adatok CSV-be, Excel-be és PowerPointba exportálására. Pro-licenc szükséges az itt fel nem sorolt tevékenységekhez, például megosztott adatkészletekre épülő jelentések létrehozásához és az Excelben való elemezéshez. További információ a [Power BI ingyenes és Pro verziókban](service-free-vs-pro.md) elérhető funkciókról.*  
*<sup>2</sup> A Power BI Premium általános elérhetőségét követően további fejlesztések várhatók.*

### <a name="premium-capacity"></a>Prémium-kapacitás
A Power BI Prémium-kapacitás használatának megkezdéséhez hozzá kell rendelnie a munkaterületet a kapacitáshoz. Ha további információkra van szüksége a munkaterületek prémium szintű kapacitáshoz rendelésével kapcsolatban, tekintse meg a [Power BI Premium kezeléséről](service-admin-premium-manage.md) szóló cikket.

Ha egy munkaterülethez prémium szintű kapacitás tartozik, élvezheti a Power BI Premium csomag előnyeit.

* Ütemezett frissítések: Importált modellek esetén a frissítések száma korábban napi 8-ra volt korlátozva. Ez a korlát a Prémium munkaterületeken található adatkészleteknél magasabb. A DirectQueryhez tartozó ütemezett gyorsítótár-frissítési beállításokra ugyanakkor ez nem vonatkozik. Azok változatlanok maradnak, függetlenül attól, hogy megosztott vagy prémium szintű kapacitású munkaterülethez tartoznak-e.
* Elkülönítés dedikált hardverrel – A megosztott kapacitás természetéből adódóan a jelentések és irányítópultok teljesítményére hatással lehet a kapacitásban jelentkező egyéb számítási feladatok erőforrásokkal szemben támasztott igénye, noha ezt próbáljuk kivédeni. Ezzel szemben a Prémium szint sokkal egyenletesebb, megbízhatóbb teljesítményt nyújt annak köszönhetően, hogy a munkaterülethez tartozó számítási feladatokat elkülöníti a többi számítási feladattól.

Ha egy alkalmazás prémium szintű kapacitással van támogatva (azaz prémium szintű kapacitáshoz rendelt munkaterületről lett közzétéve), a közzétett alkalmazást a cég bármely felhasználója használhatja, függetlenül attól, hogy milyen licenccel rendelkeznek. Ez azt jelenti, hogy az ingyenes Power BI-licenccel rendelkező felhasználók is használhatják azokat a közzétett alkalmazásokat.

### <a name="shared-capacity"></a>Megosztott kapacitás
Alapértelmezés szerint a munkaterületek megosztott kapacitáshoz tartoznak. Ez a személyes, *Saját munkaterületek* és az alkalmazás-munkaterületek esetén is így van. A Megosztott kapacitás a Power BI megszokott felhasználási módja, amelyben a számítási feladatok olyan számítási erőforrásokon futnak, amelyek más felhasználókkal vannak megosztva.

<a name="premiumskus"/>

### <a name="premium-capacity-nodes"></a>Prémium szintű kapacitást használó csomópontok
A Power BI Premium csomópont-konfigurációkban különböző virtuálismag-kapacitások érhetők el. A konkrét termékváltozat-ajánlatokról és a költségekről a [Power BI díjszabása](https://powerbi.microsoft.com/pricing/) témakörben tájékozódhat. Itt egy [költségkalkulátor](https://powerbi.microsoft.com/calculator/) is elérhető. Ha további információra van szüksége a beágyazott elemzési kapacitások tervezésével kapcsolatban, tekintse át a [Planning a Power BI Enterprise Deployment](https://aka.ms/pbienterprisedeploy) (A Power BI vállalati bevezetésének a megtervezése) című tanulmányt.

* A P csomópontok beágyazott, illetve szolgáltatási környezetben is használhatók
* Az EM csomópontok csak beágyazott környezetekben használhatók
* EM1 és EM2 

>[!NOTE]
>A táblázatban szereplő hivatkozások csak az Office 365 globális rendszergazdái számára működnek megfelelően; mindenki más 404-es hibaüzenetet kap. 

| Kapacitáscsomópont | Összes virtuális mag<br/>*(Háttérrendszer + előtérrendszer)* | Háttérrendszeri virtuális magok | Előtérrendszeri virtuális magok | DirectQuery-/élő kapcsolat korlátai | Maximális oldalmegjelenítések óránként csúcsidőszakban | Elérhetőség |
| --- | --- | --- | --- | --- | --- | --- |
| [EM1 (havonta megújuló)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |1 virtuális mag |0,5 virtuális mag, 2,5 GB RAM |0,5 virtuális mag |Másodpercenként 3,75 |150-300 |Elérhető |
| [EM2 (havonta megújuló)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |2 virtuális mag |1 virtuális mag, 5 GB RAM |1 virtuális mag |Másodpercenként 7.5 |301-600 |Elérhető |
| [EM3 (havonta megújuló)](https://portal.office.com/SubscriptionDetails?OfferId=4004702D-749C-4F74-BF47-3048F1833780&adminportal=1) |4 virtuális mag |2 virtuális mag, 10 GB RAM |2 virtuális mag | |601-1200 |Elérhető |
| [P1](https://portal.office.com/SubscriptionDetails?OfferId=b3ec5615-cc11-48de-967d-8d79f7cb0af1&adminportal=1) |8 virtuális mag |4 virtuális mag, 25 GB RAM |4 virtuális mag |Másodpercenként 30 |1201-2400 |Elérhető ([havonta megújulóként](https://portal.office.com/SubscriptionDetails?OfferId=E4C8EDD3-74A1-4D42-A738-C647972FBE81&adminportal=1) is elérhető) |
| [P2](https://portal.office.com/SubscriptionDetails?OfferId=062F2AA7-B4BC-4B0E-980F-2072102D8605&adminportal=1) |16 virtuális mag |8 virtuális mag, 50 GB RAM |8 virtuális mag |Másodpercenként 60 |2401-4800 |Elérhető |
| [P3](https://portal.office.com/SubscriptionDetails?OfferId=40c7d673-375c-42a1-84ca-f993a524fed0&adminportal=1) |32 virtuális mag |16 virtuális mag, 100 GB RAM |16 virtuális mag |Másodpercenként 120 |4801-9600 |Elérhető |

* Az előtérrendszeri virtuális magokat használja a rendszer webes szolgáltatásokhoz, az irányítópultokhoz, a jelentés- és dokumentumkezeléshez, a hozzáférések kezeléséhez, az ütemezéshez, az API-khoz, a feltöltésekhez, és letöltésekhez és többnyire mindenhez, ami a felhasználói élmény részét képzi.
* A háttérrendszeri virtuális magokat a nagyobb erőforrásigényű feladatokhoz, például a lekérdezések feldolgozásához, a gyorsítótár kezeléséhez, R szerverek futtatásához, adatfrissítéshez, természetes nyelvi feldolgozásához, valós idejű adatcsatornákhoz és a jelentések és képek megjelenítéséhez használja. A háttérrendszeri virtuális magokkal bizonyos mennyiségű memóriát is fenntart. A megfelelő mennyiségű memória nagy adatmodellek esetén vagy akkor válik különösen fontossá, amikor nagy számú aktív adatkészlet kezelésére van szükség.

## <a name="power-bi-report-server"></a>Power BI jelentéskészítő kiszolgáló
A Power BI Premium szintű előfizetés keretében lehetőség van a Power BI jelentéskészítő kiszolgáló helyszíni futtatására is. Ha további információra van szüksége, tekintse át a [Power BI jelentéskészítő kiszolgáló használatának kezdő lépéseit](report-server/get-started.md).

## <a name="next-steps"></a>További lépések
[Power BI Premium – gyakori kérdések](service-premium-faq.md)  
[A Power BI Premium kiadásával kapcsolatos megjegyzések](service-premium-release-notes.md)  
[A Power BI Premium megvásárlása](service-admin-premium-purchase.md)  
[A Power BI prémium kezelése](service-admin-premium-manage.md)  
[Microsoft Power BI Premium-tanulmány](https://aka.ms/pbipremiumwhitepaper)  
[A Power BI vállalati bevezetésének megtervezése ‒ tanulmány](https://aka.ms/pbienterprisedeploy)  
[A Power BI felügyelete a cégnél](service-admin-administering-power-bi-in-your-organization.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](https://community.powerbi.com/)

