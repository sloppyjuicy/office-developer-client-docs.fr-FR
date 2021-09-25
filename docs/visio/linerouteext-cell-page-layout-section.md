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
ms.openlocfilehash: 37bcf569b4a095ed1b3e08823db1673ef5cc95cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615885"
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
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LineRouteExt  <br/> |
   
Pour obtenir une référence à la cellule LineRouteExt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOLineRouteExt** <br/> |
   

