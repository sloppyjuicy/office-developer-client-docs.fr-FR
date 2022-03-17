---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Détermine la quantité de distorsion d’un effet d’croquis, sous la mesure d’un nombre integer entre 0 et 25.
ms.openlocfilehash: 74d7c4371f3eab1307892a29a079d2d0bf08cfc3
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522974"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>SketchAmount Cell (Additional Effect Properties Section)

Détermine la quantité de distorsion d’un effet d’croquis, sous la mesure d’un nombre integer entre 0 et 25. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Aucun effet d’croquis n’est appliqué à la forme. |
|1-25  <br/> |Une distorsion de croquis est appliquée à la forme, où la valeur 1 est la plus distorsion et 25 la moins. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **SketchAmount** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | SketchAmount  <br/> |
   
Pour obtenir une référence à la **cellule SketchAmount** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowOtherEffectProperties** <br/> |
| **Index de la cellule :**  <br/> |**visSketchAmount** <br/> |
   

