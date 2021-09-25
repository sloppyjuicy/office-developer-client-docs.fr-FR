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
ms.openlocfilehash: f2e6c3c74329c196e2e527a2879c0604ef5c5c61
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559905"
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
   

