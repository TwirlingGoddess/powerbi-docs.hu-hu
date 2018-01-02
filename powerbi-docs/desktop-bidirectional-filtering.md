---
title: "Kétirányú keresztszűrés a Power BI Desktopban (előzetes verzió)"
description: "Keresztszűrés engedélyezése a DirectQuery használatával a Power BI Desktopban"
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
ms.openlocfilehash: 7946a9389897c4401e581482c0630547a764616d
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/15/2017
---
# <a name="bidirectional-cross-filtering-using-directquery-in-power-bi-desktop-preview"></a>Kétirányú keresztszűrés a DirectQuery használatával a Power BI Desktopban (előzetes verzió)

Amikor táblák szűrését alkalmazzuk a megfelelő adatnézetek létrehozásához, a jelentéskészítők (és adatmodellezők) különböző kihívásokkal találkoznak, amikor el kell dönteniük, hogy milyen szűrést alkalmazzanak egy jelentésen. A táblák szűrőkontextusa a kapcsolatok egyik oldalán megmarad, de a másikon nem, így gyakran összetett DAX-képletek szükségesek a kívánt eredmények eléréséhez.

A kétirányú keresztszűrésnek köszönhetően a jelentéskészítők (és adatmodellezők) jobban tudják szabályozni a szűrők alkalmazását a kapcsolódó táblák használatakor, mivel engedélyezhetik a szűrők alkalmazását a táblakapcsolatok *mindkét* oldalán. Ezt úgy érik el, hogy a szűrő kontextusát propagálják egy másik kapcsolódó táblára egy táblakapcsolat másik oldalán.

Egy [részletes tanulmány](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) ismerteti a Power BI Desktopban elérhető kétirányú keresztszűrést (valamint az SQL Server Analysis Services 2016 működését, amely ugyanígy viselkedik).

* A [Power BI Desktopban használható kétirányú keresztszűrést ismertető](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) tanulmány letöltése

### <a name="enabling-bidirectional-cross-filtering-for-directquery"></a>Kétirányú keresztszűrés engedélyezése DirectQueryhez
A DirectQuery keresztszűrését először engedélyezni kell, hogy használni lehessen. Ez egy előzetes verziójú funkció, ami azt jelenti, hogy a rendelkezésre állása és viselkedése a Power BI Desktop későbbi kiadásaiban változhat.

A Power BI Desktopban a DirectQuery keresztszűrésének engedélyezéséhez kattintson a **Fájl > Lehetőségek és beállítások > Beállítások** elemre, majd jelölje be a **Kétirányú keresztszűrés engedélyezése a DirectQueryben** lehetőséget, ahogy az a következő képen látható.

![](media/desktop-bidirectional-filtering/bidirectional-filtering_1.png)

> [!NOTE]
> A Power BI Desktopban a keresztszűrési DAX-képletek létrehozásakor használja a *UserPrincipalName* paramétert (ami általában ugyanaz, mint a felhasználó bejelentkezési neve, például *joe@contoso.com*) a *UserName* helyett. Ehhez lehet, hogy létre kell hozni egy kapcsolódó táblát, amely egymáshoz rendeli a *UserName* (vagy például EmployeeID) és a *UserPrincipleName* paramétereket.
> 
> 

A keresztszűrés engedélyezéséhez egy kapcsolat **Kapcsolat szerkesztése** párbeszédpaneljén a következőket kell választani:

* A **Szűrő irányának keresztezése** beállításnál a **Mindkettő** értéket kell beállítani
* Emellett ki kell választani a **Biztonsági szűrők alkalmazása mindkét irányba** lehetőséget
  
  ![](media/desktop-bidirectional-filtering/bidirectional-filtering_2.png)

További információkért és a kétirányú keresztszűrés működési példáiért tekintse át a jelen cikkben korábban említett [tanulmányt](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx).

