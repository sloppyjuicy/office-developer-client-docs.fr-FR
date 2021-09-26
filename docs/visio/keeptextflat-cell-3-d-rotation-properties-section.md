---
title: KeepTextFlat Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indique si le texte d’une forme ignore la rotation de la forme en 3D. Ne s’applique pas à la rotation 2D.
ms.openlocfilehash: a37cfabe00742f7850fd1fa9a1faab7a6be8e5a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618741"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>KeepTextFlat Cell (3-D Rotation Properties Section)

Indique si le texte d’une forme ignore la rotation de la forme en 3D. Ne s’applique pas à la rotation 2D. 
  
****

|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte de la forme ne pivote pas avec la géométrie de la forme.  <br/> |
|FALSE  <br/> |Le texte de la forme est transformé pour pivoter avec la géométrie de la forme.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **KeepTextFlat** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |KeepTextFlat  <br/> |
   
Pour obtenir une référence à la **cellule KeepTextFlat** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRow3DRotationProperties** <br/> |
|Index de la cellule :  <br/> |**visKeepTextFlat** <br/> |
   

