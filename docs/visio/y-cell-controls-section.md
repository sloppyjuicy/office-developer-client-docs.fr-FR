---
title: Y, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Représente la valeur y-coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local.
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790076"
---
# <a name="y-cell-controls-section"></a>Y, cellule (section Controls)

Représente la valeur *y* -coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom* . Contrôles Ywhere.  *nom* est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule Y par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCtlY** <br/> |
   

