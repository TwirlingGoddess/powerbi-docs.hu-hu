---
title: Csatlakozás a Zendeskhez a Power BI segítségével
description: Power BI Zendesk
author: SarinaJoan
manager: kfile
ms.reviewer: maggiesMSFT
ms.service: powerbi
ms.component: powerbi-service
ms.topic: conceptual
ms.date: 10/16/2017
ms.author: sarinas
LocalizationGroup: Connect to services
ms.openlocfilehash: afcaae9499aa1c7e1461030cfa6b5d7b35a47188
ms.sourcegitcommit: fbb7924603f8915d07b5e6fc8f4d0c7f70c1a1e1
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/02/2018
ms.locfileid: "37136019"
---
# <a name="connect-to-zendesk-with-power-bi"></a>Csatlakozás a Zendeskhez a Power BI segítségével
A Zendesk-tartalomcsomag egy Power BI-irányítópultot és néhány Power BI-jelentést kínál, amelyek hibajegyek és ügynöki teljesítmények elemzésében segítenek. Használhatja a kész irányítópultot és jelentéseket, vagy testre is szabhatja őket az Önnek legfontosabb információ kiemeléséhez.  Az adatok automatikusan frissülnek naponta egyszer. 

Csatlakozzon a [Zendesk-tartalomcsomaghoz](https://app.powerbi.com/getdata/services/zendesk), vagy olvasson még arról, hogy miképpen jön létre [a Zendesk integrációja](https://powerbi.microsoft.com/integrations/zendesk) a Power BI szolgáltatással.

>[!NOTE]
>A csatlakozáshoz Zendesk-rendszergazdai fiók szükséges. További információt a [követelményekről](#Requirements) lent talál.

## <a name="how-to-connect"></a>A kapcsolódás menete
1. A bal oldali navigációs ablaktábla alján kattintson az **Adatok lekérése** elemre.
   
   ![](media/service-connect-to-zendesk/pbi_getdata.png)
2. A **Szolgáltatások** mezőben válasza a **Beolvasás** elemet.
   
   ![](media/service-connect-to-zendesk/pbi_getservices.png) 
3. Válassza a **Zendesk** \> **Letöltés most** elemet.
   
   ![](media/service-connect-to-zendesk/zendesk.png)
4. Adja meg a fiókjához társított URL-címet. Ennek formátuma **https://company.zendesk.com**. A [paraméterek megkereséséről](#FindingParams) alább olvashat részletesebben.
   
   ![](media/service-connect-to-zendesk/pbi_zendeskconnect.png)
5. Amikor a rendszer kéri, adja meg Zendesk-fiókja hitelesítő adatait.  Válassza ki az **oAuth 2** hitelesítési mechanizmust, és kattintson a **Bejelentkezés** elemre. Kövesse a Zendesk hitelesítési folyamatát. (Ha már bejelentkezett a Zendeskbe a böngészőjében, akkor a rendszer nem feltétlenül kéri a hitelesítő adatait.)
   
   > [!NOTE]
   > Ez a tartalomcsomag megköveteli, hogy egy Zendesk-rendszergazdai fiókkal kapcsolódjon. 
   > 
   > 
   
   ![](media/service-connect-to-zendesk/pbi_zendesksignin.png)
6. Zendesk-adatai eléréséhez kattintson az **Engedélyezés** gombra.
   
   ![](media/service-connect-to-zendesk/zendesk2.jpg)
7. A **Csatlakozás** gombra kattintva indíthatja el az importálási folyamatot. Miután a Power BI importálta az adatokat, a bal oldali navigációs panelen megjelenik egy új irányítópult, egy új jelentés és egy új adatkészlet. Az új elemeket sárga csillag \* jelöli.
   
   ![](media/service-connect-to-zendesk/pbi_zendeskdash.png)

**Hogyan tovább?**

* [Kérdéseket tehet fel a Q&A mezőben](power-bi-q-and-a.md) az irányítópult tetején.
* [Módosíthatja az irányítópult csempéit](service-dashboard-edit-tile.md).
* [Kiválaszthatja valamelyik csempét](service-dashboard-tiles.md) a mögöttes jelentés megnyitásához.
* Noha az adatkészlet napi frissítésre van ütemezve, módosíthatja a frissítési ütemezést, vagy igény szerint frissíthet az **Azonnali frissítés** gombbal.

## <a name="whats-included"></a>A csomag tartalma
A Power BI-tartalomcsomag a következőkről tartalmaz adatokat:  

* Felhasználók (végfelhasználók és ügynökök)  
* Cégek  
* Csoportok  
* Hibajegyek  

Több mérték is kiszámítódik, többek között az Átlagos várakozási idő és az Utolsó 7 napban megoldott jegyek száma. A tartalomcsomag a teljes listát tartalmazza.

<a name="Requirements"></a>

## <a name="system-requirements"></a>Rendszerkövetelmények
A Zendesk-tartalomcsomaghoz való kapcsolódáshoz Zendesk-rendszergazdai fiók szükséges. Ha Ön ügynök vagy végfelhasználó, és szeretné megtekinteni Zendesk-adatait, akkor írja meg javaslatát, és értékelje a [Power BI Desktop](desktop-connect-to-data.md) Zendesk-összekötőjét.

<a name="FindingParams"></a>

## <a name="finding-parameters"></a>Paraméterek keresése
A Zendesk-URL-cím megegyezik azzal, amelyet a Zendesk-fiókjába való belépéshez használ. Ha nem biztos a Zendesk-URL-címében, használhatja a Zendesk [bejelentkezési súgóját](https://www.zendesk.com/login/).

## <a name="troubleshooting"></a>Hibaelhárítás
Ha a kapcsolódási problémába ütközik, ellenőrizze a Zendesk-URL-címét, és győződjön meg arról, hogy Zendesk-rendszergazdai fiókot használ.

## <a name="next-steps"></a>Következő lépések
* [Mi az a Power BI?](power-bi-overview.md)
* [Adatok lekérése](service-get-data.md)

