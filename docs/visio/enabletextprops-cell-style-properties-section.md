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
ms.openlocfilehash: ca1667e2f47a3c2fcab83890c55d111b658deb7b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774312"
---
# <a name="enabletextprops-cell-style-properties-section"></a>EnableTextProps, cellule (section Style Properties)

Détermine si un style inclut ou non des propriétés de texte.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Inclut les propriétés de texte. |
|FALSE  <br/> |Exclut les propriétés de texte. |
   
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
   

