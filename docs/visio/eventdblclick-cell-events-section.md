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
ms.openlocfilehash: b3db37ac8a843eff18628dd65df9f26d0ce4c4e5
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63523226"
---
# <a name="eventdblclick-cell-events-section"></a>EventDblClick, cellule (section Events)

Cellule Event qui est évaluée lors d'un double-clic sur une forme.
  
## <a name="remarks"></a>Remarques

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule EventDblClick par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | EventDblClick  <br/> |
   
Pour obtenir une référence à la cellule EventDblClick à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowEvent** <br/> |
| **Index de la cellule :**  <br/> |**visEvtCellDblClick** <br/> |
   

