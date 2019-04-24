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
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326676"
---
# <a name="thetext-cell-events-section"></a>TheText, cellule (section Events)

Cellule d'événement qui est calculée lorsque la composition du texte ou le texte d'une forme change.
  
## <a name="remarks"></a>Remarques

Les cellules d'événement sont évaluées lorsque l'événement se produit et non lors de la saisie de la formule. La cellule TheText permet de déclencher des recalculs, pour recalculer par exemple la largeur et la hauteur du texte avec les fonctions TEXTWIDTH( ) et TEXTHEIGHT( ).
  
Pour obtenir une référence à la cellule TheText par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | TheText  <br/> |
   
Pour obtenir une référence à la cellule TheText par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowEvent** <br/> |
| Index de la cellule :  <br/> |**visEvtCellTheText** <br/> |
   

