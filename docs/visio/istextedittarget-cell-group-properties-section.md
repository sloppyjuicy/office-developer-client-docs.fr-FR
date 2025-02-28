---
title: IsTextEditTarget, cellule (section Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
ms.localizationpriority: medium
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Détermine l'attribution de texte à un groupe.
ms.openlocfilehash: f7e417b3a94d0771b437b7556573834bbcad873a
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426789"
---
# <a name="istextedittarget-cell-group-properties-section"></a>IsTextEditTarget, cellule (section Group Properties)

Détermine l'attribution de texte à un groupe.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le texte est ajouté à la forme de groupe. |
|FALSE  <br/> |Le texte est ajouté dans le groupe à la forme qui se trouve au premier rang de la pile. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur en sélectionnant le groupe, en cliquant sur **Comportement** sous l’onglet [Développeur](run-in-developer-mode-display-the-developer-tab.md), puis activant la case à cocher **Modifier le texte du groupe**. 
  
Les groupes créés dans les versions antérieures à Visio 2000 ont une valeur par défaut de FALSE. À partir de Visio 2000, la valeur par défaut est TRUE. 
  
Pour obtenir une référence à la cellule IsTextEditTarget par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |IsTextEditTarget  <br/> |
   
Pour obtenir une référence à la cellule IsTextEditTarget à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowGroup** <br/> |
|**Index de la cellule :**  <br/> |**visGroupIsTextEditTarget** <br/> |
   

