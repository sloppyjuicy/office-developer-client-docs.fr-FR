---
title: Width, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: "Contient la largeur de la forme sélectionnée, exprimée en unités de dessin. La formule par défaut permettant de déterminer la largeur d'une forme 1D est la suivante :"
ms.openlocfilehash: 55e77c5ccfca2425a8a2985564448e0f656aebbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790032"
---
# <a name="width-cell-shape-transform-section"></a>Width, cellule (section Shape Transform)

Contient la largeur de la forme sélectionnée, exprimée en unités de dessin. La formule par défaut permettant de déterminer la largeur d'une forme 1D est la suivante :
  
= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Width par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Width  <br/> |
   
Pour obtenir une référence à la cellule Width par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormWidth** <br/> |
   

