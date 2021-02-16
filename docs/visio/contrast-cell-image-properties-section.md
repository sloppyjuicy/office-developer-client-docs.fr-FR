---
title: Contrast, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm200
localization_priority: Normal
ms.assetid: f0e4c644-c646-9649-c697-82feb02f5e29
description: Règle le contraste d'une image bitmap. Réduisez le contraste de l'image en entrant une valeur comprise entre 0 et 49 % ou augmentez-le en entrant une valeur comprise entre 51 et 100 %. La valeur par défaut est 50 %.
ms.openlocfilehash: f0a27090ea1ec96bf11726ae641ff918dd581e2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404924"
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
   

