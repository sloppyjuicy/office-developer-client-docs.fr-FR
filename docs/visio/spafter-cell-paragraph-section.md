---
title: SpAfter, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
ms.localizationpriority: medium
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Détermine l'espace inséré après chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du dernier paragraphe d'un bloc, de l'espace défini dans la cellule BottomMargin.
ms.openlocfilehash: cdabd57f5dbad41e9b4d09e684c59df242d1e2ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622787"
---
# <a name="spafter-cell-paragraph-section"></a>SpAfter, cellule (section Paragraph)

Détermine l'espace inséré après chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du dernier paragraphe d'un bloc, de l'espace défini dans la cellule BottomMargin.
  
## <a name="remarks"></a>Remarques

Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, le paramètre de l'espace après ne change pas.
  
Pour obtenir une référence à la cellule SpAfter par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.SpAfter[  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule SpAfter par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSpaceAfter** <br/> |
   

