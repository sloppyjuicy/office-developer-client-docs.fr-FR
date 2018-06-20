---
title: BeginGroup, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Indique si un séparateur est inséré dans le menu au-dessus de cette action.
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788048"
---
# <a name="begingroup-cell-actions-section"></a>BeginGroup, cellule (section Actions)

Indique si un séparateur est inséré dans le menu au-dessus de cette action. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Un séparateur est inséré dans le menu au-dessus de cette action.  <br/> |
|FALSE  <br/> |Un séparateur n’est pas inséré dans le menu au-dessus de cette action (la valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule BeginGroup par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Actions. *nom*. BeginGroup où Actions. *nom* est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule BeginGroup par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionBeginGroup** <br/> |
   

