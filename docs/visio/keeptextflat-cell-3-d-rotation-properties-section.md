---
title: KeepTextFlat Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indique si le texte d'une forme ignore la rotation de la forme en 3D. Ne s'applique pas à la rotation 2D.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422039"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>KeepTextFlat Cell (3-D Rotation Properties Section)

Indique si le texte d'une forme ignore la rotation de la forme en 3D. Ne s'applique pas à la rotation 2D. 
  
****

|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte de la forme ne pivote pas avec la géométrie de la forme.  <br/> |
|FALSE  <br/> |Le texte de la forme est transformé pour faire pivoter avec la géométrie de la forme.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **KeepTextFlat** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez: 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |KeepTextFlat  <br/> |
   
Pour obtenir une référence à la cellule **KeepTextFlat** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants: 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRow3DRotationProperties** <br/> |
|Index de la cellule :  <br/> |**visKeepTextFlat** <br/> |
   

