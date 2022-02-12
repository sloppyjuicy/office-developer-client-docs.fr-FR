---
title: Disabled, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
ms.localizationpriority: medium
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Indique si une option d’un menu contextuel ou de balise d’action est désactivée.
ms.openlocfilehash: 7b1d6d61325a6612117e14b637c1f1d2d02828a1
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771621"
---
# <a name="disabled-cell-actions-section"></a>Disabled, cellule (section Actions)

Indique si une option d’un menu contextuel ou de balise d’action est désactivée.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Désactive (fait apparaître en grisé) le nom de la commande. |
|FALSE  <br/> |Active le nom de la commande (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Disabled à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Actions. *nom*  . Désactivé lorsque Actions. *name*  est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule Disabled à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visActionDisabled** <br/> |
   

