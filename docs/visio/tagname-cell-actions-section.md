---
title: TagName, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Contient le nom de la balise d’action à laquelle cette action est associée.
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332388"
---
# <a name="tagname-cell-actions-section"></a>TagName, cellule (section Actions)

Contient le nom de la balise d’action à laquelle cette action est associée.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

La cellule TagName de la section Actions fonctionne avec la cellule TagName de la section Action Tags pour associer une balise d’action à ses actions. 
  
- Si la cellule TagName d'une ligne actions est vide, l'action apparaît dans un menu contextuel, pas dans un menu de balise d'action.
    
- Si la valeur d'une cellule TagName de la ligne actions correspond à la valeur de la cellule TagName d'une ligne Smart Tags, l'action apparaît dans le menu de la balise d'action.
    
- Si la cellule TagName d'une action a une valeur mais qu'elle ne correspond pas à la valeur TagName de la ligne de la balise de la forme, cette action n'apparaît pas dans les menus de la balise d'action ou dans les menus contextuels.
    
- Si plusieurs lignes Smart Tags contiennent la même valeur TagName, elles présentent toutes les mêmes actions.
    
Pour obtenir une référence à la cellule TagName par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Mesures. *nom* . Actions Tagnameoù.  *Name* est le nom de la ligne d'actions  <br/> |
   
Pour obtenir une référence à la cellule TagName par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionTagName** <br/> |
   

