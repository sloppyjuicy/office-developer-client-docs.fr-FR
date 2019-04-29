---
title: SpBefore, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Détermine l'espace inséré avant chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du premier paragraphe d'un bloc, de l'espace défini dans la cellule TopMargin.
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425756"
---
# <a name="spbefore-cell-paragraph-section"></a>SpBefore, cellule (section Paragraph)

Détermine l'espace inséré avant chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du premier paragraphe d'un bloc, de l'espace défini dans la cellule TopMargin.
  
## <a name="remarks"></a>Remarques

Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, le paramètre de l'espace avant ne change pas.
  
Pour obtenir une référence à la cellule SpBefore par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para. SpBefore [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule SpBefore par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSpaceBefore** <br/> |
   

