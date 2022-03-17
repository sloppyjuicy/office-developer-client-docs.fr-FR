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
ms.openlocfilehash: 75b02daa7c3a392510bbc7b1864c02ebeed5b85a
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522414"
---
# <a name="hidetext-cell-miscellaneous-section"></a>HideText, cellule (section Miscellaneous)

Masque le texte d'une forme. Vous pouvez visualiser le texte, modifier ses propriétés et lui appliquer des styles dans le bloc de texte, mais les modifications n'apparaîtront pas tant que vous ne rétablirez pas la cellule sur FALSE (0).
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Le texte est masqué et ne s'imprime pas. |
| FALSE  <br/> | Le texte n'est pas masqué. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule HideText par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | HideText  <br/> |
   
Pour obtenir une référence à la cellule HideText à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowMisc** <br/> |
| **Index de la cellule :**  <br/> |**visHideText** <br/> |
   

