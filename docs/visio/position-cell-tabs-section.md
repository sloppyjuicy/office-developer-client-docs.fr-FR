---
title: Position, cellule (section Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
ms.localizationpriority: medium
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Définit la position d'une tabulation. La position de la tabulation est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la position de la tabulation ne change pas.
ms.openlocfilehash: 40cf12b3b2cbbbc0a2ade8055880b4188f09804c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573739"
---
# <a name="position-cell-tabs-section"></a>Position, cellule (section Tabs)

Définit la position d'une tabulation. La position de la tabulation est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la position de la tabulation ne change pas.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Position par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Onglets.  *ij*            où  *i*  et  *j*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Position à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTab** <br/> |
| Index de la ligne :  <br/> |**visRowTab**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> | (*j*  *3) + **visTabPos** <br/> |
   

