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
ms.openlocfilehash: 34b1cf25667ba6fd4354ec2bc6ca3afd5b49bf91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570644"
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
   

