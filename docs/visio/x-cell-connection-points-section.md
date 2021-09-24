---
title: X, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
ms.localizationpriority: medium
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Représente la coordonnée x d’un point de connexion dans les coordonnées locales.
ms.openlocfilehash: 5703cd13e6679a97cfdd576e1972e806d3353a39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549300"
---
# <a name="x-cell-connection-points-section"></a>X, cellule (section Connection Points)

Représente la  *coordonnée x d’un*  point de connexion dans les coordonnées locales. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Connections.X  *i*            où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionConnectionPts** <br/> |
| Index de la ligne :  <br/> |**visRowConnectionPts**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visX** <br/> |
   

