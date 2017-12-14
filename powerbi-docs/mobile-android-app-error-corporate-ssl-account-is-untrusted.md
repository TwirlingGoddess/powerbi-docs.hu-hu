---
title: 'Hiba: '
corporate: 
ssl: 
certificate: 
is: 
untrusted": 
'-': 
power: 
bi": 
description: "A Power BI Androidos alkalmazásba való bejelentkezéskor a következő üzenet jelenhet meg: „A hitelesítés nem sikerült, mert a vállalati SSL-tanúsítványt nem megbízhatóként kezeli ez az eszköz”"
.": 
services: powerbi
documentationcenter: 
author: maggiesMSFT
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
ms.date: 10/13/2017
ms.author: maggies
ms.openlocfilehash: 4ef29c0cab96e21045f30805d7445aa34d37697a
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="error-corporate-ssl-certificate-is-untrusted---power-bi"></a>Hiba: „A vállalati SSL-tanúsítvány nem megbízható” – Power BI
A Microsoft Power BI Android-mobilalkalmazásba való bejelentkezéskor a következő üzenet jelenhet meg: „A hitelesítés nem sikerült, mert a vállalati SSL-tanúsítványt nem megbízhatóként kezeli ez az eszköz. Kérjük, lépjen kapcsolatba a vállalata rendszergazdájával.” 

Az ilyenkor szükséges lépések általában az Android-eszköz operációs rendszerétől függenek, azonban a hibát néhány egyéb dolog is okozhatja.

## <a name="on-android-7-or-later"></a>Az Android 7-es vagy újabb verzióján
Keressen rá a **Chrome** nevű alkalmazás frissítésére, és telepítse azt.

## <a name="on-android-6-and-earlier"></a>Az Android 6-os vagy újabb verzióján
Szükség lehet a System Webview frissített verziójára az eszközön. Ha ez telepítve van az eszközön, elég csak a **Frissítés** gombra kattintania.

Ha a System Webview nincs telepítve az eszközön:

1. Zárja be a Power BI alkalmazást az Android-eszközön.
2. Nyissa meg a Google Play Áruházat, és keressen rá a Google Inc. által készített **System Webview** alkalmazásra.
3. Telepítse.
4. Indítsa el újra a Power BI alkalmazást, és jelentkezzen be.

## <a name="time-zone-settings"></a>Időzóna-beállítások
Elképzelhető, hogy az eszköz időzóna-beállításai nem megfelelőek. 

A **Beállítások** > **Rendszer** > **Dátum és idő** helyen tudja ellenőrizni ezeket.

## <a name="custom-authentication-server"></a>Egyéni hitelesítési kiszolgáló
Ha egyéni hitelesítési kiszolgálót használ, előfordulhat, hogy a vállalati hitelesítési kiszolgáló SSL-tanúsítványa nem érvényes. Segítségért forduljon a szervezet rendszergazdájához.

## <a name="next-steps"></a>További lépések
* [Töltse le az Android-alkalmazást](http://go.microsoft.com/fwlink/?LinkID=544867) az Androidos alkalmazás-áruházból.
* Kérdése van? [Kérdezze meg a Power BI közösségét](http://community.powerbi.com/)

