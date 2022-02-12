---
title: IndLeft, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
ms.localizationpriority: medium
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: "Représente la distance entre chaque ligne du paragraphe et la marge gauche du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle."
ms.openlocfilehash: 1fcf33c928c7ece891adec3cd754a6892f750a92
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787162"
---
# <a name="indleft-cell-paragraph-section"></a>IndLeft, cellule (section Paragraph)

Représente la distance entre chaque ligne du paragraphe et la marge gauche du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule IndLeft par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.IndLeft[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule IndLeft à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visIndentLeft** <br/> |
   

