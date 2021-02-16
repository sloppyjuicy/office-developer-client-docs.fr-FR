---
title: BottomMargin, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm120
localization_priority: Normal
ms.assetid: 3121911b-34d5-d99c-3806-76f6e2824f92
description: "Détermine la distance entre la bordure inférieure du bloc de texte et la dernière ligne de texte qu'il contient. La valeur par défaut est 2,5 mm. Cette valeur est indépendante de l'échelle du dessin : si le dessin est mis à l'échelle, la marge inférieure reste inchangée."
ms.openlocfilehash: 544557f1e797315619bc9975db0b87a09981726c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417209"
---
# <a name="bottommargin-cell-text-block-format-section"></a>BottomMargin, cellule (section Text Block Format)

Détermine la distance entre la bordure inférieure du bloc de texte et la dernière ligne de texte qu'il contient. La valeur par défaut est 2,5 mm. Cette valeur est indépendante de l'échelle du dessin : si le dessin est mis à l'échelle, la marge inférieure reste inchangée.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule BottomMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | BottomMargin  <br/> |
   
Pour obtenir une référence à la cellule BottomMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowText** <br/> |
| Index de la cellule :  <br/> |**visTxtBlkBottomMargin** <br/> |
   

