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
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789175"
---
# <a name="objectkind-cell-text-fields-section"></a>ObjectKind, cellule (section Text Fields)

Indique le type de champ de texte.
  
|**Valeur**|**Description**|**Constante d’Automation**|
|:-----|:-----|:-----|
| 0  <br/> | Standard  <br/> |**visTFOKStandard** <br/> |
| 1  <br/> |Horizontal en vertical  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>Note

Les champs de texte peuvent présenter l'un des types suivants :
  
- standard, indiquant que le champ a été inséré par catégorie de champ ;
    
- horizontal en vertical, indiquant que le champ est du texte horizontal défini dans du texte vertical.
    
Pour obtenir une référence à la cellule ObjectKind par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Fields.ObjectKind [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule ObjectKind par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTextField** <br/> |
| Index de la ligne :  <br/> |**visRowField** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visFieldObjectKind** <br/> |
   

