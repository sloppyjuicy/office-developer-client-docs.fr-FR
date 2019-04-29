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
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405421"
---
# <a name="bulletsize-cell-paragraph-section"></a>BulletSize, cellule (section Paragraph)

Indique la taille d'une puce. 
  
## <a name="remarks"></a>Remarques

Cette valeur peut être spécifiée pour des puces prédéfinies ou personnalisées, sous forme de pourcentage ou de valeur spécifique. 
  
Si la valeur est égale à zéro (0), la puce est de la même taille de police que le premier caractère du paragraphe. Si la valeur est un pourcentage, la puce a pour taille un pourcentage de la taille de police du premier caractère du paragraphe. Les nombres négatifs sont traités comme des pourcentages.
  
Pour obtenir une référence à la cellule BulletSize par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Para. BulletFontSize [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule BulletSize à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionParagraph** <br/> |
| Index de la ligne :  <br/> |**visRowParagraph** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visBulletFontSize** <br/> |
   

