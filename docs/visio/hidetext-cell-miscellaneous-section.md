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
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788782"
---
# <a name="hidetext-cell-miscellaneous-section"></a>HideText, cellule (section Miscellaneous)

Masque le texte d'une forme. Vous pouvez visualiser le texte, modifier ses propriétés et lui appliquer des styles dans le bloc de texte, mais les modifications n'apparaîtront pas tant que vous ne rétablirez pas la cellule sur FALSE (0).
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le texte est masqué et ne s'imprime pas.  <br/> |
| FALSE  <br/> | Le texte n'est pas masqué.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule HideText par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | HideText  <br/> |
   
Pour obtenir une référence à la cellule HideText par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visHideText** <br/> |
   

