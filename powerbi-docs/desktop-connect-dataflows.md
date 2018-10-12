---
title: Csatlakozás Power BI-adatfolyamok által létrehozott adatokhoz a Power BI Desktopban (előzetes verzió)
description: Egyszerű csatlakozás adatfolyamokhoz, és azok használata a Power BI Desktopban
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.component: powerbi-desktop
ms.topic: conceptual
ms.date: 09/10/2018
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: f3964b96f8f282772f6d511c9c412e0caabd1d00
ms.sourcegitcommit: c51461690e8faa121a1325957ca79b7a3975e8b8
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/12/2018
ms.locfileid: "44512911"
---
# <a name="connect-to-data-created-by-power-bi-dataflows-in-power-bi-desktop-preview"></a>Csatlakozás Power BI-adatfolyamok által létrehozott adatokhoz a Power BI Desktopban (előzetes verzió)
A **Power BI Desktopban** ugyanúgy csatlakozhat a **Power BI-adatfolyamok** által létrehozott adatokhoz, mint bármely más adatforráshoz.

![Csatlakozás adatfolyamokhoz](media/desktop-connect-dataflows/connect-dataflows_01.png)

A **Power BI-adatfolyamok (előzetes verzió)** összekötővel olyan entitásokhoz csatlakozhat, amelyeket adatfolyamok hoztak létre a Power BI szolgáltatásban. Mivel az adatfolyamok előzetes verzióban érhetők el, végre kell hajtania néhány lépést, hogy az adatfolyam-összekötő elérhető legyen a rendszerén. 


## <a name="download-and-enable-the-power-bi-dataflows-connector-preview"></a>A Power BI-adatfolyamok összekötő (előzetes verzió) letöltése és engedélyezése

Le kell töltenie a **Power BI-adatfolyamok** összekötőt, majd egy adott helyre kell bemásolnia a számítógépén. A Power BI Desktop következő havi frissítésével az összekötő automatikusan bekerül az adatösszekötők listájába. Ekkor ezek a lépések szükségtelenné válnak.

A **Power BI-adatfolyamok összekötő** a következő helyről tölthető le: [Power BI-adatfolyamok összekötő](https://visuals.azureedge.net/cds-analytics/PublicPreview/CDSA.mez)

A **Power BI-adatfolyamok** összekötő (előzetes verzió) az alábbi lépésekkel tehető elérhetővé a számítógépén:

1. Töltse le a .MEZ fájlt (az adatösszekötő fájlt). A privát előzetes verzióval rendelkező ügyfelek közvetlenül a Microsofttól kapnak tájékoztatást a .MEZ fájl letöltésével kapcsolatban.

2. Helyezze el a letöltött adatösszekötő fájlt a számítógépe következő mappájában: **Dokumentumok > Power BI Desktop > az egyéni összekötők mappája**

3. A Power BI Desktopban válassza a **Fájl > Lehetőségek és beállítások > Lehetőségek** menüpontot, majd a bal oldali panel **Előzetes funkciók** elemét.

    ![Egyéni összekötők engedélyezése](media/desktop-connect-dataflows/connect-dataflows_02.png)

4. Jelölje be az **Egyéni adatösszekötők** jelölőnégyzetet, ha nincs bejelölve. 

5. Az összekötő megjelenéséhez indítsa újra a **Power BI Desktopot**.

## <a name="use-the-power-bi-dataflows-connector-preview"></a>A Power BI-adatfolyamok összekötő (előzetes verzió) használata
A **Power BI Desktop** újraindítása után az összekötő elérhető adatforrásként jelenik meg. Adatkészlethez való csatlakozáshoz válassza az **Adatok betöltése > Online szolgáltatások > Power BI-adatfolyamok (bétaverzió)** lehetőséget, az alábbi ábrán látható módon:

![Csatlakozás adatfolyamokhoz](media/desktop-connect-dataflows/connect-dataflows_01.png)

## <a name="considerations-and-limitations"></a>Megfontolandó szempontok és korlátozások

A **Power BI-adatfolyamok összekötő** előzetes verziójának használatához a **Power BI Desktop** legújabb verzióját kell futtatnia. Bármikor [letöltheti a Power BI Desktopot](desktop-get-the-desktop.md), és telepítheti a számítógépére, hogy mindig a legújabb verzióval rendelkezzen.  

Megjegyzés: Amikor a Power BI-adatfolyamok összekötő megjelenik a **Power BI Desktop** következő havi frissítésében, az ütközések elkerülése érdekében *mindenképpen* törölnie kell ezt a letöltött .MEZ fájlt a **Dokumentumok > Power BI Desktop > egyéni összekötők** mappából. 


## <a name="next-steps"></a>Következő lépések
Power BI-adatkapcsolatokkal sok érdekes ötletet megvalósíthat. A **Power BI Desktopról** számos olyan cikk szól, amelyeket hasznosnak találhat:

* [Adatforrások a Power BI Desktopban](desktop-data-sources.md)
* [Adatok formázása és kombinálása a Power BI Desktoppal](desktop-shape-and-combine-data.md)
* [Adatok közvetlen bevitele a Power BI Desktopba](desktop-enter-data-directly-into-desktop.md)   

