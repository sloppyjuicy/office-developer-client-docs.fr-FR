---
title: LineGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Détermine si un dégradé de trait est activé pour un trait ou la bordure d’une forme.
ms.openlocfilehash: b6056bff18a1d0a3c19d31c6310c558088fb6ace
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780700"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>LineGradientEnabled Cell (Gradient Properties Section)

Détermine si un dégradé de trait est activé pour un trait ou la bordure d’une forme. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le dégradé est affiché sur le trait ou la bordure d’une forme. |
|FALSE  <br/> |Les dégradés ne sont pas affichés sur le trait ou la bordure d’une forme. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LineGradientEnabled** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LineGradientEnabled  <br/> |
   
Pour obtenir une référence à la cellule **LineGradientEnabled** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visLineGradientEnabled** <br/> |
   

