---
title: ReadOnly, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
ms.localizationpriority: medium
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule.
ms.openlocfilehash: 6f9e2dd875687aa626775e1adbc2df659a663ae1
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774054"
---
# <a name="readonly-cell-actions-section"></a>ReadOnly, cellule (section Actions)

Contrôle si l’action d’un menu contextuel ou de balise d’action est en lecture seule. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |L'action apparaît dans le menu mais est en lecture seule. |
|FALSE  <br/> |L'action apparaît dans le menu et peut être sélectionnée (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

Lorsqu’une action est en lecture seule, elle apparaît dans le menu contextuel ou de balise d’action, mais vous ne pouvez pas la sélectionner. Elle n’est pas grisée, mais apparaît sur un arrière-plan de couleur, comme une étiquette. Pour griser l’option de menu, utilisez la cellule Disabled. 
  
Pour obtenir une référence à la cellule ReadOnly à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Actions. *nom*  . ReadOnlywhere Actions.  *name*  est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule ReadOnly à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visActionReadOnly** <br/> |
   

