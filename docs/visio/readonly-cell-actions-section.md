---
title: ReadOnly, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule.
ms.openlocfilehash: bf2d0f7e50a3126611662af8e068485986c26a13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789391"
---
# <a name="readonly-cell-actions-section"></a>ReadOnly, cellule (section Actions)

Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |L'action apparaît dans le menu mais est en lecture seule.  <br/> |
|FALSE  <br/> |L'action apparaît dans le menu et peut être sélectionnée (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Note

Lorsqu’une action est en lecture seule, il apparaît dans le menu contextuel ou de balise d’action, mais vous ne pouvez pas le sélectionner. Il n’est pas grisée mais apparaît sur un fond de couleur, comme une étiquette. Pour rendre l’élément de menu apparaît estompé, utilisez la cellule Disabled. 
  
Pour obtenir une référence à la cellule ReadOnly par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Actions. *nom* . Actions ReadOnlywhere.  *nom* est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule ReadOnly par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionReadOnly** <br/> |
   

