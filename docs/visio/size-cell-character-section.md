---
title: Size, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
ms.localizationpriority: medium
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Détermine la taille de la police figurant dans le bloc de texte d'une forme.
ms.openlocfilehash: 796ab5aa8d7730d4cc23ebb9351cf66e770211b5
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520279"
---
# <a name="size-cell-character-section"></a>Size, cellule (section Character)

Détermine la taille de la police figurant dans le bloc de texte d'une forme.
  
## <a name="remarks"></a>Remarques

La taille de la police est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la taille de la police ne change pas.
  
Pour obtenir une référence à la cellule Size par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Char.Size[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule Size par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionCharacter** <br/> |
| **Index de la ligne :**  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visCharacterSize** <br/> |
   

