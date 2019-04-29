---
title: ShapeFixedCode, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Indique le comportement du positionnement d'une forme positionnable.
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431742"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a>ShapeFixedCode, cellule (section Shape Layout)

Indique le comportement du positionnement d'une forme positionnable.
  
|**Valeur**|**Mode de sélection**|**Constante d'automation**|
|:-----|:-----|:-----|
|&amp;H1  <br/> |Ne pas déplacer cette forme lorsque les formes sont disposées à l'aide de la boîte de dialogue **configurer la disposition** .  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |Ne pas déplacer cette forme et ne pas permettre aux formes qui tracent d'être positionnées sur cette forme.  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |Ne pas déplacer cette forme et permettre aux formes qui tracent d'être positionnées sur cette forme.  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |Ne pas tenir compte des emplacements des points de connexion en cas de positionnement.  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |Autoriser uniquement le positionnement sur les côtés ayant des points de connexion.  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |Ne pas coller au périmètre de cette forme. Coller plutôt au rectangle de sélection de la forme.  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule sous l'onglet **placement** de la boîte de dialogue **comportement** (sélectionnez une forme, sous l'onglet [développeur](run-in-developer-mode-display-the-developer-tab.md) , dans le groupe création de la **forme** , cliquez sur **comportement**, puis sur l'onglet **placement** . ). 
  
Vous pouvez définir n’importe quelle combinaison de ces valeurs pour cette cellule. Par exemple, vous pouvez entrer la valeur 3 (&amp;H3), ce qui élimine le mouvement lorsque vous disposez des formes à l'aide de la boîte de dialogue **configurer la disposition** (sous l'onglet **création** , dans le groupe **disposition** , cliquez sur **nouvelle disposition de page**, puis cliquez sur ** Autres options de disposition** ) et lorsque d'autres formes positionnables sont placées sur la forme ou près de celle-ci. 
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous. 
  
Pour obtenir une référence à la cellule ShapeFixedCode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ShapeFixedCode  <br/> |
   
Pour obtenir une référence à la cellule ShapeFixedCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOFixedCode** <br/> |
   

