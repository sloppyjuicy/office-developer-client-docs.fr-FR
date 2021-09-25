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
ms.openlocfilehash: d3756a3077d91e5068fda35e01e304ed3ba39aee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582833"
---
# <a name="disabled-cell-actions-section"></a>Disabled, cellule (section Actions)

Indique si une option d’un menu contextuel ou de balise d’action est désactivée.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Désactive (fait apparaître en grisé) le nom de la commande.  <br/> |
|FALSE  <br/> |Active le nom de la commande (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Disabled à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Actions. *nom*  . Désactivation de l’endroit où Actions. *name*  est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule Disabled à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionDisabled** <br/> |
   

