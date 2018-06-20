---
title: LineGradientEnabled, cellule (Section Propriétés de dégradé)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 276a661f-d14e-404a-a494-ae36601a8ce3
description: Détermine si un dégradé de ligne est activé pour une ligne ou de la bordure d’une forme.
ms.openlocfilehash: d78a94a25c0290bd5e58522c9a45955868f31b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788939"
---
# <a name="linegradientenabled-cell-gradient-properties-section"></a>LineGradientEnabled, cellule (Section Propriétés de dégradé)

Détermine si un dégradé de ligne est activé pour une ligne ou de la bordure d’une forme. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Dégradé s’affiche sur la ligne ou de la bordure d’une forme.  <br/> |
|FALSE  <br/> |Dégradés ne sont pas affichés sur la ligne ou de la bordure d’une forme.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LineGradientEnabled** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LineGradientEnabled  <br/> |
   
Pour obtenir une référence à la cellule **LineGradientEnabled** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visLineGradientEnabled** <br/> |
   

