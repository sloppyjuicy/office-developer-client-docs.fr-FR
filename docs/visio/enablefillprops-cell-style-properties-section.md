---
title: EnableFillProps, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm300
localization_priority: Normal
ms.assetid: 2b3334de-588c-6cf3-bc88-be03ae71b1a6
description: Détermine si un style comporte des propriétés de remplissage.
ms.openlocfilehash: 399af4b9d1a2245ea7a9b91ebbf036eb122f15bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788558"
---
# <a name="enablefillprops-cell-style-properties-section"></a>EnableFillProps, cellule (section Style Properties)

Détermine si un style comporte des propriétés de remplissage.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Comprend des propriétés de remplissage.  <br/> |
|FALSE  <br/> |Exclut les propriétés de remplissage.  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule EnableFillProps par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EnableFillProps  <br/> |
   
Pour obtenir une référence à la cellule EnableFillProps par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowStyle** <br/> |
|Index de la cellule :  <br/> |**visStyleIncludesFill** <br/> |
   

