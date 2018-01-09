---
title: "Adatvédelmi beállítások letiltása"
description: "Így engedélyezheti a Gyors összevonást a Személyes átjárón az adatvédelmi beállítások frissítésének letiltásához."
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
ms.tgt_pltfrm: na
ms.workload: powerbi
ms.date: 12/06/2017
ms.author: davidi
ms.openlocfilehash: 1e68f7df5214e038df8bcd1584acb815c0af98bf
ms.sourcegitcommit: 70e9239e375ae03744fb9bc122d5fc029fb83469
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/22/2017
---
# <a name="disable-privacy-setting-in-power-bi-gateway---personal"></a>Adatvédelem letiltása a személyes Power BI Gatewayen
> [!NOTE]
> A személye Power BI Gatewaynek van egy új verziója, melynek neve **helyszíni adatátjáró (személyes mód)**. A következő cikk a személyes átjáró korábbi verzióját, a **Személyes Power BI Gatewayt** ismerteti, amely 2017. július 31-ével elavult, és nem használható tovább. A személyes átjáró új verziójával kapcsolatos információkat, beleértve az új verzió telepítésének menetét, a [**helyszíni adatátjárót (személyes mód)** ismertető cikkben](service-gateway-personal-mode.md) találhatja. A Gyors összevonás a személyes átjáró új verziójában is elérhető, és az a cikk is kitér az ismertetésére.
> 
> 

Az adatok a személyes átjáróval való használatakor az adatforrások adatvédelmi beállításai miatt a következő hibaüzenet jelenhet meg.

> *Hiba történt az adatkészlet adatainak feldolgozása során.*
> 
> *[Nem kombinálhatók az adatok] &lt;A lekérdezés &gt;/&lt;…&gt;/&lt;…&gt; részei olyan adatforrásokhoz próbálnak hozzáférni, amelyeket az adatvédelmi beállításaik miatt nem lehet együtt használni. Kérjük, építse újra az adategyesítést.*
> 
> 

A problémát megkerülheti a **Gyors összevonás** bekapcsolásával. A **Gyors összevonás** figyelmen kívül hagyja az adatvédelmi beállításokat, ezáltal lehetővé teszi a különböző adatforrások egyesítését.

> [!NOTE]
> Az adatok összevonása során az adatvédelmi szintek nem lesznek figyelembe véve. Az adatok összevonásakor ezért más adatforrások bizalmas adatokhoz férhetnek hozzá.
> 
> 

## <a name="what-is-fast-combine"></a>Mi az a Gyors összevonás?
Az adatvédelmi szintekkel és a Gyors összevonással kapcsolatos további tudnivalókért tekintse meg az [adatvédelmi szinteket](https://support.office.com/en-us/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540) ismertető cikket. Alapértelmezés szerint a privát adatvédelmi szint van beállítva, ami a fentebb említett hibát eredményezheti. Ez azért van, mert a privát beállítás elzárja az adatforrást a többi adatforrás elől. Ez például olyan esetekben okozhat problémát, ha egy parametrizált lekérdezés egy másik adatforrásból szerez adatokat.

A Gyors összevonás bekapcsolásával figyelmen kívül hagyja a privát beállítást, és lehetővé teszi, hogy a kivétel érvényesüljön.

## <a name="turn-on-fast-combine"></a>A Gyors összevonás bekapcsolása
A következő lépésekkel engedélyezheti a Gyors összevonást a saját személyes átjárójához. A helyszíni adatátjárón nincs ilyen beállítás.

1. Nyissa meg a **ConnectorConfig.xml** fájlt.  Ez a számítógépen két helyen lehet.  Ha Ön a számítógép rendszergazdája, akkor a hely a következő.
   
    <pre><code>C:\Program Files\Power BI Personal Gateway\1.0\Configurator\Connector</code></pre>
   
    Ha Ön nem rendszergazda, akkor a hely a következő.
   
    <pre><code>C:\Users\[username]\AppData\Local\Power BI Personal Gateway\1.0\Configurator\Connector</code></pre>
    
2. Adja hozzá a konfigurációs fájlhoz az **&lt;EnableFastCombine&gt;** (Gyors összevonás engedélyezése) elemet true (igaz) értékkel. Az elem hozzáadásával kapcsolja be a **Gyors összevonást**.
   
   <pre><code>&lt;EnableFastCombine&gt;true&lt;/EnableFastCombine&gt;</code></pre>
   
   ![](media/refresh-enable-fast-combine/configfile.png)
3. Lépjen ki, majd indítsa újra az átjáró konfigurációs képernyőjét.
4. Megjelenik egy állapot, amely arról értesíti, hogy a Gyors összevonás engedélyezve lett.
   
   ![](media/refresh-enable-fast-combine/fastcombineenabled.png)

## <a name="turn-off-fast-combine"></a>A Gyors összevonás kikapcsolása
1. Nyissa meg a **ConnectorConfig.xml** fájlt.  Ez a számítógépen két helyen lehet.  Ha Ön a számítógép rendszergazdája, akkor a hely a következő.
   
    <pre><code>C:\Program Files\Power BI Personal Gateway\1.0\Configurator\Connector</code></pre>
   
    Ha Ön nem rendszergazda, akkor a hely a következő.
   
    <pre><code>C:\Users\[username]\AppData\Local\Power BI Personal Gateway\1.0\Configurator\Connector</code></pre>

2. Távolítsa el a konfigurációs fájlból az **&lt;EnableFastCombine&gt;** elemet. Az elem eltávolításával kapcsolja ki a **Gyors összevonást**.
3. Lépjen ki, majd indítsa újra az átjáró konfigurációs képernyőjét.
4. Nem lesz többé látható az állapot, amely arról értesíti, hogy a **Gyors összevonás** engedélyezve van.

## <a name="next-steps"></a>Következő lépések
[Helyszíni adatátjáró (személyes mód) – a személyes átjáró új verziója](service-gateway-personal-mode.md)
[Adatvédelmi szintek](https://support.office.com/en-us/article/Privacy-levels-Power-Query-CC3EDE4D-359E-4B28-BC72-9BEE7900B540)  
[Gyakori lekérdezési feladatok a Power BI Desktopban](desktop-common-query-tasks.md)  
További kérdései vannak? [Felteheti azokat a Power BI-közösségnek](http://community.powerbi.com/)

