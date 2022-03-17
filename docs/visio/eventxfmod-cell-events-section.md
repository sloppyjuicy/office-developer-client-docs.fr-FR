---
title: EventXFMod, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
ms.localizationpriority: medium
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: Cellule d’événement évaluée lors de la transformation de la position ou de l’orientation d’une forme sur la page (XF).
ms.openlocfilehash: 536db8b11e95fe85d31bf2bf97e79560668134d6
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63520132"
---
# <a name="eventxfmod-cell-events-section"></a>EventXFMod, cellule (section Events)

Cellule Event qui est évaluée lorsque la position ou l'orientation d'une forme sur la page est modifiée (« XF »).
  
## <a name="remarks"></a>Remarques

Les cellules Event ne sont évaluées que lorsque l'événement se produit, et non lors de l'entrée de la formule.
  
Pour obtenir une référence à la cellule EventXFMod par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | EventXFMod  <br/> |
   
Pour obtenir une référence à la cellule Event XFMod à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowEvent** <br/> |
| **Index de la cellule :**  <br/> |**visEvtCellXFMod** <br/> |
   

