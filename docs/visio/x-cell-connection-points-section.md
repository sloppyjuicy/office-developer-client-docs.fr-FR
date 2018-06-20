---
title: X, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Représente le x-coordonnées d’un point de connexion dans le système de coordonnées local.
ms.openlocfilehash: 27821f9aa94f97d8e019d7c7307c036549bf807b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790051"
---
# <a name="x-cell-connection-points-section"></a>X, cellule (section Connection Points)

Représente le *x* -coordonnées d’un point de connexion dans le système de coordonnées local. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Connections.X *i* où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule X par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
| Index de la ligne :  <br/> |**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visX** <br/> |
   

