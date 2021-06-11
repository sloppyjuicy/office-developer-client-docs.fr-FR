---
title: DisplayMode Cell (Action Tags Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Détermine si la balise d’action s’affiche lorsque l’utilisateur déplace le pointeur sur la balise, lorsque la forme est sélectionnée ou en tout temps.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415816"
---
# <a name="displaymode-cell-action-tags-section"></a>DisplayMode Cell (Action Tags Section)

Détermine si la balise d’action s’affiche lorsque l’utilisateur déplace le pointeur sur la balise, lorsque la forme est sélectionnée ou en tout temps.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Mode d’affichage**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | S’affiche lorsque la souris est suspendue sur la balise (valeur par défaut).  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | Apparaît tant que la forme est sélectionnée.  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | Apparaît tout le temps.  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>Remarques

Les balises d’action n’apparaissent pas dans les résultats imprimés ou publiés. 
  
Si une balise d’action est définie pour une page et si cette cellule contient la valeur 1, la balise n’apparaît jamais, car une page ne peut pas être sélectionnée. 
  
Pour obtenir une référence à la cellule DisplayMode à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTags.  *nom*  . DisplayMode où SmartTags. *name est*  le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule DisplayMode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagDisplayMode** <br/> |
   

