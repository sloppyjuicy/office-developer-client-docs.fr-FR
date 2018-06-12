---
title: Position, cellule (section Tabs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Définit la position d'une tabulation. La position de la tabulation est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la position de la tabulation ne change pas.
ms.openlocfilehash: 06f3a9fd5cfdf78f5383e70f32f8514b0adab114
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789350"
---
# <a name="position-cell-tabs-section"></a>Position, cellule (section Tabs)

Définit la position d'une tabulation. La position de la tabulation est indépendante de l'échelle du dessin. Si le dessin est mis à l'échelle, la position de la tabulation ne change pas.
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Position par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Onglets.  *ij* où *i* et *j* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Position par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTab** <br/> |
| Index de la ligne :  <br/> |**visRowTab** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> | (*j* * 3) + **visTabPos** <br/> |
   

