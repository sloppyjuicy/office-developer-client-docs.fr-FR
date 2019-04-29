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
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414549"
---
# <a name="angle-cell-shape-transform-section"></a>Cellule Angle (section Shape Transform)

Représente l'angle de rotation actuel de la forme par rapport à son parent. La formule par défaut déterminant l'angle de rotation d'une forme 1D est : =ATAN2(EndY-BeginY,EndX-BeginX).
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Angle par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Angle  <br/> |
   
Pour obtenir une référence à la cellule Angle à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormAngle** <br/> |
   

