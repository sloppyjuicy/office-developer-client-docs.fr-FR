---
title: KeepTextFlat Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Indique si le texte d’une forme ignore la rotation de la forme en 3D. Ne s’applique pas à la rotation 2D.
ms.openlocfilehash: a25a5eb646b883c4216933d072b9f454d551e25b
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448740"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>KeepTextFlat Cell (3-D Rotation Properties Section)

Indique si le texte d’une forme ignore la rotation de la forme en 3D. Ne s’applique pas à la rotation 2D. 
  
****

|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte de la forme ne pivote pas avec la géométrie de la forme. |
|FALSE  <br/> |Le texte de la forme est transformé pour pivoter avec la géométrie de la forme. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **KeepTextFlat** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |KeepTextFlat  <br/> |
   
Pour obtenir une référence à la **cellule KeepTextFlat** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRow3DRotationProperties** <br/> |
|**Index de la cellule :**  <br/> |**visKeepTextFlat** <br/> |
   

