---
title: BulletSize, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
ms.localizationpriority: medium
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Indique la taille d'une puce.
ms.openlocfilehash: 97f22bc3e4071757de1336dca2efd2b4f1e12c41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623543"
---
# <a name="bulletsize-cell-paragraph-section"></a>BulletSize, cellule (section Paragraph)

Indique la taille d'une puce. 
  
## <a name="remarks"></a>Remarques

Cette valeur peut être spécifiée pour des puces prédéfinies ou personnalisées, sous forme de pourcentage ou de valeur spécifique. 
  
Si la valeur est zéro (0), la puce a la même taille de police que celle du premier caractère du paragraphe. Si la valeur est un pourcentage, la puce a pour taille un pourcentage de la taille de police du premier caractère du paragraphe. Les nombres négatifs sont traités comme des pourcentages.
  
Pour obtenir une référence à la cellule BulletSize par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para.BulletFontSize[  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule BulletSize à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visBulletFontSize** <br/> |
   

