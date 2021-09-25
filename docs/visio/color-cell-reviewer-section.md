---
title: Color, cellule (section Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
ms.localizationpriority: medium
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Valeur RVB qui représente la couleur affectée au code d’un réviseur de documents.
ms.openlocfilehash: a5b34ad4902a7b6ba2e8143c358533fb235467b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566072"
---
# <a name="color-cell-reviewer-section"></a>Color, cellule (section Reviewer)

Valeur RVB qui représente la couleur affectée au code d’un réviseur de documents. 
  
## <a name="remarks"></a>Remarques

Les couleurs sont attribuées aux réviseurs selon la séquence suivante : rouge, bleu, vert, violet, orange, turquoise, gris. Ces couleurs se succèdent à nouveau pour chaque autre réviseur. 
  
Les commentaires entrés sur la page de dessin d'origine sont toujours de couleur jaune, peu importe la couleur attribuée à un réviseur dans la cellule Color. 
  
Pour obtenir une référence à la cellule Color par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Reviewer.Color [  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Color à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionReviewer** <br/> |
| Index de la ligne :  <br/> |**visRowReviewer**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visReviewerColor** <br/> |
   

