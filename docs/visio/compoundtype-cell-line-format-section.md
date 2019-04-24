---
title: CompoundType Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Détermine le type composé de la ligne d'une forme.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359367"
---
# <a name="compoundtype-cell-line-format-section"></a>CompoundType Cell (Line Format Section)

Détermine le type composé de la ligne d'une forme. 
  
|**Value**|**Description**|
|:-----|:-----|
|0  <br/> |Simple  <br/> |
|0,1  <br/> |Double  <br/> |
|n°2  <br/> |Épais fin  <br/> |
|3  <br/> |Fin épais  <br/> |
|4  <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **CompoundType** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | CompoundType  <br/> |
   
Pour obtenir une référence à la cellule **CompoundType** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowLine** <br/> |
| Index de la cellule :  <br/> |**visCompoundType** <br/> |
   

