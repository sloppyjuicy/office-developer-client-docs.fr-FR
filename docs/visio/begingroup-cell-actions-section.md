---
title: BeginGroup, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
ms.localizationpriority: medium
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Indique si un séparateur est inséré dans le menu au-dessus de cette action.
ms.openlocfilehash: 7f6ce3836cf71adcdb7135c390abc84834d57fad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616025"
---
# <a name="begingroup-cell-actions-section"></a>BeginGroup, cellule (section Actions)

Indique si un séparateur est inséré dans le menu au-dessus de cette action. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Un séparateur est inséré dans le menu au-dessus de cette action.  <br/> |
|FALSE  <br/> |Aucun séparateur n'est inséré dans le menu au-dessus de cette action (la valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule BeginGroup par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Actions. *nom*. BeginGroup où Actions. *nom* est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule BeginGroup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionBeginGroup** <br/> |
   

