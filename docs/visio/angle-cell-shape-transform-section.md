---
title: Cellule Angle (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: "Représente l'angle de rotation actuel de la forme par rapport à son parent. La formule par défaut déterminant l'angle de rotation d'une forme 1D est : =ATAN2(EndY-BeginY,EndX-BeginX)."
ms.openlocfilehash: ff052c5b254f9b49a97f5d362a4643e16a27b85d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788014"
---
# <a name="angle-cell-shape-transform-section"></a>Cellule Angle (section Shape Transform)

Représente l'angle de rotation actuel de la forme par rapport à son parent. La formule par défaut déterminant l'angle de rotation d'une forme 1D est : =ATAN2(EndY-BeginY,EndX-BeginX).
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Angle par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Angle  <br/> |
   
Pour obtenir une référence à la cellule Angle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormAngle** <br/> |
   

