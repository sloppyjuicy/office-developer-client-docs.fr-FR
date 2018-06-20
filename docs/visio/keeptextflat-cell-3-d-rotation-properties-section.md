---
title: KeepTextFlat, cellule (Section Propriétés de Rotation 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indique si le texte d’une forme ignorera rotation d’une forme en 3D. Ne s’applique pas à la rotation 2D.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788890"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>KeepTextFlat, cellule (Section Propriétés de Rotation 3D)

Indique si le texte d’une forme ignorera rotation d’une forme en 3D. Ne s’applique pas à la rotation 2D. 
  
****

|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Texte de la forme ne pivote pas avec la géométrie d’une forme.  <br/> |
|FALSE  <br/> |Texte de la forme est transformé pivote avec la géométrie d’une forme.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **KeepTextFlat** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |KeepTextFlat  <br/> |
   
Pour obtenir une référence à la cellule **KeepTextFlat** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRow3DRotationProperties** <br/> |
|Index de la cellule :  <br/> |**visKeepTextFlat** <br/> |
   

