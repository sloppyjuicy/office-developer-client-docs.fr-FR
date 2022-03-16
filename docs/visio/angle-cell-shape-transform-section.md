---
title: Cellule Angle (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
ms.localizationpriority: medium
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: "Représente l'angle de rotation actuel de la forme par rapport à son parent. La formule par défaut déterminant l'angle de rotation d'une forme 1D est : =ATAN2(EndY-BeginY,EndX-BeginX)."
ms.openlocfilehash: 07eedfe41335a9e46ff415254cf8b2dfcc45d5de
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63508270"
---
# <a name="angle-cell-shape-transform-section"></a>Cellule Angle (section Shape Transform)

Représente l'angle de rotation actuel de la forme par rapport à son parent. La formule par défaut déterminant l'angle de rotation d'une forme 1D est : =ATAN2(EndY-BeginY,EndX-BeginX).
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Angle par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | Angle  <br/> |
   
Pour obtenir une référence à la cellule Angle à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowXFormOut** <br/> |
| **Index de la cellule :**  <br/> |**visXFormAngle** <br/> |
   

