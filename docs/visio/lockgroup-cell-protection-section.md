---
title: LockGroup, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
ms.localizationpriority: medium
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Verrouille un groupe afin d'empêcher sa dissociation.
ms.openlocfilehash: 31472fe76a879188d6f90a4ea954ad11d5ac27c1
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521175"
---
# <a name="lockgroup-cell-protection-section"></a>LockGroup, cellule (section Protection)

Verrouille un groupe afin d'empêcher sa dissociation.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le groupe ne peut pas être dissocié. |
|FALSE  <br/> |Le groupe peut être dissocié. |
   
## <a name="remarks"></a>Remarques

La définition de la valeur LockGroupCell sur TRUE empêche également la suppression de toutes les formes qui sont membres du groupe.
  
Pour obtenir une référence à la cellule LockGroup par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |LockGroup  <br/> |
   
Pour obtenir une référence à la cellule LockGroup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLock** <br/> |
|**Index de la cellule :**  <br/> |**visLockGroup** <br/> |
   

