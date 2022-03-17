---
title: EnableLineProps, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
ms.localizationpriority: medium
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: Détermine si un style inclut ou non des propriétés de trait.
ms.openlocfilehash: a8883c492ea6e7553fa53666279e5b92164263dd
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63519712"
---
# <a name="enablelineprops-cell-style-properties-section"></a>EnableLineProps, cellule (section Style Properties)

Détermine si un style inclut ou non des propriétés de trait.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Inclut des propriétés de trait. |
|FALSE  <br/> |Exclut les propriétés de trait. |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule EnableLineProps par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |EnableLineProps  <br/> |
   
Pour obtenir une référence à la cellule EnableLineProps à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowStyle** <br/> |
|**Index de la cellule :**  <br/> |**visStyleIncludesLine** <br/> |
   

