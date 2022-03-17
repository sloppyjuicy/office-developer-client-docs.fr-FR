---
title: LineGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Détermine la direction du dégradé de trait. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès.
ms.openlocfilehash: 0cae74990fde3872c8274ae7c29cf8a94226be75
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522099"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>LineGradientDir Cell (Gradient Properties Section)

Détermine la direction du dégradé de trait. Un dégradé peut être linéaire, radial, rectangulaire ou suivre un chemin d’accès. 
  
> [!NOTE]
> Un dégradé linéaire est le seul dégradé qui prend une valeur d’angle supplémentaire (tel que déterminé par la cellule **LineGradientDir** ). Toutes les autres directions de dégradé ont des éumérations prédéfinie. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Dégradé linéaire. La **cellule LineGradientAngle** détermine la direction du dégradé. |
|1-7  <br/> |Dégradés radiaux. Le dégradé étend l’extérieur dans un cercle à partir d’un point central. |
|8-12  <br/> |Dégradés rectangulaires. Le dégradé s’étend sous la forme d’une ligne directionnelle à partir d’une origine avec un fondu rectangulaire. |
|13  <br/> |Dégradé de chemin d’accès. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **LineGradientDir** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | LineGradientDir  <br/> |
   
Pour obtenir une référence à la cellule **LineGradientDir** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowGradientProperties** <br/> |
| **Index de la cellule :**  <br/> |**visLineGradientDir** <br/> |
   

