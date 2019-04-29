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
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423292"
---
# <a name="can-glue-cell-controls-section"></a>Can Glue, cellule (section Controls)

Détermine si une poignée de contrôle peut être collée à d'autres formes.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La poignée de contrôle peut être collée.  <br/> |
| FALSE  <br/> | La poignée de contrôle ne peut pas être collée.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Can Glue par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Vérifie.  *nom* . Contrôles CanGluewhere.  *Name* est le nom de la ligne Controls.  <br/> |
   
Pour obtenir une référence à la cellule Can Glue à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionControls** <br/> |
| Index de la ligne :  <br/> |**visRowControl** +  *i* où *i* = 0, 1, 2,...  <br/> |
| Index de la cellule :  <br/> |**visCtlGlue** <br/> |
   

