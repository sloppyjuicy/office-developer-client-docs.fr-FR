---
title: LineGradientDir, cellule (Section Propriétés de dégradé)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Détermine la direction du dégradé ligne. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788958"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>LineGradientDir, cellule (Section Propriétés de dégradé)

Détermine la direction du dégradé ligne. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès. 
  
> [!NOTE]
> Dégradé linéaire est le seul dégradé qui prend une valeur d’angle supplémentaires (tel que déterminé par la cellule **LineGradientDir** ). Toutes les autres directions dégradées ont prédéfinie énumérations. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Dégradé linéaire. La cellule **LineGradientAngle** détermine la direction du dégradé.  <br/> |
|1 à 7  <br/> |Dégradé radial. Dégradé s’étend vers l’extérieur d’un cercle à partir d’un point central.  <br/> |
|8-12  <br/> |Dégradé rectangulaire. Dégradé étend par un trait de direction à partir d’une origine de fondu rectangulaire.  <br/> |
|13  <br/> |Dégradé de chemin d’accès.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LineGradientDir** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LineGradientDir  <br/> |
   
Pour obtenir une référence à la cellule **LineGradientDir** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visLineGradientDir** <br/> |
   

