---
title: IndFirst, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
ms.localizationpriority: medium
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Représente la distance entre la première ligne de chaque paragraphe du bloc de texte et le retrait gauche du paragraphe. Cette valeur est indépendante de l'échelle de dessin. Elle ne change pas si le dessin est mis à l'échelle.
ms.openlocfilehash: 16b3d13afa81958d1b428b417c28683441703fd9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612602"
---
# <a name="indfirst-cell-paragraph-section"></a>IndFirst, cellule (section Paragraph)

Représente la distance entre la première ligne de chaque paragraphe du bloc de texte et le retrait gauche du paragraphe. Cette valeur est indépendante de l'échelle de dessin. Elle ne change pas si le dessin est mis à l'échelle.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule IndFirst par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.IndFirst[  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule IndFirst à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visIndentFirst** <br/> |
   

