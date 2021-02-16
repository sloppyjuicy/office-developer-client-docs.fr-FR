---
title: EnableLineProps, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
localization_priority: Normal
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: Détermine si un style inclut ou non des propriétés de trait.
ms.openlocfilehash: 38964194626be052b2a168fa929b69ebe4b28e01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409999"
---
# <a name="enablelineprops-cell-style-properties-section"></a>EnableLineProps, cellule (section Style Properties)

Détermine si un style inclut ou non des propriétés de trait.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Inclut des propriétés de trait.  <br/> |
|FALSE  <br/> |Exclut les propriétés de trait.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule EnableLineProps par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EnableLineProps  <br/> |
   
Pour obtenir une référence à la cellule EnableLineProps à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowStyle** <br/> |
|Index de la cellule :  <br/> |**visStyleIncludesLine** <br/> |
   

