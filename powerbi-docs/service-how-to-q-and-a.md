---
title: "A Power BI Q&A használata"
description: "A Power BI Q&A használata"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
editor: 
tags: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/25/2017
ms.author: mihart
ms.openlocfilehash: a6736916a4bb2e94c1f5e1e3c3c3e5339cf990ec
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="how-to-use-power-bi-qa"></a>A Power BI Q&A használata
## <a name="ask-questions-of-your-data-using-natural-language"></a>Természetes nyelvi kérdések az adatokról
Kezdje a műveletet egy irányítópulttal. A Q&A kérdésmezőben természetes nyelvet használva tehet fel kérdéseket. A Q&A felismeri a beírt szavakat, és kitalálja, hogy hol (melyik adatkészletben) található meg a válasz. A Q&A a kérdés megfogalmazásában is segít automatikus kiegészítéssel, átfogalmazással és más szöveges és vizuális támogatással.

![](media/service-how-to-q-and-a/powerbi-qna.png)

A kérdésére adott válasz használható vizualizációként jelenik meg, és a kérdés módosításakor frissül.

A Q&A interaktív, és még szórakoztató is lehet. Az esetek többségében a kérdések újabbakhoz vezetnek, és érdekes, követésre érdemes utakat nyitnak meg. Figyelje meg, hogyan hoz létre Amanda vizualizációkat a Q&A-val, hogyan tárja fel ezeket a vizualizációkat, és rögzíti őket irányítópultokon.

> [!NOTE]
> A Q&A szolgáltatás a [Microsoft Power BI](mobile-apps-ios-qna.md) iOS rendszerű alkalmazásában iPadeken, iPhone-okon és iPod Touch eszközökön is rendelkezésre áll.
> 
> 

<iframe width="560" height="315" src="https://www.youtube.com/embed/qMf7OLJfCz8?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

## <a name="use-natural-language-to-ask-questions-about-your-data"></a>Kérdések feltétele az adatokkal kapcsolatban természetes nyelven
1. Vigye a kurzort a kérdésmező fölé. Még mielőtt gépelni kezdene, a Q&A egy új képernyőt nyit meg, amelyen javaslatokkal segít a kérdés megfogalmazásában.
   
   ![](media/service-how-to-q-and-a/powerbi-qna-cursor.png)  
   
   A lista tartalma:  
   a.  a már az irányítópulton rögzített [csempék](service-dashboard-tiles.md) létrehozásához használt kérdések, és  
   b.  a [kiinduló adatkészlet(ek)](service-get-data.md) tábláinak nevei.  
   
   Kiindulásként mindig választhatja ezen kérdések egyikét, míg a kérdés finomításával rá nem talál az Ön által keresett válaszra. Egy tábla nevét használva új kérdést is megfogalmazhat.
2. Válasszon a legördülő listából, vagy kezdje begépelni saját kérdését.  
   
   ![](media/service-how-to-q-and-a/powerbi-qna-list.png)
3. A kérdés beírása közben a Power BI Q&A kiválasztja a legjobb [vizualizációt](power-bi-visualization-types-for-reports-and-q-and-a.md) a válasz megjelenítéséhez. A kérdés módosítása közben a vizualizáció dinamikusan változik. A Q&A a kérdés megfogalmazásában is segít automatikus kiegészítéssel, a kérdés átfogalmazásával és más szöveges és vizuális támogatással.  
   ![](media/service-how-to-q-and-a/powerbi-qna-viz.png)
4. A kérdés begépelésekor a Power BI minden olyan adatkészletben keresi a választ, amelyhez csempe tartozik az irányítópulton.  Ha az összes csempe forrása az *A adatkészlet*, akkor a válaszok az *A adatkészletből* származnak.  Ha vannak az *A adatkészletből* és a *B adatkészletből* származó csempék is, akkor a Q&A a két adatkészletből keresi ki a legjobb választ.
   
   > [!TIP]
   > Ügyeljen rá, hogy ha az *A adatkészletnek* csak egy csempéje van, és eltávolítja azt az irányítópultról, akkor a Q&A többé nem fog hozzáférni az *A adatkészlethez*.
   > 
   > 
5. Ha elégedett az eredménnyel, [rögzítse a vizualizációt egy irányítópulton](service-dashboard-pin-tile-from-q-and-a.md) a jobb felső sarokban lévő gombostű ikon használatával. Ha az irányítópultot más osztotta meg Önnel, vagy egy alkalmazás része, akkor a rögzítésre nincs lehetősége.
   
   ![](media/service-how-to-q-and-a/pbi_qna_finish-typing-question.jpg)

### <a name="tell-qa-which-visualization-to-use"></a>Adja meg a Q&A-nak a használandó vizualizációt.
A Q&A-tól nem csak annyit kérhet, hogy az adatok beszéljenek magukért, azt is megadhatja, hogy hogyan jelenjenek meg. Elég a kérdés végét a "as a <visualization type>" ("mint ...") szöveggel kiegészíteni.  Erre példa a "show inventory volume by plant as a map" ("mutasd a raktárkészletet üzemenként mint térkép") és a "show total inventory as a card" ("mutasd a teljes leltárt mint kártya").  Próbálja ki.

## <a name="how-does-qa-know-how-to-answer-questions"></a>Honnan tudja a Q&A, hogy hogyan válaszoljon meg egy kérdést?
### <a name="which-datasets-does-qa-use"></a>Melyik adatkészleteket használja a Q&A?
Honnan tudja a Q&A, hogy hogyan válaszoljon meg egy adott adatokra vonatkozó kérdést? Az alapul szolgáló adatkészlet tábláinak, oszlopainak és számított mezőinek nevére támaszkodik. Éppen ezért fontos, hogy Ön (vagy az adatkészlet tulajdonosa) mit minek nevez el! 

Például egy “Eladások” nevű Excel-táblázatban, amelynek “Termék”, “Hónap”, “Eladott mennyiség”, “Bruttó bevétel” és “Nyereség” nevű oszlopai vannak, Ön kérdéseket tehet fel ezek bármelyikével kapcsolatban.  Kérheti az *eladások* és az összes *nyereség* *havonkénti* kimutatását, a *termékek* *eladott mennyiség* szerinti rendezését és sok minden mást.

A Q&A az adatkészlet felépítésén alapuló kérdésekre képes választ adni. Hogyan működne ez Salesforce-adatok esetén? Amikor Ön a salesforce.com-fiókjához kapcsolódik, a Power BI automatikusan létrehoz egy irányítópultot.  Mielőtt elkezdene kérdéseket feltenni a Q&A-val, vessen egy pillantást az irányítópult vizualizációin és a Q&A legördülő menüjében látható adatokra.

* Ha a vizualizáció tengelyfeliratai és értékei között szerepelnek a "sales", "account", "month" és "opportunity" szavak, akkor feltehet olyan angol nyelvű kérdéseket, mint hogy "Which *account* has the highest *opportunity*", vagy "show *sales* by month as a bar chart".
* Ha a legördülő listában szerepelnek a "salesperson", "state", és "year" szavak, akkor bizonyára választ kap a "which *salesperson* had the lowest *sales* in *Florida* in *2013*" angol nyelvű kérdésre.

Ha egy webhely Google Analytics-beli teljesítményadatairól van szó, akkor kérdezheti a Q&A-t a weboldalakon töltött időről, az egyedi látogatások számáról és a felhasználói érdeklődés mérőszámairól. Demográfiai adatok lekérdezésekor például az életkor és a háztartások bevétele földrajzi hely szerinti eloszlásáról tehet fel kérdéseket.

### <a name="which-visualization-does-qa-use"></a>Mely vizualizációkat használja a Q&A?
A Q&A az éppen megjelenített adatok alapján választja ki a legalkalmasabb vizualizációt. Az alapul szolgáló adatkészlet(ek) adatai egy bizonyos típusba vagy kategóriába vannak besorolva, ami segít a Q&A-nak eldönteni, hogy hogyan jelenítse meg. Ha az adat például dátum típusúként van megadva, akkor nagyobb valószínűséggel jelenik meg vonaldiagramként. Városként kategorizált adatok nagyobb valószínűséggel lesznek térképen megjelenítve.

Utasíthatja is a Q&A-t, hogy melyik vizualizációt használja, ha hozzáfűzi azt a kérdéséhez. Azt azonban mindig vegye figyelembe, hogy a Q&A nem mindig tudja a kért vizualizációtípusban megjeleníteni az adatokat.

A Q&A által felismert kulcsszavakról a [Tippek kérdések feltevéséhez](service-q-and-a-tips.md) című cikkben talál információt.

## <a name="next-steps"></a>További lépések
Vissza a [Q&A a Power BI-ban](service-q-and-a.md) című témakörhöz  
[Oktatóanyag: A Q&A használata a kiskereskedelmi értékesítési mintával](power-bi-visualization-introduction-to-q-and-a.md)  
[Tippek kérdések feltevéséhez a Q&A-ben](service-q-and-a-tips.md)  
[Munkafüzet előkészítése a Q&A használatához](service-prepare-data-for-q-and-a.md)  
[Csempe rögzítése az irányítópulton a Q&A-ból](service-dashboard-pin-tile-from-q-and-a.md)  

