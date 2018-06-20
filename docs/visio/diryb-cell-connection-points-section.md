---
title: DirY / B, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Détermine la valeur y-composant requis vecteur d’alignement d’un point de connexion correspondant. Il est également utilisé pour orienter la branche reliée d’un connecteur dynamique. Cette cellule prend flottante valeur du point.
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788463"
---
# <a name="diry--b-cell-connection-points-section"></a>DirY / B, cellule (section Connection Points)

Détermine la valeur *y* -composant requis vecteur d’alignement d’un point de connexion correspondant. Il est également utilisé pour orienter la branche reliée d’un connecteur dynamique. Cette cellule prend flottante valeur du point. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la DirY / B, cellule par un nom à partir d’une autre formule ou d’un programme à l’aide de la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Connections.DirY [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la DirY / B, cellule par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
|Index de la ligne :  <br/> |**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visCnnctDirY** (lignes non étendues)           **visCnnctB** (lignes étendues)  <br/> |
   
Pour plus d'informations sur les lignes non étendues et étendues, reportez-vous à la ligne Connection Points.
  

