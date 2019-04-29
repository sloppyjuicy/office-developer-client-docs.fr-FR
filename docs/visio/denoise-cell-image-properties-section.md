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
ms.openlocfilehash: f970fde22e864239ea3f3f9bcb704e7f4692e9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415802"
---
# <a name="denoise-cell-image-properties-section"></a>Denoise, cellule (section Image Properties)

Supprime le bruit (pixels comportant des niveaux de couleur répartis de façon aléatoire) d'une image en mode point. La valeur par défaut est 0 %.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Denoise par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Noise  <br/> |
   
Pour obtenir une référence à la cellule Denoise à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowImage** <br/> |
| Index de la cellule :  <br/> |**visImageDenoise** <br/> |
   

