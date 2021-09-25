---
title: LineGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Détermine si un dégradé de trait est activé pour un trait ou la bordure d’une forme.
ms.openlocfilehash: 93139db462363c53828f62d1036f0075edfc4f96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615906"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>LineGradientEnabled Cell (Gradient Properties Section)

Détermine si un dégradé de trait est activé pour un trait ou la bordure d’une forme. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le dégradé est affiché sur la ligne ou la bordure d’une forme.  <br/> |
|FALSE  <br/> |Les dégradés ne sont pas affichés sur le trait ou la bordure d’une forme.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LineGradientEnabled** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LineGradientEnabled  <br/> |
   
Pour obtenir une référence à la cellule **LineGradientEnabled** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visLineGradientEnabled** <br/> |
   

