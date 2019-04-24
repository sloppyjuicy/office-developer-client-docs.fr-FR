---
title: RightMargin, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Définit la distance séparant le bord droit du bloc de texte du texte qui y figure. La valeur par défaut est 2,54 mm.
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326774"
---
# <a name="rightmargin-cell-text-block-format-section"></a>RightMargin, cellule (section Text Block Format)

Définit la distance séparant le bord droit du bloc de texte du texte qui y figure. La valeur par défaut est 2,54 mm.
  
## <a name="remarks"></a>Remarques

Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge droite ne change pas.
  
Pour obtenir une référence à la cellule RightMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | RightMargin  <br/> |
   
Pour obtenir une référence à la cellule RightMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowText** <br/> |
| Index de la cellule :  <br/> |**visTxtBlkRightMargin** <br/> |
   

