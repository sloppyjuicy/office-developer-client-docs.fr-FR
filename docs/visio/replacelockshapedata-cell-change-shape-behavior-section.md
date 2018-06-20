---
title: ReplaceLockShapeData, cellule (Section de comportement de forme modification)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme. Le ReplaceLockShapeData détermine si les données de forme de la forme de base remplacent toutes les données de forme de la forme remplacée.
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789470"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>ReplaceLockShapeData, cellule (Section de comportement de forme modification)

Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme. Le **ReplaceLockShapeData** détermine si les données de forme de la forme de base remplacent toutes les données de forme de la forme remplacée. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|1 (TRUE)  <br/> |Toutes les lignes et les valeurs de la section **Données de forme** de la forme de base sont copiés dans la forme de remplacement et des valeurs locales de la forme ancienne remplacée sont ignorées.  <br/> |
|0 (FALSE)  <br/> |Les lignes et les valeurs de la section **Données de forme** de la forme de base sont copiés à la forme de remplacement. Toutes les lignes dans la section **Données de forme** de la forme avec les valeurs locales ancienne sont transférés vers la forme de remplacement.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **ReplaceLockShapeData** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ReplaceLockShapeData  <br/> |
   
Pour obtenir une référence à la cellule **ReplaceLockShapeData** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowReplaceBehaviors** <br/> |
| Index de la cellule :  <br/> |**visReplaceLockShapeData** <br/> |
   

