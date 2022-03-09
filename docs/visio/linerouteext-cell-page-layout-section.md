---
title: LineRouteExt, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
ms.localizationpriority: medium
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Détermine l'aspect par défaut de tous les connecteurs d'une page de dessin.
ms.openlocfilehash: 44f7fdba540ac8bebf723e4ed61364ba39260820
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63406273"
---
# <a name="linerouteext-cell-page-layout-section"></a>LineRouteExt, cellule (section Page Layout)

Détermine l'aspect par défaut de tous les connecteurs d'une page de dessin.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Par défaut (droit)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Droite  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Courbe  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LineRouteExt par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | LineRouteExt  <br/> |
   
Pour obtenir une référence à la cellule LineRouteExt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPageLayout** <br/> |
| **Index de la cellule :**  <br/> |**visPLOLineRouteExt** <br/> |
   

