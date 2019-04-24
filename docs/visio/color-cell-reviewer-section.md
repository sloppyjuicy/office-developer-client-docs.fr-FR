---
title: Color, cellule (section Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Valeur RVB qui représente la couleur attribuée au balisage d'un réviseur de document.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341817"
---
# <a name="color-cell-reviewer-section"></a>Color, cellule (section Reviewer)

Valeur RVB qui représente la couleur attribuée au balisage d'un réviseur de document. 
  
## <a name="remarks"></a>Remarques

Les couleurs sont attribuées aux réviseurs selon la séquence suivante : rouge, bleu, vert, violet, orange, turquoise, gris. Ces couleurs se succèdent à nouveau pour chaque autre réviseur. 
  
Les commentaires entrés sur la page de dessin d'origine sont toujours de couleur jaune, peu importe la couleur attribuée à un réviseur dans la cellule Color. 
  
Pour obtenir une référence à la cellule Color par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Reviewer. Color [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Color à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionReviewer** <br/> |
| Index de la ligne :  <br/> |**visRowReviewer** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visReviewerColor** <br/> |
   

