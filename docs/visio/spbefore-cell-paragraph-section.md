---
title: SpBefore, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
ms.localizationpriority: medium
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Détermine l'espace inséré avant chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du premier paragraphe d'un bloc, de l'espace défini dans la cellule TopMargin.
ms.openlocfilehash: ac6f844cd524e83ab0a0dd3e446e5aac86c627ba
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521385"
---
# <a name="spbefore-cell-paragraph-section"></a>SpBefore, cellule (section Paragraph)

Détermine l'espace inséré avant chaque paragraphe dans le bloc de texte de la forme, en plus de l'espace issu de la cellule SpLine et, s'il s'agit du premier paragraphe d'un bloc, de l'espace défini dans la cellule TopMargin.
  
## <a name="remarks"></a>Remarques

Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, le paramètre de l'espace avant ne change pas.
  
Pour obtenir une référence à la cellule SpBefore par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Para.SpBefore[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule SpBefore par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionParagraph** <br/> |
| **Index de la ligne :**  <br/> |**visRowParagraph** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visSpaceBefore** <br/> |
   

