---
title: BulletSize, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Indique la taille d'une puce.
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788168"
---
# <a name="bulletsize-cell-paragraph-section"></a>BulletSize, cellule (section Paragraph)

Indique la taille d'une puce. 
  
## <a name="remarks"></a>Remarques

Cette valeur peut être spécifiée pour des puces prédéfinies ou personnalisées, sous forme de pourcentage ou de valeur spécifique. 
  
Si la valeur est égale à zéro (0), la puce est la même taille que celle du premier caractère du paragraphe. Si la valeur est un pourcentage, la puce est dimensionnée sous forme de pourcentage de la taille de police du premier caractère du paragraphe. Les nombres négatifs sont traités comme des pourcentages.
  
Pour obtenir une référence à la cellule BulletSize par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.BulletFontSize [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule BulletSize par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visBulletFontSize** <br/> |
   

