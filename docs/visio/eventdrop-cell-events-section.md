---
title: EventDrop, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
ms.localizationpriority: medium
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: Cellule Event qui est évaluée lorsqu'une forme est insérée sur la page de dessin, soit comme instance, soit lorsqu'elle est dupliquée ou collée.
ms.openlocfilehash: e89ec57231f205f1eead224370afcfc9b4469059
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631112"
---
# <a name="eventdrop-cell-events-section"></a>EventDrop, cellule (section Events)

Cellule Event qui est évaluée lorsqu'une forme est insérée sur la page de dessin, soit comme instance, soit lorsqu'elle est dupliquée ou collée.
  
## <a name="remarks"></a>Remarques

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule EventDrop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | EventDrop  <br/> |
   
Pour obtenir une référence à la cellule EventDrop à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowEvent** <br/> |
| **Index de la cellule :**  <br/> |**visEvtCellDrop** <br/> |
   

