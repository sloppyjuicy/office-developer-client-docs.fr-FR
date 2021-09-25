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
ms.openlocfilehash: bd20175567010aafd2e2a88ebdf5722032f5624e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559544"
---
# <a name="size-cell-character-section"></a>Size, cellule (section Character)

Détermine la taille de la police figurant dans le bloc de texte d'une forme.
  
## <a name="remarks"></a>Remarques

La taille de la police est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la taille de la police ne change pas.
  
Pour obtenir une référence à la cellule Size par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.Size[  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Size par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCharacterSize** <br/> |
   

