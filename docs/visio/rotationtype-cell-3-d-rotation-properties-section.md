---
title: RotationType Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Détermine si la forme suit une rotation parallèle, une rotation de perspective ou une rotation oblique, sous la forme d’un nombre integer de 0 à 6.
ms.openlocfilehash: 7e5929b4bc80ae499174c3f7c290de4d6e5666ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573501"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>RotationType Cell (3-D Rotation Properties Section)

Détermine si la forme suit une rotation parallèle, une rotation de perspective ou une rotation oblique, sous la forme d’un nombre integer de 0 à 6. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |La forme n’a aucune rotation.  <br/> |
|1  <br/> |La forme a une rotation parallèle.  <br/> |
|2  <br/> |La forme a une rotation de perspective.  <br/> |
|3  <br/> |La forme possède une rotation oblique supérieure gauche.  <br/> |
|4   <br/> |La forme possède une rotation oblique supérieure droite.  <br/> |
|5  <br/> |La forme a une rotation oblique vers le bas à gauche.  <br/> |
|6   <br/> |La forme a une rotation oblique vers le bas à droite.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **RotationType** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |RotationType  <br/> |
   
Pour obtenir une référence à la cellule **RotationType** à l’aide d’un index à partir d’un programme, utilisez la **propriété CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRow3DRotationProperties** <br/> |
|Index de la cellule :  <br/> |**visRotationType** <br/> |
   

