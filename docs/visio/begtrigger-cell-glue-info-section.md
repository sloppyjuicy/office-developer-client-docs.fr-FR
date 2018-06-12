---
title: BegTrigger, cellule (section Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
localization_priority: Normal
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: Contient une formule de déclenchement générée par l'application, qui détermine si le point de début d'une forme 1D doit être déplacé pour maintenir son lien à une autre forme.
ms.openlocfilehash: 5dec179f1847c30c6ef563d866360b6dd31a1d88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788040"
---
# <a name="begtrigger-cell-glue-info-section"></a>BegTrigger, cellule (section Glue Info)

Contient une formule de déclenchement générée par l'application, qui détermine si le point de début d'une forme 1D doit être déplacé pour maintenir son lien à une autre forme.
  
## <a name="remarks"></a>Note

Lorsque vous collez une forme 1D à une autre forme au moyen de la colle dynamique, l'application génère une formule qui fait référence à la cellule EventXFMod de l'autre forme. Lorsque cette forme est modifiée, Visio recalcule toutes les formules faisant référence à sa cellule EventXFMod, y compris la formule de la cellule BegTrigger. Les autres formules de la forme 1D font référence à la cellule BegTrigger et déplacent le point de début de la forme 1D ou modifient la forme en conséquence.
  
Pour obtenir une référence à la cellule BegTrigger par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | BegTrigger  <br/> |
   
Pour obtenir une référence à la cellule BegTrigger par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowGroup** <br/> |
| Index de la cellule :  <br/> |**visBegTrigger** <br/> |
   

