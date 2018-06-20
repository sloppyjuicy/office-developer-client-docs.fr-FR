---
title: X, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Représente le x-coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local.
ms.openlocfilehash: e47b26c72709a2ee74675e73b8e8424bbfb325e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790056"
---
# <a name="x-cell-controls-section"></a>X, cellule (section Controls)

Représente le *x* -coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom* . X où contrôle.  *nom* est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule X par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlX** <br/> |
   

