---
title: ReplaceLockFormat, cellule (Section de comportement de forme modification)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme. Si la cellule ReplaceLockFormat d’une forme de base est définie sur TRUE (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes de la forme remplacée par la forme de base.
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789448"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>ReplaceLockFormat, cellule (Section de comportement de forme modification)

Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme. Si la cellule **ReplaceLockFormat** d’une forme de base est définie sur TRUE (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes de la forme remplacée par la forme de base. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Si la cellule **ReplaceLockFormat** d’une forme de base est définie sur TRUE, les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes de la forme remplacée par la forme de base.  <br/> |
|FALSE  <br/> |Si la cellule **ReplaceLockFormat** d’une forme de base est définie sur FALSE, la forme de remplacement contient les valeurs de mise en forme locales à partir de la forme ancienne après l’opération de remplacement.  <br/> |
   
## <a name="remarks"></a>Remarques

La cellule **ReplaceLockFormat** détermine si la forme de base remplace les valeurs locales de mise en forme des cellules dans les sections suivantes lors d’une opération de remplacement de forme : 
  
- Section **Format de remplissage** 
    
- Section **Format de ligne** 
    
- Section **Style rapide** 
    
- Section **Propriétés de thème** 
    
- Section **Propriétés du dégradé** 
    
- Section **Propriétés de biseau** 
    
- Section **Propriétés d’effet supplémentaires** 
    
- Section **Points de dégradés ligne** 
    
- Section **De dégradé de remplissage** 
    
Pour obtenir une référence à la cellule **ReplaceLockFormat** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ReplaceLockFormat  <br/> |
   
Pour obtenir une référence à la cellule **ReplaceLockFormat** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowReplaceBehaviors** <br/> |
| Index de la cellule :  <br/> |**visReplaceLockFormat** <br/> |
   

