---
title: Y, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Représente la valeur y-coordonnées d’un point de connexion dans le système de coordonnées local.
ms.openlocfilehash: 270ae98789e29ca170f260aa70e951d4b2af2962
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790065"
---
# <a name="y-cell-connection-points-section"></a>Y, cellule (section Connection Points)

Représente la valeur *y* -coordonnées d’un point de connexion dans le système de coordonnées local. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Y par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Connections.Y *i* où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Y par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
| Index de la ligne :  <br/> |**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visY** <br/> |
   

