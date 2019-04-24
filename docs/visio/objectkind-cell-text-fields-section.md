---
title: ObjectKind, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Indique le type de champ de texte.
ms.openlocfilehash: c2f891620f704a3c48861124b886e49d356960ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360990"
---
# <a name="objectkind-cell-text-fields-section"></a>ObjectKind, cellule (section Text Fields)

Indique le type de champ de texte.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Standard  <br/> |**visTFOKStandard** <br/> |
| 0,1  <br/> |Horizontal en vertical  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>Remarques

Les champs de texte peuvent présenter l'un des types suivants :
  
- standard, indiquant que le champ a été inséré par catégorie de champ ;
    
- horizontal en vertical, indiquant que le champ est du texte horizontal défini dans du texte vertical.
    
Pour obtenir une référence à la cellule ObjectKind par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Fields. ObjectKind [ *i* ] où *i* = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule ObjectKind à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTextField** <br/> |
| Index de la ligne :  <br/> |**visRowField** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visFieldObjectKind** <br/> |
   

