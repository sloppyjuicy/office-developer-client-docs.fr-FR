---
title: LeftMargin, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
ms.localizationpriority: medium
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Définit la distance entre le bord gauche du bloc de texte et le texte qui y figure. La valeur par défaut est de 2,5 mm. Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge gauche ne change pas.
ms.openlocfilehash: 57dcc1a0b99a8fc3d2a205555ccbee5520b1dac7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618678"
---
# <a name="leftmargin-cell-text-block-format-section"></a>LeftMargin, cellule (section Text Block Format)

Définit la distance entre le bord gauche du bloc de texte et le texte qui y figure. La valeur par défaut est de 2,5 mm. Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge gauche ne change pas.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LeftMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LeftMargin  <br/> |
   
Pour obtenir une référence à la cellule LeftMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowText** <br/> |
| Index de la cellule :  <br/> |**visTxtBlkLeftMargin** <br/> |
   

