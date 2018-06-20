---
title: TypeRotation, cellule (Section Propriétés de Rotation 3D)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Détermine si la forme suit une rotation en parallèle, une rotation du point de vue ou une rotation de l’effet oblique, comme un entier compris entre 0 et 6.
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789532"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>TypeRotation, cellule (Section Propriétés de Rotation 3D)

Détermine si la forme suit une rotation en parallèle, une rotation du point de vue ou une rotation de l’effet oblique, comme un entier compris entre 0 et 6. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |La forme n’a pas de rotation.  <br/> |
|1  <br/> |La forme est une rotation en parallèle.  <br/> |
|2  <br/> |La forme est une rotation en perspective.  <br/> |
|3  <br/> |La forme est une rotation de l’effet oblique supérieure gauche.  <br/> |
|4  <br/> |La forme est une rotation de l’effet oblique droite supérieure.  <br/> |
|5  <br/> |La forme est une rotation de l’effet oblique gauche en bas.  <br/> |
|6  <br/> |La forme possède un bas à droite de rotation de l’effet oblique.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule **TypeRotation** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |TypeRotation  <br/> |
   
Pour obtenir une référence à la cellule **TypeRotation** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRow3DRotationProperties** <br/> |
|Index de la cellule :  <br/> |**visRotationType** <br/> |
   

