---
title: PageLineJumpDirX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Détermine la direction des déviations de trait pour les connecteurs dynamiques horizontaux de la page de dessin n'ayant pas de direction de déviation locale.
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789207"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a>PageLineJumpDirX, cellule (section Page Layout)

Détermine la direction des déviations de trait pour les connecteurs dynamiques horizontaux de la page de dessin n'ayant pas de direction de déviation locale.
  
|**Valeur**|**Direction de déviation de trait**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Par défaut ; à gauche ou paramètres de la page pour les formes  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Haut  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Bas  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule PageLineJumpDirX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageLineJumpDirX  <br/> |
   
Pour obtenir une référence à la cellule PageLineJumpDirX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPageLayout** <br/> |
| Index de la cellule :  <br/> |**visPLOJumpDirX** <br/> |
   

