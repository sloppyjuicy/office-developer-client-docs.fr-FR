---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Détermine la quantité de distorsion d’un effet d’croquis, sous la mesure d’un nombre integer entre 0 et 25.
ms.openlocfilehash: dc33ea18881cce3d7e5a31f4522074a7b942ddb4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549601"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>SketchAmount Cell (Additional Effect Properties Section)

Détermine la quantité de distorsion d’un effet d’croquis, sous la mesure d’un nombre integer entre 0 et 25. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun effet d’croquis n’est appliqué à la forme.  <br/> |
|1-25  <br/> |Une distorsion de croquis est appliquée à la forme, où la valeur 1 est la plus distorsion et 25 la moins.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **SketchAmount** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SketchAmount  <br/> |
   
Pour obtenir une référence à la **cellule SketchAmount** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowOtherEffectProperties** <br/> |
| Index de la cellule :  <br/> |**visSketchAmount** <br/> |
   

