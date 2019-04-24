---
title: HideText, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Masque le texte d'une forme. Vous pouvez visualiser le texte, modifier ses propriétés et lui appliquer des styles dans le bloc de texte, mais les modifications n'apparaîtront pas tant que vous ne rétablirez pas la cellule sur FALSE (0).
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329959"
---
# <a name="hidetext-cell-miscellaneous-section"></a>HideText, cellule (section Miscellaneous)

Masque le texte d'une forme. Vous pouvez visualiser le texte, modifier ses propriétés et lui appliquer des styles dans le bloc de texte, mais les modifications n'apparaîtront pas tant que vous ne rétablirez pas la cellule sur FALSE (0).
  
|**Value**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le texte est masqué et ne s'imprime pas.  <br/> |
| FALSE  <br/> | Le texte n'est pas masqué.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule HideText par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | HideText  <br/> |
   
Pour obtenir une référence à la cellule HideText à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visHideText** <br/> |
   

