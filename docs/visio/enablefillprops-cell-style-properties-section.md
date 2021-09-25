---
title: EnableFillProps, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm300
ms.localizationpriority: medium
ms.assetid: 2b3334de-588c-6cf3-bc88-be03ae71b1a6
description: Détermine si un style comporte des propriétés de remplissage.
ms.openlocfilehash: 4621b40287b8e03464e2f27db3a5639ac7eb6d6f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570742"
---
# <a name="enablefillprops-cell-style-properties-section"></a>EnableFillProps, cellule (section Style Properties)

Détermine si un style comporte des propriétés de remplissage.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Comprend des propriétés de remplissage.  <br/> |
|FALSE  <br/> |Exclut les propriétés de remplissage.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule EnableFillProps par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EnableFillProps  <br/> |
   
Pour obtenir une référence à la cellule EnableFillProps à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowStyle** <br/> |
|Index de la cellule :  <br/> |**visStyleIncludesFill** <br/> |
   

