---
title: X Dynamics, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Représente le x-coordonnées d’un point d’ancrage d’une poignée de contrôle dans le système de coordonnées local.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790080"
---
# <a name="x-dynamics-cell-controls-section"></a>X Dynamics, cellule (section Controls)

Représente le *x* -coordonnées d’un point d’ancrage d’une poignée de contrôle dans le système de coordonnées local. 
  
## <a name="remarks"></a>Remarques

Le point d'ancrage est utilisé pour l'étirement dynamique des formes.
  
Pour obtenir une référence à la cellule X Dynamics par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom* . Contrôles XDynwhere.  *nom* est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule X Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlXDyn** <br/> |
   

