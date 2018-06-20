---
title: CompoundType, cellule (Section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Détermine le type de la ligne d’une forme composé.
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788300"
---
# <a name="compoundtype-cell-line-format-section"></a>CompoundType, cellule (Section Line Format)

Détermine le type de la ligne d’une forme composé. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Simple  <br/> |
|1  <br/> |Double  <br/> |
|2  <br/> |Épais fin  <br/> |
|3  <br/> |Épais fin  <br/> |
|4  <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **CompoundType** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | CompoundType  <br/> |
   
Pour obtenir une référence à la cellule **CompoundType** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLine** <br/> |
| Index de la cellule :  <br/> |**visCompoundType** <br/> |
   

