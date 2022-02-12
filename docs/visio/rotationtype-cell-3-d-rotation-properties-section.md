---
title: RotationType Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Détermine si la forme suit une rotation parallèle, une rotation de perspective ou une rotation oblique, sous la forme d’un nombre integer de 0 à 6.
ms.openlocfilehash: afbb587f6f52eb2b9ecfc062838df65cc3453a0b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770001"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>RotationType Cell (3-D Rotation Properties Section)

Détermine si la forme suit une rotation parallèle, une rotation de perspective ou une rotation oblique, sous la forme d’un nombre integer de 0 à 6. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |La forme n’a aucune rotation. |
|1  <br/> |La forme a une rotation parallèle. |
|2  <br/> |La forme a une rotation de perspective. |
|3  <br/> |La forme possède une rotation oblique supérieure gauche. |
|4  <br/> |La forme possède une rotation oblique supérieure droite. |
|5  <br/> |La forme a une rotation oblique vers le bas à gauche. |
|6   <br/> |La forme a une rotation oblique vers le bas à droite. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **RotationType** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |RotationType  <br/> |
   
Pour obtenir une référence à la cellule **RotationType** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRow3DRotationProperties** <br/> |
|Index de la cellule :  <br/> |**visRotationType** <br/> |
   

