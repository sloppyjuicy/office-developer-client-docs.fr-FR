---
title: Denoise, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
ms.localizationpriority: medium
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: Supprime le bruit (pixels comportant des niveaux de couleur répartis de façon aléatoire) d'une image en mode point. La valeur par défaut est 0 %.
ms.openlocfilehash: 33ade61e43ef6e9dae2558386627f301d450889b
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63508135"
---
# <a name="denoise-cell-image-properties-section"></a>Denoise, cellule (section Image Properties)

Supprime le bruit (pixels comportant des niveaux de couleur répartis de façon aléatoire) d'une image en mode point. La valeur par défaut est 0 %.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Denoise par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | Denoise  <br/> |
   
Pour obtenir une référence à la cellule Denoise à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowImage** <br/> |
| **Index de la cellule :**  <br/> |**visImageDenimageDenimage** <br/> |
   

