---
title: Power BI vegyes valósághoz alkalmazás (előzetes verzió)
description: A Power BI vegyes valósághoz alkalmazásban megtekintheti az irányítópultjait és jelentéseit a virtuális világban vagy a környezetében elhelyezve.
services: powerbi
documentationcenter: ''
author: maggiesMSFT
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: ''
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: ''
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 03/13/2018
ms.author: maggies
ms.openlocfilehash: 4226973fa48470faf46db68509b05eb02d88c113
ms.sourcegitcommit: 00b4911ab5fbf4c2d5ffc000a3d95b3149909c28
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2018
---
# <a name="power-bi-for-mixed-reality-app-preview"></a>Power BI vegyes valósághoz alkalmazás (előzetes verzió)
A Power BI vegyes valósághoz alkalmazásban megtekintheti az irányítópultjait és jelentéseit a virtuális világban, vagy elhelyezheti őket igény szerint a környezetében. 

Az irányítópultok és jelentések megtekintéséhez töltse le a Power BI vegyes valósághoz alkalmazás előzetes verzióját a Windows Áruházból. A virtuális valóságban műveleteket végezhet velük, majd kiválaszthatja, melyeket szeretné elhelyezni. 

## <a name="two-views-windows-classic-and-holographic"></a>Két nézet: klasszikus Windows és holografikus Windows

A Power BI vegyes valósághoz alkalmazás a Windowsos Power BI mobilalkalmazáson alapul, amelyet további, a vegyes valóságra jellemző egyedi funkciókkal bővítettünk. A Power BI vegyes valósághoz alkalmazás indításakor a Power BI „klasszikus” Windows nézetét láthatja. Ebben a nézetben navigálhat az elérhető irányítópultok és jelentések között. Ha megtalálta a megfelelőt, a klasszikus nézetről a holografikus nézetre válthat. 


## <a name="windows-classic-view-basics"></a>A klasszikus Windows nézet alapjai

Ha még csak most ismerkedik a vegyes valósággal, ez a szakasz hasznos információkat nyújt. A vegyes valóságon alapuló alkalmazások eltérnek a számítógépes, táblagépes vagy telefonos alkalmazásoktól. A klasszikus Windows nézetben a vegyes valóságon alapuló alkalmazások olyan mozdulatokra és hangparancsokra reagálnak, amelyek a hagyományos egér- és billentyűzetparancsok, illetve a telefonos koppintás helyett használhatók. 

**Légi koppintás**

A levegőben végzett koppintás a legalapvetőbb mozdulat, amelyre szüksége lesz a vegyes valóságon alapuló alkalmazásokhoz. Ehhez koppintsa össze felemelt kézzel a hüvelyk- és mutatóujját, mintha egy egérrel kattintana vagy a telefonján koppintana.  

![Légi koppintás a vegyes valóságban](media/mobile-mixed-reality-app/power-bi-hololens-airtap.png)

A klasszikus Windowsos Power BI-ban minden kattintásos funkció helyett használhatja a légi koppintást. A légi koppintással megnyithat irányítópultokat és jelentéseket a munkaterületen, vagy egy vizualizáció egyik részére koppinthat, amellyel szűrést vagy keresztkijelölést végezhet, és még számos más műveletre használhatja.

![Légi koppintás a Power BI szolgáltatásban](media/mobile-mixed-reality-app/power-bi-hololens-airtap-hand.png) 

További információ a [Microsoft vegyes valóságban használható kézmozdulatairól](https://developer.microsoft.com/windows/mixed-reality/gestures).

**Elem rögzítése** 

Koppintson a levegőben a **rajzszög** ikonra ![rajzszög ikon](media/mobile-mixed-reality-app/power-bi-hololens-pin.png) egy irányítópult vagy jelentés a klasszikus Windows nézetből a holografikus nézetbe való rögzítéséhez. A holografikus nézetben számos elemet rögzíthet. 

**Váltás a holografikus nézetre**

Miután rögzített egy elemet a klasszikus Windows nézetben, légi koppintással válassza a **teljes képernyő** ikont ![teljes képernyő ikon](media/mobile-mixed-reality-app/power-bi-hololens-fullscreen.png) a holografikus nézetre váltáshoz. 


## <a name="holographic-view-basics"></a>A holografikus nézet alapjai

A holografikus nézetben a rögzített összetevők a rögzítősávon jelennek meg. Ezeket a rögzített elemeket konkrét, valós térbeli elemeken helyezheti el, például amellett a berendezés mellett, amelyet az elem ismertet. Holografikus nézetben a kézmozdulatok mellett hangparancsokat is használhat. Az alábbiakban bemutatunk néhány gyakori hangparancsot.

**„Follow me”** 

Megragad egy Power BI-összetevőt, így az a látómezeje közepén marad és követi a szeme mozgását, amíg el nem helyezi valahol.

**„Dock”** 

A „dock” paranccsal elhelyezhet egy Power BI-összetevőt a rögzítősávon, így az a látómezeje szélén, könnyen elérhető távolságban követi Önt.

**„Place here”**

Ez a parancs egy falon vagy tárgyon, esetleg a levegőben lebegve helyez el egy irányítópultot vagy tárgyat.

![Irányítópult elhelyezése a levegőben](media/mobile-mixed-reality-app/power-bi-hololens-place-visuals.png)

**„Go home”**

A „Go home” kifejezést kimondva visszatérhet a Power BI klasszikus Windows nézetébe. 

**„Remove”**

Ezzel a paranccsal eltávolíthat egy összetevőt a holografikus nézetből.

**„Remove all”** 

Ezzel a paranccsal eltávolíthatja az összes összetevőt a holografikus nézetből.


## <a name="scan-a-report-qr-code-in-holographic-view"></a>Egy jelentés QR-kódjának beolvasása holografikus nézetben

Az iPhone-os és Androidos [Power BI mobilalkalmazáshoz hasonlóan](mobile-apps-qr-code.md) holografikus nézetben is beolvashatja a jelentések QR-kódjait.

- Holografikus nézetben nézzen a QR-kódra. A Power BI megnyitja a kódhoz társított jelentést.

## <a name="limitations-and-considerations"></a>Korlátozások és szempontok

A holografikus nézet használatakor figyelembe kell venni néhány korlátozást és szempontot.

- A klasszikus Windows nézetben beállított keresztszűrések és kiemelések nem jelennek meg.
- A rögzített irányítópultokat és jelentéseket csak Ön látja. A megosztott munkamenetek jelenleg nem támogatottak.
- Az irányítópultok és a jelentések 45 másodpercenként, az adatok változásával frissülnek.


## <a name="next-steps"></a>Következő lépések

- [A való világból származó Power BI-adatok mobilalkalmazásokkal](mobile-apps-data-in-real-world-context.md)

 



