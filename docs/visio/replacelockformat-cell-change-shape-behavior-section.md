---
title: ReplaceLockFormat Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d’une forme remplacée lors d’une opération de remplacement de forme. Si la cellule ReplaceLockFormat d’une forme de base est définie sur TRUE (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes d’une forme remplacée par la forme de base.
ms.openlocfilehash: 2953636e325960f2947a8ecb0f38d505a66a8ceb
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521812"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>ReplaceLockFormat Cell (Change Shape Behavior Section)

Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d’une forme remplacée lors d’une opération de remplacement de forme. Si la **cellule ReplaceLockFormat** d’une forme de base est définie sur TRUE (1), les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes d’une forme remplacée par la forme de base. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Si la **cellule ReplaceLockFormat** d’une forme de base est définie sur TRUE, les valeurs de mise en forme de la forme de base remplacent toutes les valeurs correspondantes d’une forme remplacée par la forme de base. |
|FALSE  <br/> |Si la **cellule ReplaceLockFormat** d’une forme de base a la valeur FALSE, la forme de remplacement contient les valeurs de mise en forme locales de l’ancienne forme après l’opération de remplacement. |
   
## <a name="remarks"></a>Remarques

La **cellule ReplaceLockFormat** détermine si la forme de base remplace les valeurs de mise en forme locales des cellules des sections suivantes lors d’une opération de remplacement de forme : 
  
- **Section Format de** remplissage 
    
- **Section Format de** ligne 
    
- **Section Style rapide** 
    
- **Section Propriétés du** thème 
    
- **Section Propriétés du** dégradé 
    
- **Section Propriétés du biseau** 
    
- **Section Propriétés d’effet supplémentaires** 
    
- **Section Line Gradient Stops** 
    
- **Section Fill Gradient Stops** 
    
Pour obtenir une référence à la cellule **ReplaceLockFormat** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | ReplaceLockFormat  <br/> |
   
Pour obtenir une référence à la **cellule ReplaceLockFormat** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowReplaceBehaviors** <br/> |
| **Index de la cellule :**  <br/> |**visReplaceLockFormat** <br/> |
   

