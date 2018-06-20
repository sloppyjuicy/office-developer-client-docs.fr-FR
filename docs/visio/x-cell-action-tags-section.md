---
title: X, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: Le x - position des coordonnées dans le système de coordonnées locales de la forme autour de laquelle est positionné le bouton de balise d’action.
ms.openlocfilehash: f6b3a57b825c96398058e7b71e3cebeb8480dd49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790047"
---
# <a name="x-cell-action-tags-section"></a>X, cellule (section Action Tags)

*X* -position dans les coordonnées locales de la forme autour de laquelle est positionné le bouton de balise d’action de la coordonnée. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Notes

Les cellules X et Y définissent un point dans le système de coordonnées locales de la forme, tandis que les cellules X Justify et Y Justify définissent le positionnement du bouton de balise d’action par rapport à ce point. 
  
Pour obtenir une référence à la cellule X par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> |Balises actives. *nom* . X où SmartTags. *nom* est le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule X par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagX** <br/> |
   

