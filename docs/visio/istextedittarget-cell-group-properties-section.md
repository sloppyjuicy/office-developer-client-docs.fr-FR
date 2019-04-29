---
title: IsTextEditTarget, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Détermine l'attribution de texte à un groupe.
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432645"
---
# <a name="istextedittarget-cell-group-properties-section"></a>IsTextEditTarget, cellule (section Group Properties)

Détermine l'attribution de texte à un groupe.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte est ajouté à la forme de groupe.  <br/> |
|FALSE  <br/> |Le texte est ajouté dans le groupe à la forme qui se trouve au premier rang de la pile.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis activant la case à cocher **Modifier le texte du groupe**. 
  
Les groupes créés dans les versions antérieures à Visio 2000 ont une valeur par défaut de FALSE. À partir de Visio 2000, la valeur par défaut est TRUE. 
  
Pour obtenir une référence à la cellule IsTextEditTarget par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |IsTextEditTarget  <br/> |
   
Pour obtenir une référence à la cellule IsTextEditTarget à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowGroup** <br/> |
|Index de la cellule :  <br/> |**visGroupIsTextEditTarget** <br/> |
   

