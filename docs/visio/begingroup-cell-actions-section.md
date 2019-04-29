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
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407836"
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
|Nom de cellule :  <br/> |Mesures. *nom*. BeginGroup, où actions. *nom* est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule BeginGroup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionBeginGroup** <br/> |
   

