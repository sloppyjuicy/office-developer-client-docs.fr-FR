---
title: Can Glue, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Détermine si une poignée de contrôle peut être collée à d'autres formes.
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788176"
---
# <a name="can-glue-cell-controls-section"></a>Can Glue, cellule (section Controls)

Détermine si une poignée de contrôle peut être collée à d'autres formes.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La poignée de contrôle peut être collée.  <br/> |
| FALSE  <br/> | La poignée de contrôle ne peut pas être collée.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Can Glue par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Contrôles.  *nom* . Contrôles CanGluewhere.  *nom* est le nom de la ligne des contrôles.  <br/> |
   
Pour obtenir une référence à la cellule Can Glue par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +  *i* où *i* = 0, 1, 2,...  <br/> |
| Index de la cellule :  <br/> |**visCtlGlue** <br/> |
   

