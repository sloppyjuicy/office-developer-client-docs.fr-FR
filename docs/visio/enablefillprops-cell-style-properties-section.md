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
ms.openlocfilehash: 85dba6ee92b66283946908a7f06777a7fbb6cbc1
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506034"
---
# <a name="enablefillprops-cell-style-properties-section"></a>EnableFillProps, cellule (section Style Properties)

Détermine si un style comporte des propriétés de remplissage.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Comprend des propriétés de remplissage. |
|FALSE  <br/> |Exclut les propriétés de remplissage. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule EnableFillProps par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |EnableFillProps  <br/> |
   
Pour obtenir une référence à la cellule EnableFillProps à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowStyle** <br/> |
|**Index de la cellule :**  <br/> |**visStyleIncludesFill** <br/> |
   

