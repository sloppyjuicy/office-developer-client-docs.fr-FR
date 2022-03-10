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
ms.openlocfilehash: 034135b128bfc8cddcd73b9be360e28fa4119181
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426950"
---
# <a name="begingroup-cell-actions-section"></a>BeginGroup, cellule (section Actions)

Indique si un séparateur est inséré dans le menu au-dessus de cette action. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Un séparateur est inséré dans le menu au-dessus de cette action. |
|FALSE  <br/> |Aucun séparateur n'est inséré dans le menu au-dessus de cette action (la valeur par défaut). |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule BeginGroup par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Actions. *nom*. BeginGroup où Actions. *nom* est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule BeginGroup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionAction** <br/> |
|**Index de la ligne :**  <br/> |**visRowAction** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visActionBeginGroup** <br/> |
   

