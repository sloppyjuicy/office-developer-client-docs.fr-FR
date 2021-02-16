---
title: ReplaceLockShapeData Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d’une forme remplacée lors d’une opération de remplacement de forme. ReplaceLockShapeData détermine si les données de forme de la forme de base remplacent toutes les données de forme de la forme en cours de remplacement.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408872"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>ReplaceLockShapeData Cell (Change Shape Behavior Section)

Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d’une forme remplacée lors d’une opération de remplacement de forme. **ReplaceLockShapeData** détermine si les données de forme de la forme de base remplacent toutes les données de forme de la forme en cours de remplacement. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|1 (TRUE)  <br/> |Toutes les lignes et valeurs de la section **Données** de forme de la forme de base sont copiées sur la forme de remplacement et toutes les valeurs locales de l’ancienne forme en cours de remplacement sont ignorées.  <br/> |
|0 (FALSE)  <br/> |Les lignes et les valeurs de la section **Données** de forme de la forme de base sont copiées dans la forme de remplacement. Toutes les lignes de la section **Données de** forme de l’ancienne forme avec des valeurs locales sont transférées vers la forme de remplacement.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ReplaceLockShapeData** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | ReplaceLockShapeData  <br/> |
   
Pour obtenir une référence à la **cellule ReplaceLockShapeData** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowReplaceBehaviors** <br/> |
| Index de la cellule :  <br/> |**visReplaceLockShapeData** <br/> |
   

