---
title: LockGroup, cellule (section Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Verrouille un groupe afin d'empêcher sa dissociation.
ms.openlocfilehash: 4d09d514a3fff8ada40c67eb9cd9537539a1039a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789019"
---
# <a name="lockgroup-cell-protection-section"></a>LockGroup, cellule (section Protection)

Verrouille un groupe afin d'empêcher sa dissociation.
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le groupe ne peut pas être dissocié.  <br/> |
|FALSE  <br/> |Le groupe peut être dissocié.  <br/> |
   
## <a name="remarks"></a>Note

La définition de la valeur LockGroupCell sur TRUE empêche également la suppression de toutes les formes qui sont membres du groupe.
  
Pour obtenir une référence à la cellule LockGroup par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |LockGroup  <br/> |
   
Pour obtenir une référence à la cellule LockGroup par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLock** <br/> |
|Index de la cellule :  <br/> |**visLockGroup** <br/> |
   

