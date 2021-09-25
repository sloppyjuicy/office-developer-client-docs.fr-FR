---
title: TextPosAfterBullet, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
ms.localizationpriority: medium
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Représente la distance entre la première ligne du paragraphe et la puce.
ms.openlocfilehash: 7568babf9d23c1055ce4a68955b43cb98c02f94b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559401"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>TextPosAfterBullet, cellule (section Paragraph)

Représente la distance entre la première ligne du paragraphe et la puce. 
  
## <a name="remarks"></a>Remarques

Cette distance est ajoutée à celle contenue dans la cellule IndFirst, qui est le retrait gauche par défaut. Cette valeur est indépendante de l'échelle du dessin. 
  
Pour obtenir une référence à la cellule TextPosAfterBullet à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.TextPosAfterBullet[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule TextPosAfterBullet à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visTextPosAfterBullet** <br/> |
   

