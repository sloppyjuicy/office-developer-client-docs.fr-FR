---
title: TheText, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Cellule d'événement qui est calculée lorsque la composition du texte ou le texte d'une forme change.
ms.openlocfilehash: 942ccee4478c87243207d8d65785857758d2a068
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789894"
---
# <a name="thetext-cell-events-section"></a>TheText, cellule (section Events)

Cellule d'événement qui est calculée lorsque la composition du texte ou le texte d'une forme change.
  
## <a name="remarks"></a>Note

Les cellules d'événement sont évaluées lorsque l'événement se produit et non lors de la saisie de la formule. La cellule TheText permet de déclencher des recalculs, pour recalculer par exemple la largeur et la hauteur du texte avec les fonctions TEXTWIDTH( ) et TEXTHEIGHT( ).
  
Pour obtenir une référence à la cellule TheText par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TheText  <br/> |
   
Pour obtenir une référence à la cellule TheText par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowEvent** <br/> |
| Index de la cellule :  <br/> |**visEvtCellTheText** <br/> |
   

