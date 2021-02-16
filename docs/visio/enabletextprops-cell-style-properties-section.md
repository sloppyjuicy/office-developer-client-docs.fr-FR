---
title: EnableTextProps, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
localization_priority: Normal
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: Détermine si un style inclut ou non des propriétés de texte.
ms.openlocfilehash: 3f1d87316955b4e6e40cea16634cff7645a720fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419260"
---
# <a name="enabletextprops-cell-style-properties-section"></a>EnableTextProps, cellule (section Style Properties)

Détermine si un style inclut ou non des propriétés de texte.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Inclut les propriétés de texte.  <br/> |
|FALSE  <br/> |Exclut les propriétés de texte.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule EnableTextProps par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EnableTextProps  <br/> |
   
Pour obtenir une référence à la cellule EnableTextProps à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowStyle** <br/> |
|Index de la cellule :  <br/> |**visStyleIncludesText** <br/> |
   

