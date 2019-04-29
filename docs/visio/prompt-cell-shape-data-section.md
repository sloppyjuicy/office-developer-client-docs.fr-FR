---
title: Prompt, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Contient la description ou l’instruction qui apparaît sous la forme d’un conseil lorsque vous positionnez la souris sur la valeur dans la fenêtre Données de forme.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405484"
---
# <a name="prompt-cell-shape-data-section"></a>Prompt, cellule (section Shape Data)

Contient la description ou l’instruction qui apparaît sous la forme d’un conseil lorsque vous positionnez la souris sur la valeur dans la fenêtre **Données de forme**. 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Prompt par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Hélice.  *Nom* . Invite où *nom* est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Prompt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp +** *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsPrompt** <br/> |
   

