---
title: "Irányítópult-csempék szerkesztése és eltávolítása"
description: "Irányítópult-csempék szerkesztésére vonatkozó dokumentáció – átméretezés, áthelyezés, átnevezés, rögzítés, törlés, hivatkozás hozzáadása."
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: lJKgWnvl6bQ
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/26/2017
ms.author: mihart
ms.openlocfilehash: ca59631223fda705ed828f6c923f0ad58d262d76
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 11/13/2017
---
# <a name="edit-or-remove-a-dashboard-tile"></a>Irányítópult-csempék szerkesztése és eltávolítása
Módosíthatja az irányítópulton lévő csempék megjelenését és alapértelmezett viselkedését.

<iframe width="560" height="315" src="https://www.youtube.com/embed/lJKgWnvl6bQ" frameborder="0" allowfullscreen></iframe>

Ez a cikk az alábbiakat ismerteti.

* [Csempe rögzítése egy másik irányítópulton](#different)
* [ Csempe átnevezése](#rename)
* [Csempe áthelyezése](#move)
* [ Csempe átméretezése](#resize)
* [Hivatkozás hozzáadása egy csempéhez](#hyperlink)
* [Csempe törlése](#delete)
  
  > [!TIP]
  > Ha magán a csempén látható vizualizációt szeretné módosítani, törölje a csempét, és vegyen fel egy új [irányítópult-csempét](service-dashboard-tiles.md).
  > 
  > 

## <a name="how-to-begin"></a>Első lépések
1. Nyisson meg egy olyan [irányítópultot](service-dashboards.md), amelyen legalább egy csempe van. 
   
   ![](media/service-dashboard-edit-tile/power-bi-tile.png)
2. Mozgassa az egérmutatót az irányítópult-csempe fölé, és a három pontot kiválasztva jelenítse meg a beállításokat.
   
   ![](media/service-dashboard-edit-tile/power-bi-tile-menu-new.png)

<a name="different"></a>

## <a name="pin-the-tile-to-a-dashboard"></a>Csempe rögzítése egy irányítópulton
1. Válassza a **Csempe rögzítése** ikont ![](media/service-dashboard-edit-tile/pinnooutline.png).
2. Döntse el, hogy egy meglévő vagy egy új irányítópulton rögzíti-e a csempét. 
   
   ![](media/service-dashboard-edit-tile/pbi_pintoanotherdash.png)
3. Válassza a **Rögzítés** lehetőséget.

- - -
<a name="rename"></a>

## <a name="rename-the-tile-and-edit-tile-details"></a>A csempe átnevezése, valamint a csempe részleteinek szerkesztése
A Csempe részletei ikon ![](media/service-dashboard-edit-tile/pbi_nancy_pencilicon.png) kiválasztásával szerkesztheti a címet, és megjelenítheti a legutóbbi frissítési időpontot.

![](media/service-dashboard-edit-tile/power-bi-tile-details.png)

- - -
<a name="move"></a>

## <a name="move-the-tile"></a>A csempe áthelyezése
A csempe kiválasztásával és lenyomva tartásával húzhatja azt át az új helyre az irányítópult vásznán.

- - -
<a name="resize"></a>

## <a name="resize-the-tile"></a>A csempe átméretezése
Különböző méretekre állíthatja a csempéket – az 1x1-es elrendezéstől akár az 5x5-ös elrendezésig. A fogópont (a jobb alsó sarokban) kiválasztásával és húzásával méretezheti át a csempét.
    ![](media/service-dashboard-edit-tile/pbigif_resizetile4.gif)

- - -
<a name="hyperlink"></a>

## <a name="change-the-default-hyperlink"></a>Az alapértelmezett hivatkozás módosítása
Alapértelmezés szerint egy csempe kiválasztásával nyitható meg a csempe létrehozásakor használt jelentés vagy a Q&A (ha a csempe a Q&A-ben jött létre). Egy weblap, egy másik irányítópult vagy jelentés (ugyanazon a munkaterületen), egy SSRS-jelentés vagy egyéb online tartalom hivatkozásához vegyen fel egyéni hivatkozást:

1. Válassza ki a **Részletek szerkesztése** ikont ![](media/service-dashboard-edit-tile/pbi_nancy_pencilicon.png) a csempe szerkesztéséhez.
2. Jelölje be pipával az **Egyéni hivatkozás beállítása** jelölőnégyzetet, és válassza ki a hivatkozás típusát.    
   
   * Külső hivatkozás esetén adja meg az URL-címet.     
   * Az aktuális munkaterület egy irányítópultjának vagy jelentésének hivatkozásához válassza ki azt a legördülő menüből.
   
   ![](media/service-dashboard-edit-tile/power-bi-set-custom-link.png)

- - -
<a name="delete"></a>

## <a name="delete-the-tile"></a>A csempe törlése
* Válassza ki a **Csempe törlése** ikont ![](media/service-dashboard-edit-tile/power-bi-delete-tile-icon.png) a csempe törléséhez. A csempe törlésével nem törli az alapul szolgáló jelentést vagy vizualizációt.

- - -
## <a name="next-steps"></a>Következő lépések
[Irányítópult-csempék a Power BI-ban](service-dashboard-tiles.md)

[Irányítópultok a Power BI-ban](service-dashboards.md)

[Power BI – alapfogalmak](service-basic-concepts.md)

További kérdései vannak? [Kérdezze a Power BI-közösséget!](http://community.powerbi.com/)

