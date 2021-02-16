---
title: RotateGradientWithShape Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Détermine si un dégradé de remplissage pivote avec une forme en rotation 2D, sous forme de booléen.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412218"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>RotateGradientWithShape Cell (Gradient Properties Section)

Détermine si un dégradé de remplissage pivote avec une forme en rotation 2D, sous forme de booléen.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le dégradé pivote avec la forme lorsque la forme pivote autour de l’axe de rotation. Le « haut » du dégradé est parallèle au handle de rotation.  <br/> |
|FALSE  <br/> |Le dégradé ne pivote pas avec la forme lorsque la forme est pivotée autour de l’axe de rotation. Le « haut » du dégradé est parallèle à la zone de dessin.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **RotateGradientWithShape** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | RotateGradientWithShape  <br/> |
   
Pour obtenir une référence à la **cellule RotateGradientWithShape** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visRotateGradientWithShape** <br/> |
   

