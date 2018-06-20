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
description: Spécifie le texte descriptif ou d’instructions qui apparaît comme une info-bulle lorsque vous positionnez la souris sur une valeur dans la fenêtre données de forme.
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789355"
---
# <a name="prompt-cell-shape-data-section"></a>Prompt, cellule (section Shape Data)

Spécifie le texte descriptif ou d’instructions qui apparaît comme une info-bulle lorsque vous positionnez la souris sur une valeur dans la fenêtre **Données de forme** . 
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Prompt par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Propriétés.  *Nom* . Invite où *nom* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Prompt par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionProp** <br/> |
| Index de la ligne :  <br/> |**visRowProp +** *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visCustPropsPrompt** <br/> |
   

