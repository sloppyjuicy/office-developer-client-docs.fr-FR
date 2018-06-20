---
title: DirX / A, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Détermine le x-composant requis vecteur d’alignement d’un point de connexion correspondant. Le DirX / une cellule est également utilisée pour orienter la branche reliée d’un connecteur dynamique. Cette cellule prend flottante valeur du point.
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788492"
---
# <a name="dirx--a-cell-connection-points-section"></a>DirX / A, cellule (section Connection Points)

Détermine le *x* -composant requis vecteur d’alignement d’un point de connexion correspondant. Le DirX / une cellule est également utilisée pour orienter la branche reliée d’un connecteur dynamique. Cette cellule prend flottante valeur du point. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la DirX / une cellule par un nom à partir d’une autre formule ou d’un programme à l’aide de la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Connections.DirX [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la DirX / une cellule par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
| Index de la ligne :  <br/> |**visRowConnectionPts** +  *i* où *i* = 0, 1, 2  <br/> |
| Index de la cellule :  <br/> |**visCnnctDirX** (lignes non étendues)           **visCnnctA** (lignes étendues)  <br/> |
   
Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.
  

