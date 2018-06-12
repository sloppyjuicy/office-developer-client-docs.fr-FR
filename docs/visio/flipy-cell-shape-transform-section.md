---
title: FlipY, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Indique si la forme a été retournée verticalement.
ms.openlocfilehash: 42ee740a13c3f447f5cd4a6caa9959189320a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788644"
---
# <a name="flipy-cell-shape-transform-section"></a>FlipY, cellule (section Shape Transform)

Indique si la forme a été retournée verticalement.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La forme a été retournée verticalement.  <br/> |
| FALSE  <br/> | La forme n'a pas été retournée verticalement.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule FlipY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | FlipY  <br/> |
   
Pour obtenir une référence à la cellule FlipY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormFlipY** <br/> |
   

