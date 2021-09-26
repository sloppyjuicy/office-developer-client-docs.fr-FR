---
title: EventDblClick, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
ms.localizationpriority: medium
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: Cellule Event qui est évaluée lors d'un double-clic sur une forme.
ms.openlocfilehash: 7e3fc2568d4afbeb041057aa78790953a2357acc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619075"
---
# <a name="eventdblclick-cell-events-section"></a>EventDblClick, cellule (section Events)

Cellule Event qui est évaluée lors d'un double-clic sur une forme.
  
## <a name="remarks"></a>Remarques

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule EventDblClick par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | EventDblClick  <br/> |
   
Pour obtenir une référence à la cellule EventDblClick à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowEvent** <br/> |
| Index de la cellule :  <br/> |**visEvtCellDblClick** <br/> |
   

