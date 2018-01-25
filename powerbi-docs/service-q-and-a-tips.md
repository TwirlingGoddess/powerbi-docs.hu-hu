---
title: "Tippek és trükkök Q&A-kérdések feltevéséhez a Power BI-ban"
description: "Tippek és trükkök Q&A-kérdések feltevéséhez a Power BI-ban"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 01/18/2018
ms.author: jastru
ms.openlocfilehash: 5d9b65448fced78bf3eb4ed02c84e1561d2d209a
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/19/2018
---
# <a name="tips-for-asking-questions-in-power-bi-qa"></a>Tippek kérdések feltevéséhez a Power BI Q&A-ben
## <a name="words-and-terminology-that-qa-recognizes"></a>Szavak és kifejezések, amelyeket a Q&A felismer
A kulcsszavak listája nem teljes körű.  A legjobban úgy ellenőrizheti, hogy a Power BI felismer-e egy adott kulcsszót, hogy megpróbálja azt beírni a kérdésmezőbe.  Ha a szó vagy a kifejezés szürkén jelenik meg, a Power BI nem ismeri a kifejezést, vagy nem ismeri fel azt az aktuális környezetben.

Az alábbi lista jelen idejű kifejezéseket tartalmaz, de a rendszer a legtöbb esetben az összes igealakot felismeri. Például az angol nyelvű „is” ige magában foglalja a következő igealakokat is: are, was, were, will be, have, has, had, will have, has got, do, does, did.  A „sort” ige pedig magában foglalja a „sorted” és a „sorting” alakokat is.  A Power BI felismeri és magában foglalja a szavak többes és egyes számú verzióit. Például a Power BI felismeri a „year” és a „years” szavakat is.

> [!NOTE]
> A Q&A szolgáltatás a [Microsoft Power BI](mobile-apps-ios-qna.md) iOS rendszerű alkalmazásában iPadeken, iPhone-okon és iPod touch eszközökön is rendelkezésre áll.
> 
> 

Ha Ön a tulajdonosa egy adatkészletnek, különböző kifejezéseket és szinonimákat adhat hozzá, és fejlesztheti az ügyfelek által kapott Q&A-eredményeket.

**Összesítések**: total, sum, amount, number, quantity, count, average, most, least, fewest, largest, smallest, highest, biggest, maximum, max, greatest, lowest, littlest, minimum, min

**Névelők**: a, an, the

**Üres és logikai értékek**: blank, empty, null, „non” vagy „non-” előtaggal, empty string, empty text, true, t, false, f

**Összehasonlítások**: vs, versus, compared to, compared with

**Kötőszavak**: and, or, each of, with, versus, &, and, but, nor, along with, in addition to

**Összevonások**: a Q&A szinte minden összevonást felismer, próbálja csak ki.  Íme néhány angol nyelvű példa: didn’t, haven’t, he’d, he’s, isn’t, it’s, she’ll, they’d, weren’t, where’ll, who’s, won’t, wouldn’t.

**Dátumok**: a Power BI felismeri a legtöbb dátummal kapcsolatos angol nyelvű kifejezést (day, week, month, year, quarter, decade stb.), valamint a különböző formátumokban írt dátumokat is (lásd alább). A Power BI felismeri a következő kulcsszavakat: MonthName, Days 1-31, decade.

Angol nyelvű példák: January 3rd of 1995, January 3rd 1995, jan 03 1995, 3 Jan 1995, the 3rd of January, January 1995, 1995 January, 1995-01, 01/1995, hónapok nevei.

**Angol nyelvű relatív dátumok**: today, right now, current time, yesterday, tomorrow, the current, next, the coming, last, previous, ago, before now, sooner than, after, later than, from, at, on, from now, after now, in the future, past, last, previous, within, in, over, N days ago, N days from now, next, once, twice.

Angol nyelvű példa: count of orders in the past 6 days.

**Egyenlőség (tartomány)**: in, equal to, =, after, is more than, in, between, before

Angol nyelvű példák: Order year is before 2012? Price equals between 10 and 20? Is the age of John greater than 40? Total sales in 200-300?

**Egyenlőség (érték)**: is, equal, equal to, in, of, for, within, is in, is on

Angol nyelvű példák: Which products are green? Order date equals 2012. Is the age of John 40? Total sales that is not equal to 200? Order date of 1/1/2016. 10 in price? Green for color? 10 in price?

**Nevek**: Ha az adatkészlet egyik oszlopa tartalmazza a „name” (például EmployeeName) kifejezést, a Q&A megérti, hogy az oszlopértékek nevek, ezért fel lehet tenni például a következő angol nyelvű kérdést: „which employees are named robert”.

**Névmások**: he, him, himself, his, she, herself, her, hers, it, itself, its, they, their, them, themselves, theirs, this, these, that, those

**Lekérdezési parancsok**: sorted, sort by, direction, group, group by, by, show, list, display, give me, name, just, only, arrange, rank, compare, to, with, against, alphabetically, ascending, descending, order

**Tartomány**: greater, more, larger, above, over, >, less, smaller, fewer, below, under, <,  at least, no less than, >=, at most, no more than, <=, in, between, in the range of, from, later, earlier, sooner, after, on, at, later than, after, since, starting with, starting from, ending with

**Időszakok**: am, pm, o'clock, noon, midnight, hour, minute, second, hh:mm:ss

Angol nyelvű példák: 10 pm, 10:35 pm, 10:35:15 pm, 10 oclock, noon, midnight, hour, minute, second.

**Felső N** (rendezés, rangsorolás): top, bottom, highest, lowest, first, last, next, earliest, newest, oldest, latest, most recent, next

**Vizualizációs típusok**: a Power BI minden vizualizációs típust natívan támogat.  Ha a Megjelenítések ablaktábla egyik beállításáról van szó, szerepelhet a kérdésben.  A kivételt ez alól az [egyéni vizualizációk](power-bi-custom-visuals.md) képezik, amelyeket manuálisan vett fel a Megjelenítések ablaktáblán.

Angol nyelvű példa: show districts by month and sales total as bar chart

**Kérdőszavak (kapcsolat, minősített)**: when, where, which, who, whom, how many, how much, how many times, how often, how frequently, amount, number, quantity, how long, what

## <a name="qa-helps-you-phrase-the-question"></a>A Q&A segít megfogalmazni a kérdést
A Q&A mindent megtesz azért, hogy az adott kérdésre pontosan válaszoljon. Ezt többféle módon teszi. Az összes ilyen megoldás esetében a műveletet teljes mértékben, részletesen vagy egyáltalán nem lehet elfogadni. A kérdés beírásakor a Q&A az alábbiakat teszi:

* automatikusan kiegészíti a szavakat és a kérdéseket. Különböző stratégiákat használ, beleértve a felismerhető szavak, az alapul szolgáló munkafüzetekhez tartozó népszerű kérdések, valamint a korábban használt és érvényes válaszokat eredményező kérdések automatikus kiegészítését. Egynél több automatikus kiegészítés esetén a rendszer a lehetőségeket egy legördülő listában jeleníti meg.
* kijavítja a helyesírási hibákat.
* vizualizáció formájában jeleníti meg a válasz előnézetét. A vizualizáció a kérdés beírása és szerkesztése közben frissül (a rendszer nem várja meg, amíg a felhasználó lenyomja az Enter billentyűt).
* automatikusan helyettesítő kifejezéseket javasol a mögöttes adatkészlet(ek)ből, ha a felhasználó a kurzort a kérdésmezőbe helyezi.
* újrafogalmazza a kérdést a mögöttes adatkészlet(ek) adatai alapján. Ezzel elősegíti a Q&A számára a kérdés megértését, mivel a Q&A a használt szavakat a mögöttes adatkészlet(ek)ben található szinonimákra cseréli le.
* elhalványítja a nem érthető szavakat.

## <a name="combine-results-from-more-than-one-dataset"></a>Eredmények összevonása több adatkészletből
A Power BI egyik leghatékonyabb szolgáltatása a különböző adatkészletekből származó adatok összevonásának képessége.  Így nem kell egyetlen adatkészletre korlátozni a kérdéseket – a felhasználó olyan kérdéseket tehet fel, amelyekre a rendszer egynél több adatkészletből ad vissza adatokat. Például ha a saját irányítópulton a Kiskereskedelmi elemzési minta és az Államnépesség adatkészletből szerepelnek csempék, akkor kérhető a rendszertől az *áruházak számának megjelenítése államnépesség szerint, csökkenő sávdiagramon*.

## <a name="dont-stop-now"></a>Nincs megállás
Miután a Q&A megjeleníti az eredményeket, folytathatja a beszélgetést! A vizualizáció és a Q&A interaktív funkcióinak használatával további betekintést kaphat az adatokba.

## <a name="next-steps"></a>Következő lépések
Vissza a [Q&A a Power BI-ban](power-bi-q-and-a.md) című témakörhöz  

[Power BI – alapfogalmak](service-basic-concepts.md)  

További kérdései vannak? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

