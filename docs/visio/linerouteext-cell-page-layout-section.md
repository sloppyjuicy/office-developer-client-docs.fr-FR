---
title: LineRouteExt, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Détermine l'aspect par défaut de tous les connecteurs d'une page de dessin.
ms.openlocfilehash: 21da283f2d9ab43837b8fe4127840e89ea9d9949
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788970"
---
# <a name="linerouteext-cell-page-layout-section"></a>LineRouteExt, cellule (section Page Layout)

Détermine l'aspect par défaut de tous les connecteurs d'une page de dessin.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Par défaut (droit)  <br/> |**visLORouteExtDefault** <br/> |
| 1  <br/> | Droit  <br/> |**visLORouteExtStraight** <br/> |
| 2  <br/> | Courbé  <br/> |**visLORouteExtNURBS** <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LineRouteExt par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LineRouteExt  <br/> |
   
Pour obtenir une référence à la cellule LineRouteExt par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOLineRouteExt** <br/> |
   

