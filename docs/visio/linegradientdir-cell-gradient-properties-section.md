---
title: LineGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Détermine la direction du dégradé de ligne. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un tracé.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417986"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>LineGradientDir Cell (Gradient Properties Section)

Détermine la direction du dégradé de ligne. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un tracé. 
  
> [!NOTE]
> Un dégradé linéaire est le seul dégradé qui prend une valeur d'angle supplémentaire (tel que déterminé par la cellule **LineGradientDir** ). Toutes les autres directions de dégradé ont des énumérations prédéfinies. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Dégradé linéaire La cellule **LineGradientAngle** détermine la direction du dégradé.  <br/> |
|1-7  <br/> |Dégradés radiaux Le dégradé s'étend vers l'extérieur d'un cercle à partir d'un point central.  <br/> |
|8-12  <br/> |Dégradés rectangulaires. Le dégradé s'étend sous la forme d'un trait directionnel à partir d'une origine avec un fondu en forme rectangulaire.  <br/> |
|13   <br/> |Dégradé du tracé.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LineGradientDir** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | LineGradientDir  <br/> |
   
Pour obtenir une référence à la cellule **LineGradientDir** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visLineGradientDir** <br/> |
   

