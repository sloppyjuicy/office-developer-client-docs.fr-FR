---
title: RotateGradientWithShape, cellule (Section Propriétés de dégradé)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Détermine si un dégradé de remplissage pivote avec une forme 2D rotation, en tant que valeur de type boolean.
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789488"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>RotateGradientWithShape, cellule (Section Propriétés de dégradé)

Détermine si un dégradé de remplissage pivote avec une forme 2D rotation, en tant que valeur de type boolean.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Dégradé fait pivoter la forme lorsque vous faites pivoter la forme autour de l’axe de rotation. « Haut » du dégradé est parallèle à la poignée de rotation.  <br/> |
|FALSE  <br/> |Dégradé ne pivote pas avec la forme lors de la rotation de la forme autour de l’axe de rotation. « Haut » du dégradé est parallèle à la zone de dessin.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **RotateGradientWithShape** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | RotateGradientWithShape  <br/> |
   
Pour obtenir une référence à la cellule **RotateGradientWithShape** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visRotateGradientWithShape** <br/> |
   

