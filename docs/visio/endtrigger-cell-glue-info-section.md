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
ms.openlocfilehash: 3a2fadd3d00bc23e689bbf22bb3b5db3efcd71f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788564"
---
# <a name="endtrigger-cell-glue-info-section"></a>EndTrigger, cellule (section Glue Info)

Contient une formule de déclenchement générée par l'application qui détermine si le point de fin d'une forme 1D doit être déplacé pour maintenir son lien à une autre forme.
  
## <a name="remarks"></a>Note

Lorsque vous collez une forme 1D à une autre de façon dynamique, Visio génère une formule qui fait référence à la cellule EventXFMod de l'autre forme. Lorsque cette forme est modifiée, Visio recalcule toutes les formules faisant référence à sa cellule EventXFMod, y compris la formule de la cellule EndTrigger. Les autres formules de la forme 1D font référence à la cellule EndTrigger et déplacent le point de fin de la forme 1D ou modifient la forme en conséquence.
  
Pour obtenir une référence à la cellule EndTrigger par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | EndTrigger  <br/> |
   
Pour obtenir une référence à la cellule EndTrigger par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visEndTrigger** <br/> |
   

