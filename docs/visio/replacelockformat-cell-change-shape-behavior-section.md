---
title: ReplaceLockFormat Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d'une forme remplacée pendant une opération de remplacement de forme. Si la cellule ReplaceLockFormat d'une forme de base est définie sur TRUE (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes d'une forme remplacée par la forme de base.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427233"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>ReplaceLockFormat Cell (Change Shape Behavior Section)

Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d'une forme remplacée pendant une opération de remplacement de forme. Si la cellule **ReplaceLockFormat** d'une forme de base est définie sur true (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes d'une forme remplacée par la forme de base. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Si la cellule **ReplaceLockFormat** d'une forme de base est définie sur true, les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes d'une forme remplacée par la forme de base.  <br/> |
|FALSE  <br/> |Si la cellule **ReplaceLockFormat** d'une forme de base est définie sur false, la forme de remplacement contient les valeurs de mise en forme locale de l'ancienne forme après l'opération de remplacement.  <br/> |
   
## <a name="remarks"></a>Remarques

La cellule **ReplaceLockFormat** détermine si la forme de base remplace les valeurs de mise en forme locale des cellules dans les sections suivantes lors d'une opération de remplacement de forme: 
  
- Section **format de remplissage** 
    
- Section **format de ligne** 
    
- Section **style rapide** 
    
- Section **Propriétés du thème** 
    
- Section **Propriétés du dégradé** 
    
- Section **Propriétés du biseau** 
    
- Section **autres propriétés d'effet** 
    
- Section points de **dégradé de ligne** 
    
- Section points de **dégradé de remplissage** 
    
Pour obtenir une référence à la cellule **ReplaceLockFormat** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ReplaceLockFormat  <br/> |
   
Pour obtenir une référence à la cellule **ReplaceLockFormat** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowReplaceBehaviors** <br/> |
| Index de la cellule :  <br/> |**visReplaceLockFormat** <br/> |
   

