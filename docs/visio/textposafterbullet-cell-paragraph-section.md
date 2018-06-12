---
title: TextPosAfterBullet, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Représente la distance entre la première ligne du paragraphe et la puce.
ms.openlocfilehash: fe22b81113ab6537922ad4627aa53f34f2e62c48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789877"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>TextPosAfterBullet, cellule (section Paragraph)

Représente la distance entre la première ligne du paragraphe et la puce. 
  
## <a name="remarks"></a>Note

Cette distance est ajoutée à celle contenue dans la cellule IndFirst, qui est le retrait gauche par défaut. Cette valeur est indépendante de l'échelle du dessin. 
  
Pour obtenir une référence à la cellule TextPosAfterBullet par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.TextPosAfterBullet [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule TextPosAfterBullet par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visTextPosAfterBullet** <br/> |
   

