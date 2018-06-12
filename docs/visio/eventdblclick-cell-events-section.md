---
title: EventDblClick, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Cellule Event qui est évaluée lors d'un double-clic sur une forme.
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788569"
---
# <a name="eventdblclick-cell-events-section"></a>EventDblClick, cellule (section Events)

Cellule Event qui est évaluée lors d'un double-clic sur une forme.
  
## <a name="remarks"></a>Note

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule EventDblClick par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | EventDblClick  <br/> |
   
Pour obtenir une référence à la cellule EventDblClick par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowEvent** <br/> |
| Index de la cellule :  <br/> |**visEvtCellDblClick** <br/> |
   

