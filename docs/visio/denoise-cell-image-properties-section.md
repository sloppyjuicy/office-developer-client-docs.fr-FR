---
title: Denoise, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Supprime le bruit (pixels comportant des niveaux de couleur répartis de façon aléatoire) d'une image en mode point. La valeur par défaut est 0 %.
ms.openlocfilehash: f08d09126a24935c0dd4dcda5e88fdd559c8d176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788474"
---
# <a name="denoise-cell-image-properties-section"></a>Denoise, cellule (section Image Properties)

Supprime le bruit (pixels comportant des niveaux de couleur répartis de façon aléatoire) d'une image en mode point. La valeur par défaut est 0 %.
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Denoise par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Denoise  <br/> |
   
Pour obtenir une référence à la cellule Denoise par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowImage** <br/> |
| Index de la cellule :  <br/> |**visImageDenoise** <br/> |
   

