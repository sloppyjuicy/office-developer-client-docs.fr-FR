---
title: FillGradientDir, cellule (Section Propriétés de dégradé)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Détermine la direction du dégradé du remplissage. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788622"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>FillGradientDir, cellule (Section Propriétés de dégradé)

Détermine la direction du dégradé du remplissage. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès. 
  
> [!NOTE]
> Dégradé linéaire est le seul dégradé qui prend une valeur d’angle supplémentaires (tel que déterminé par la cellule **FillGradientDir** ). Toutes les autres directions dégradées ont prédéfinie énumérations. 
  
****

|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Dégradé linéaire. La cellule **FillGradientAngle** détermine la direction du dégradé.  <br/> |
|1 à 7  <br/> |Dégradé radial. Dégradé s’étend vers l’extérieur d’un cercle à partir d’un point central.  <br/> |
|8-12  <br/> |Dégradé rectangulaire. Dégradé étend par un trait de direction à partir d’une origine de fondu rectangulaire.  <br/> |
|13  <br/> |Dégradé de chemin d’accès.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **FillGradientDir** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | FillGradientDir  <br/> |
   
Pour obtenir une référence à la cellule **FillGradientDir** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGradientProperties** <br/> |
| Index de la cellule :  <br/> |**visFillGradientDir** <br/> |
   

