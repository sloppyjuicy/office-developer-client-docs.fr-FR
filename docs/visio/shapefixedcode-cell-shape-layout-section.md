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
|&amp;H1  <br/> |Ne déplacez pas cette forme lorsque les formes sont disposés à l’aide de la **boîte** de dialogue Configurer la disposition.  <br/> |**visSLOFixedPlacement** <br/> |
|&amp;H2  <br/> |Ne pas déplacer cette forme et ne pas permettre aux formes qui tracent d'être positionnées sur cette forme.  <br/> |**visSLOFixedPlow** <br/> |
|&amp;H4  <br/> |Ne pas déplacer cette forme et permettre aux formes qui tracent d'être positionnées sur cette forme.  <br/> |**visSLOFixedPermeablePlow** <br/> |
|&amp;H20 (32)  <br/> |Ne pas tenir compte des emplacements des points de connexion en cas de positionnement.  <br/> |**visSLOFixedConnPtsIgnore** <br/> |
|&amp;H40 (64)  <br/> |Autoriser uniquement le positionnement sur les côtés ayant des points de connexion.  <br/> |**visSLOFixedConnPtsOnly** <br/> |
|&amp;H80 (128)  <br/> |Ne pas coller au périmètre de cette forme. Coller plutôt au rectangle de sélection de la forme.  <br/> |**visSLOFixedNoFoldToShape** <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette  cellule sous l’onglet **Placement** dans la boîte  de dialogue Comportement (avec une forme sélectionnée, sous l’onglet Développeur, dans le groupe Création de formes, cliquez sur **Comportement,** puis cliquez sur l’onglet **Placement).** [](run-in-developer-mode-display-the-developer-tab.md) 
  
Vous pouvez définir n’importe quelle combinaison de ces valeurs pour cette cellule. Par exemple, vous pouvez entrer la valeur 3 ( H3), ce qui élimine le mouvement lorsque vous placez des formes à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition page, puis cliquez sur Autres options de disposition) et lorsque d’autres formes &amp; positionnables     sont placées sur ou près de la forme.  
  
Dans les versions antérieures à Visio 2000, vous pouviez définir ce comportement en faisant appel à la cellule ObjInteract de la section Miscellaneous. 
  
Pour obtenir une référence à la cellule ShapeFixedCode par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |ShapeFixedCode  <br/> |
   
Pour obtenir une référence à la cellule ShapeFixedCode à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowShapeLayout** <br/> |
|Index de la cellule :  <br/> |**visSLOFixedCode** <br/> |
   

