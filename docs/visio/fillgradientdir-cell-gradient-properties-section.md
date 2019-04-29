---
title: FillGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Détermine la direction du dégradé de remplissage. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un tracé.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406716"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>FillGradientDir Cell (Gradient Properties Section)

Détermine la direction du dégradé de remplissage. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un tracé. 
  
> [!NOTE]
> Un dégradé linéaire est le seul dégradé qui prend une valeur d'angle supplémentaire (tel que déterminé par la cellule **FillGradientDir** ). Toutes les autres directions de dégradé ont des énumérations prédéfinies. 
  
****

|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Dégradé linéaire La cellule **FillGradientAngle** détermine la direction du dégradé.  <br/> |
|1-7  <br/> |Dégradés radiaux Le dégradé s'étend vers l'extérieur d'un cercle à partir d'un point central.  <br/> |
|8-12  <br/> |Dégradés rectangulaires. Le dégradé s'étend sous la forme d'un trait directionnel à partir d'une origine avec un fondu en forme rectangulaire.  <br/> |
|13   <br/> |Dégradé du tracé.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **FillGradientDir** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | FillGradientDir  <br/> |
   
Pour obtenir une référence à la cellule **FillGradientDir** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visFillGradientDir** <br/> |
   

