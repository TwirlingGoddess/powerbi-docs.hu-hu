---
title: "Egyéni vizualizációk áttekintése biztonsági és adatvédelmi szempontból"
description: "Az egyéni vizualizációk engedélyezése előtt át kell tekintenie a vizualizációt biztonsági és adatvédelmi szempontból, hogy biztosan megfeleljen a vállalat igényeinek."
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 09/05/2017
ms.author: maghan
ms.openlocfilehash: 15f8d9090736a62fdaa53aa3f19e7e0fff127337
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/30/2018
---
# <a name="review-custom-visuals-for-security-and-privacy"></a>Egyéni vizualizációk áttekintése biztonsági és adatvédelmi szempontból
Az egyéni vizualizációk engedélyezése előtt át kell tekintenie a vizualizációt biztonsági és adatvédelmi szempontból, hogy biztosan megfeleljen a vállalat igényeinek.

## <a name="enable-a-custom-visual"></a>Egyéni vizualizáció engedélyezése
<a name="enable"></a>A jelentésekben az egyéni vizualizációk le vannak tiltva, amíg ki nem választja az **Egyéni vizualizációk engedélyezése** lehetőséget az alábbiakban látható módon.  

![](media/service-custom-visuals-review-for-security-and-privacy/emptyvisual.png)

## <a name="considerations-before-you-enable-a-custom-visual"></a>Egyéni vizualizáció engedélyezése előtti szempontok
<a name="considerations"></a>

> [!WARNING]
> Az egyéni vizualizációk biztonsági vagy adatvédelmi kockázatot jelentő kódot tartalmazhatnak, ezért a jelentésekben lévő egyéni vizualizációk le vannak tiltva, amíg ki nem választja az Egyéni vizualizációk engedélyezése lehetőséget. Íme néhány szempont, amely segíthet az egyéni vizualizációk engedélyezésével kapcsolatos döntésben:
> 
> 

1. Győződjön meg arról, hogy a szerző és a jelentésben használt egyéni vizualizációk forrása megbízható.
2. Ha bizonytalan a döntésében, kérjen tanácsot az informatikai csapattól azzal kapcsolatban, hogy engedélyezze-e az egyéni vizualizációkat a megtekintett jelentésekhez.
3. Ha valaki egyéni vizualizációt tartalmazó jelentést oszt meg Önnel, nem kötelező engedélyeznie az egyéni vizualizációt még akkor sem, ha közeli munkatársak. Mindig érdemes megfontolni, hogy az egyéni vizualizáció engedélyezése elengedhetetlen-e az adott feladathoz. Mindig elfogadható arra kérni a küldőt, hogy egyéni vizualizációk nélkül küldje el a jelentést, ha nem biztos benne, hogy az egyéni vizualizáció nem jelent-e kockázatot.

## <a name="security-best-practices-for-it-professionals-to-enable-a-custom-visual"></a>Ajánlott biztonsági eljárások informatikai szakembereknek egyéni vizualizáció engedélyezéséhez
<a name="security"></a>

> [!WARNING]
> Az egyéni vizualizációk biztonsági vagy adatvédelmi kockázatot jelentő kódot tartalmazhatnak, ezért a jelentésekben lévő egyéni vizualizációk le vannak tiltva, amíg ki nem választja az Egyéni vizualizációk engedélyezése lehetőséget. Többféle ajánlott eljárás használható az egyéni vizualizációk biztonsági és adatvédelmi szempontból történő értékeléséhez.
> 
> 

1. Implementáljon átvizsgálási folyamatot az egyéni vizualizációkhoz a vállalatban. A megvizsgált egyéni vizualizációk egy belső webhelyen megoszthatók a belső felhasználókkal, például SharePoint-dokumentumtárban vagy OneNote-dokumentumban.
2. Nyújtson útmutatást az üzleti felhasználóknak az egyéni vizualizációk megfelelő használatáról és biztosítson egy e-mail-csoportot, amelyre elküldhetik a biztonsággal és az adatvédelemmel kapcsolatos kérdéseiket.
3. Értékelje ki a JavaScript-kódot az egyéni vizualizáció pbiviz-fájljában.

**A JavaScript-kód kiértékelése egyéni vizualizációkban**

Az egyéni vizualizációk JavaScriptet használnak, ezért biztonsági vagy adatvédelmi kockázatot jelenthetnek. Ha egyéni vizualizációt vagy egyéni vizualizációt tartalmazó pbix-fájlt kap ismeretlen forrásból, érdemes ellenőrizni, hogy biztonságos-e a JavaScript.

Az egyéni vizualizációkban lévő JavaScript-kód kiértékeléséhez csomagolja ki az egyéni vizualizáció kódját. A kódot a következő módon csomagolhatja ki:  

1. Mentse a .pbiviz fájlt egy mappába.
2. Nevezze át a fájlt .zip fájllá.
3. Csomagolja ki a zip-fájlt egy helyi mappába.

## <a name="custom-visual-file-contents"></a>Egyénivizualizáció-fájl tartalma
A pbiviz-fájlok a következőket tartalmazzák:

| **Fájl** | **Leírás** |
|:--- |:--- |
| ./package.json |Jegyzékfájl, amely jelzi, hogy mely fájlokat kell betölteni az egyéni vizualizációhoz. |
| ./resources |Az egyéni vizualizáció által használt CSS-t, TypeScriptet és JavaScriptet tartalmazza. |
| ./resources/&lt;név&gt; |A &lt;név&gt; az egyéni vizualizáció neve. |
| ./resources/&lt;név&gt;.css |Az egyéni vizualizáció css-erőforrásfájlja. |
| ./resources/&lt;név&gt;.js |Az a kód, amely akkor fut, amikor egy felhasználó az Egyéni vizualizációk engedélyezése gombra kattint vagy miután egy felhasználó egyéni vizualizációt importál. Figyelmeztetés: A JavaScript-kód biztonsági vagy adatvédelmi kockázatokat tartalmazhat. |
| ./resources/&lt;név&gt;.ts |A vizualizáció JavaScript-forráskódja TypeScript formátumban. Figyelmeztetés: A JavaScript- vagy TypeScript-kód biztonsági vagy adatvédelmi kockázatokat tartalmazhat. |
| ./resources/&lt;név&gt;.png |A felhasználó számára a vizualizációhoz megjelenő ikon. |

A pbiviz-fájl kicsomagolása után kiértékelheti a kódot. Íme néhány ajánlott eljárás és várható fenyegetés.

## <a name="best-practices-to-evaluate-the-javascript-or-typescript-code"></a>Ajánlott eljárások a JavaScript- vagy TypeScript-kódok kiértékeléséhez
A **JavaScript**- vagy **TypeScript**-kód biztonsági vagy adatvédelmi kockázatokat tartalmazhat. Íme néhány ajánlott eljárás és várható fenyegetés.

### <a name="best-practices-to-evaluate-javascript-code"></a>Ajánlott eljárások a JavaScript-kód kiértékeléséhez
* Mindig értékelje ki a .js fájl tartalmát. Ez az a kód, amely ténylegesen fut. Előfordulhat, hogy a .ts fájl tartalma nem az egyéni vizualizációban lévő .js fájlra fordul le.
* Mindig értékelje ki a .ts fájl tartalmát. A .ts fájlt betöltheti a **fejlesztői eszközökbe**, exportálhatja a vizualizációt, és összehasonlíthatja az újonnan létrehozott .pbiviz fájlban lévő, eredményül kapott .js fájlt a vizualizációban lévő eredeti .js fájllal.
* Ellenőrizze, hogy az egyéni vizualizáció ikonja nem hasonlít-e túlzottan a felhasználó által ismert más vizualizációkéhoz.
* Mindig olyan tesztfiókon értékelje ki a vizualizációt, amely minimális jogosultságokkal rendelkezik, és nem rendelkezik hozzáféréssel bizalmas adatokhoz. Ideális esetben a tesztfiók helyi fiók, amely csak a Power BI szolgáltatás bejelentkezési információival rendelkezik.

### <a name="threats-to-look-for-in-javascript-code"></a>A JavaScript-kódban keresendő fenyegetések
* Ellenőrizze a hálózati tevékenységet, amikor a vizualizációt szerkesztési és megtekintési módban is használja. Győződjön meg arról, hogy elégedett az elvégzett kérelmekkel. A Power BI tartományon kívüli erőforrások felé nem szerepelhetnek kérelmek, ha a vizualizáció készítője ezt előre nem közölte.
* A Power BI tartományt elhagyó minden adatnak meg kell felelnie az elvárt „normál” használatnak. Például ha a vizualizáció olyan videolejátszót implementál, amely iFrame használatával játszik le videót egy másik helyről, néhány adatot továbbítani kell az iFrame kérelmekben a videó megfelelő megjelenítése érdekében. Ha azonban a teljes adatkészlet továbbítva van, érdemes további vizsgálatokat végezni, hogy ez szükséges és kívánatos-e.
* Ellenőrizze, hogy az egyéni vizualizáció küld-e vagy tárol-e személyazonosításra alkalmas adatokat.
* Ellenőrizze, hogy az egyéni vizualizáció megpróbál-e elérni helyi géperőforrásokat, például próbál-e fájlokat lemezre írni vagy cookie-kat elérni.
* Ellenőrizze, hogy az egyéni vizualizáció tartalmaz-e bármit, ami rejtjelezett kódnak vagy egyértelmű cél nélküli kódnak tűnik.
* Mentse a korábban áttekintett összes vizualizáció másolatát.
* Ha korábban áttekintett vizualizáció frissítését tekinti át, ellenőrizze a változásokat. Mindig ugyanolyan alaposan tekintse át a vizualizációk frissítéseit, mint korábban magukat a vizualizációkat.
* Ha bármi gyanúsat vagy nem egyértelműt észlel, vegye fel velünk a kapcsolatot, örömmel állunk rendelkezésére.

## <a name="next-steps"></a>Következő lépések
[Vizualizációk a Power BI-ban](power-bi-report-visualizations.md)  
[Egyéni vizualizációk a Power BI-ban](power-bi-custom-visuals.md)  
[Egyéni vizualizációk közzététele az Office áruházban](developer/office-store.md)  
[Bevezetés az egyéni vizualizációk fejlesztői eszközeinek használatába](service-custom-visuals-getting-started-with-developer-tools.md)  
[Egyéni vizualizáció tanúsítása](power-bi-custom-visuals-certified.md)    
[Videó: Egyéni vizualizációk létrehozása a Power BI-hoz Sachin Patney és Nico Cristache segítségével](https://www.youtube.com/watch?v=kULc2VbwjCc)  

További kérdései vannak? [Forduljon a Power BI közösségéhez](http://community.powerbi.com/)

