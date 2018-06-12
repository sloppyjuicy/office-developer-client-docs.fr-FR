---
title: EventDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Cellule Event qui est évaluée lorsqu'une forme est insérée sur la page de dessin, soit comme instance, soit lorsqu'elle est dupliquée ou collée.
ms.openlocfilehash: e2624c50896de061727003a48f7dc1559c6a72c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788567"
---
# <a name="eventdrop-cell-events-section"></a>EventDrop, cellule (section Events)

Cellule Event qui est évaluée lorsqu'une forme est insérée sur la page de dessin, soit comme instance, soit lorsqu'elle est dupliquée ou collée.
  
## <a name="remarks"></a>Note

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule EventDrop par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | EventDrop  <br/> |
   
Pour obtenir une référence à la cellule EventDrop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowEvent** <br/> |
| Index de la cellule :  <br/> |**visEvtCellDrop** <br/> |
   

