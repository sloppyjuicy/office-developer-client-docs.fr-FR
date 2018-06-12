---
title: Disabled, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Indique si une option d’un menu contextuel ou de balise d’action est désactivée.
ms.openlocfilehash: 3956b6cf5ccb870255d6943e74b4f02650952d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788468"
---
# <a name="disabled-cell-actions-section"></a>Disabled, cellule (section Actions)

Indique si une option d’un menu contextuel ou de balise d’action est désactivée.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Désactive (fait apparaître en grisé) le nom de la commande.  <br/> |
|FALSE  <br/> |Active le nom de la commande (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Disabled par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Actions. *nom* . Désactivé où Actions. *nom* est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule Disabled par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionDisabled** <br/> |
   

