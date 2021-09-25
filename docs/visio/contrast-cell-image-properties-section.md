---
title: Contrast, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm200
ms.localizationpriority: medium
ms.assetid: f0e4c644-c646-9649-c697-82feb02f5e29
description: Règle le contraste d'une image bitmap. Réduisez le contraste de l'image en entrant une valeur comprise entre 0 et 49 % ou augmentez-le en entrant une valeur comprise entre 51 et 100 %. La valeur par défaut est 50 %.
ms.openlocfilehash: 8e75daa36658cffa9f6c4dd26b2543d74086c4c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628569"
---
# <a name="contrast-cell-image-properties-section"></a>Contrast, cellule (section Image Properties)

Règle le contraste d'une image bitmap. Réduisez le contraste de l'image en entrant une valeur comprise entre 0 et 49 % ou augmentez-le en entrant une valeur comprise entre 51 et 100 %. La valeur par défaut est 50 %.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Contrast par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrast  <br/> |
   
Pour obtenir une référence à la cellule Contrast à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowImage** <br/> |
| Index de la cellule :  <br/> |**visImageContrast** <br/> |
   

