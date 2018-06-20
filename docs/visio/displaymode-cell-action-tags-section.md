---
title: DisplayMode, cellule (Section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Détermine si la balise d’action apparaît lorsque l’utilisateur déplace le pointeur au-dessus de la balise, quand la forme est sélectionnée ou tout le temps.
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788465"
---
# <a name="displaymode-cell-action-tags-section"></a>DisplayMode, cellule (Section Action Tags)

Détermine si la balise d’action apparaît lorsque l’utilisateur déplace le pointeur au-dessus de la balise, quand la forme est sélectionnée ou tout le temps.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Mode d’affichage**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | S’affiche lorsque vous positionnez la souris au-dessus de la balise (valeur par défaut).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | Apparaît tant que la forme est sélectionnée.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | Apparaît tout le temps.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Notes

Les balises d’action n’apparaissent pas dans les résultats imprimés ou publiés. 
  
Si une balise d’action est définie pour une page et si cette cellule contient la valeur 1, la balise n’apparaît jamais, car une page ne peut pas être sélectionnée. 
  
Pour obtenir une référence à la cellule DisplayMode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Balises actives.  *nom* . DisplayMode où SmartTags. *nom* est le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule DisplayMode par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagDisplayMode** <br/> |
   

