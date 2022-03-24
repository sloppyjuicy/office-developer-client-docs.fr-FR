---
title: TheText, cellule (section Events)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
ms.localizationpriority: medium
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Cellule d'événement qui est calculée lorsque la composition du texte ou le texte d'une forme change.
ms.openlocfilehash: 19b25a71e3a00499d90584c5989be24e48e4e1d5
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63724950"
---
# <a name="thetext-cell-events-section"></a>TheText, cellule (section Events)

Cellule d'événement qui est calculée lorsque la composition du texte ou le texte d'une forme change.
  
## <a name="remarks"></a>Remarques

Les cellules d'événement sont évaluées lorsque l'événement se produit et non lors de la saisie de la formule. La cellule TheText permet de déclencher des recalculs, pour recalculer par exemple la largeur et la hauteur du texte avec les fonctions TEXTWIDTH( ) et TEXTHEIGHT( ).
  
Pour obtenir une référence à la cellule TheText par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | TheText  <br/> |
   
Pour obtenir une référence à la cellule TheText par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowEvent** <br/> |
| **Index de la cellule :**  <br/> |**visEvtCellTheText** <br/> |
   

