---
title: EndTrigger, cellule (section Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251331
localization_priority: Normal
ms.assetid: 8dc6515b-66ab-f1ac-18fd-820209f90991
description: Contient une formule de déclenchement générée par l'application qui détermine si le point de fin d'une forme 1D doit être déplacé pour maintenir son lien à une autre forme.
ms.openlocfilehash: 9093cca782d9262b2511198ed73f512a75bb8994
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329061"
---
# <a name="endtrigger-cell-glue-info-section"></a>EndTrigger, cellule (section Glue Info)

Contient une formule de déclenchement générée par l'application qui détermine si le point de fin d'une forme 1D doit être déplacé pour maintenir son lien à une autre forme.
  
## <a name="remarks"></a>Remarques

Lorsque vous collez une forme 1D à une autre de façon dynamique, Visio génère une formule qui fait référence à la cellule EventXFMod de l'autre forme. Lorsque cette forme est modifiée, Visio recalcule toutes les formules faisant référence à sa cellule EventXFMod, y compris la formule de la cellule EndTrigger. Les autres formules de la forme 1D font référence à la cellule EndTrigger et déplacent le point de fin de la forme 1D ou modifient la forme en conséquence.
  
Pour obtenir une référence à la cellule EndTrigger par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | EndTrigger  <br/> |
   
Pour obtenir une référence à la cellule EndTrigger à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visEndTrigger** <br/> |
   

