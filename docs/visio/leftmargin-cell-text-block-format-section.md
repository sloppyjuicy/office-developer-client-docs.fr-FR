---
title: LeftMargin, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Définit la distance entre le bord gauche du bloc de texte et le texte qui y figure. La valeur par défaut est de 2,5 mm. Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge gauche ne change pas.
ms.openlocfilehash: d24ba33bffea1529490b49e105fec5d01cd828b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788931"
---
# <a name="leftmargin-cell-text-block-format-section"></a>LeftMargin, cellule (section Text Block Format)

Définit la distance entre le bord gauche du bloc de texte et le texte qui y figure. La valeur par défaut est de 2,5 mm. Cette valeur est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la marge gauche ne change pas.
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LeftMargin par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LeftMargin  <br/> |
   
Pour obtenir une référence à la cellule LeftMargin par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowText** <br/> |
| Index de la cellule :  <br/> |**visTxtBlkLeftMargin** <br/> |
   

