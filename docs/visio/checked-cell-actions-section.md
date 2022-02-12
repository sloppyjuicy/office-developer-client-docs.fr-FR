---
title: Checked, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
ms.localizationpriority: medium
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Indique si une option est cochée dans le menu contextuel ou de balise d’action.
ms.openlocfilehash: 7d2fc15a8609d1d6b010353b3a5a5ad8728b7078
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772941"
---
# <a name="checked-cell-actions-section"></a>Checked, cellule (section Actions)

Indique si une option est cochée dans le menu contextuel ou de balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |La coche est affichée. |
|FALSE  <br/> |La coche n'est pas affichée (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Checked à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Actions. *nom*  . Checked where Actions. *name*  est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule Checked à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +   *i* où *i* = 0, 1, 2, ... |
|Index de la cellule :  <br/> |**visActionChecked** <br/> |
   

