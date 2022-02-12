---
title: Invisible, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
ms.localizationpriority: medium
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Indique si l’action est visible dans le menu contextuel ou de balise d’action.
ms.openlocfilehash: 5ee2e87b18afa187ad64d3d443d4c70837b8a62f
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775723"
---
# <a name="invisible-cell-actions-section"></a>Invisible, cellule (section Actions)

Indique si l’action est visible dans le menu contextuel ou de balise d’action. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |L'action n'est pas visible dans le menu. |
|FALSE  <br/> |L'action est visible dans le menu (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Invisible à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Actions. *nom*  . Invisibleoù Actions.  *name*  est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule Invisible à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visActionInvisible** <br/> |
   

