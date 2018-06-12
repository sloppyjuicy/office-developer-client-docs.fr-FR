---
title: Size, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Détermine la taille de la police figurant dans le bloc de texte d'une forme.
ms.openlocfilehash: f3077441844b859cf224eccc8180d0d56cce851f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789743"
---
# <a name="size-cell-character-section"></a>Size, cellule (section Character)

Détermine la taille de la police figurant dans le bloc de texte d'une forme.
  
## <a name="remarks"></a>Note

La taille de la police est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la taille de la police ne change pas.
  
Pour obtenir une référence à la cellule Size par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.Size [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Size par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCharacterSize** <br/> |
   

