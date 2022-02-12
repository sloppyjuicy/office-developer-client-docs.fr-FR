---
title: FillGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Détermine la direction du dégradé de remplissage. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.
ms.openlocfilehash: a4c3b23e065dfa95dbd32d6ac9074c4c2a4ecfbd
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774333"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>FillGradientDir Cell (Gradient Properties Section)

Détermine la direction du dégradé de remplissage. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès. 
  
> [!NOTE]
> Un dégradé linéaire est le seul dégradé qui prend une valeur d’angle supplémentaire (comme déterminé par la **cellule FillGradientDir** ). Toutes les autres directions de dégradé ont des éumérations prédéfinie. 
  
****

|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Dégradé linéaire. La **cellule FillGradientAngle** détermine la direction du dégradé. |
|1-7  <br/> |Dégradés radiaux. Le dégradé étend l’extérieur dans un cercle à partir d’un point central. |
|8-12  <br/> |Dégradés rectangulaires. Le dégradé s’étend sous la forme d’une ligne directionnelle à partir d’une origine avec un fondu rectangulaire. |
|13  <br/> |Dégradé de chemin d’accès. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **FillGradientDir** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | FillGradientDir  <br/> |
   
Pour obtenir une référence à la **cellule FillGradientDir** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visFillGradientDir** <br/> |
   

