---
title: HideText, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
ms.localizationpriority: medium
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Masque le texte d'une forme. Vous pouvez visualiser le texte, modifier ses propriétés et lui appliquer des styles dans le bloc de texte, mais les modifications n'apparaîtront pas tant que vous ne rétablirez pas la cellule sur FALSE (0).
ms.openlocfilehash: 92e5285d224a7e2c8d43afd38b235cae1e920b1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574103"
---
# <a name="hidetext-cell-miscellaneous-section"></a>HideText, cellule (section Miscellaneous)

Masque le texte d'une forme. Vous pouvez visualiser le texte, modifier ses propriétés et lui appliquer des styles dans le bloc de texte, mais les modifications n'apparaîtront pas tant que vous ne rétablirez pas la cellule sur FALSE (0).
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le texte est masqué et ne s'imprime pas.  <br/> |
| FALSE  <br/> | Le texte n'est pas masqué.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule HideText par un nom à partir d’une autre formule ou d’un programme en faisant appel à la **propriété CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | HideText  <br/> |
   
Pour obtenir une référence à la cellule HideText à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visHideText** <br/> |
   

