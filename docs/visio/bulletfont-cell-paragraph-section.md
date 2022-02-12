---
title: BulletFont, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
ms.localizationpriority: medium
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Représente le numéro de la police utilisée pour mettre en forme le texte lorsqu'une chaîne de puces personnalisée est spécifiée et que la valeur dans la cellule Bullet est non nulle.
ms.openlocfilehash: 7b29ee44734fce2b622971e531d6c88a7c022a97
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771796"
---
# <a name="bulletfont-cell-paragraph-section"></a>BulletFont, cellule (section Paragraph)

Représente le numéro de la police utilisée pour mettre en forme le texte lorsqu'une chaîne de puces personnalisée est spécifiée et que la valeur dans la cellule Bullet est non nulle. 
  
## <a name="remarks"></a>Remarques

Les numéros de police varient en fonction des polices installées sur votre système. Si la valeur est 0 et s'il y a une chaîne de puces personnalisée, la police utilisée est la même que la police du premier caractère du paragraphe.
  
Pour obtenir une référence à la cellule BulletFont par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.BulletFont[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule BulletFont à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visBulletFont** <br/> |
   

