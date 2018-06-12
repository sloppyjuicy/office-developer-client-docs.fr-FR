---
title: IndLeft, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: "Représente la distance entre chaque ligne du paragraphe et la marge gauche du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle."
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788824"
---
# <a name="indleft-cell-paragraph-section"></a>IndLeft, cellule (section Paragraph)

Représente la distance entre chaque ligne du paragraphe et la marge gauche du bloc de texte. Cette valeur est indépendante de l'échelle de dessin : elle ne change pas si le dessin est mis à l'échelle.
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule IndLeft par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.IndLeft [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule IndLeft par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visIndentLeft** <br/> |
   

