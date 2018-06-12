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
description: Une valeur RVB qui représente la couleur attribuée à la balise du réviseur d’un document.
ms.openlocfilehash: a8771bb35cfc1b57990f24e1a0a3d677f9cffc0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788276"
---
# <a name="color-cell-reviewer-section"></a>Color, cellule (section Reviewer)

Une valeur RVB qui représente la couleur attribuée à la balise du réviseur d’un document. 
  
## <a name="remarks"></a>Note

Les couleurs sont attribuées aux réviseurs selon la séquence suivante : rouge, bleu, vert, violet, orange, turquoise, gris. Ces couleurs se succèdent à nouveau pour chaque autre réviseur. 
  
Les commentaires entrés sur la page de dessin d'origine sont toujours de couleur jaune, peu importe la couleur attribuée à un réviseur dans la cellule Color. 
  
Pour obtenir une référence à la cellule Color par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Reviewer.Color [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Color par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionReviewer** <br/> |
| Index de la ligne :  <br/> |**visRowReviewer** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visReviewerColor** <br/> |
   

