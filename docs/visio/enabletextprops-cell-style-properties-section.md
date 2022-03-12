---
title: EnableTextProps, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
ms.localizationpriority: medium
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: Détermine si un style inclut ou non des propriétés de texte.
ms.openlocfilehash: dd9c170a09d726029a06aa956f0381ecb8b1f6dc
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448565"
---
# <a name="enabletextprops-cell-style-properties-section"></a>EnableTextProps, cellule (section Style Properties)

Détermine si un style inclut ou non des propriétés de texte.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Inclut les propriétés de texte. |
|FALSE  <br/> |Exclut les propriétés de texte. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule EnableTextProps par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |EnableTextProps  <br/> |
   
Pour obtenir une référence à la cellule EnableTextProps à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowStyle** <br/> |
|**Index de la cellule :**  <br/> |**visStyleIncludesText** <br/> |
   

