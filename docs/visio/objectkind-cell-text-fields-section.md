---
title: ObjectKind, cellule (section Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
ms.localizationpriority: medium
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Indique le type de champ de texte.
ms.openlocfilehash: 978963cabb19d0b4321c530070d2fe1799ce6a11
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775398"
---
# <a name="objectkind-cell-text-fields-section"></a>ObjectKind, cellule (section Text Fields)

Indique le type de champ de texte.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Standard  <br/> |**visTFOKStandard** <br/> |
| 1  <br/> |Horizontal en vertical  <br/> |**visTFOKHorizontaInVertical** <br/> |
   
## <a name="remarks"></a>Remarques

Les champs de texte peuvent présenter l'un des types suivants :
  
- standard, indiquant que le champ a été inséré par catégorie de champ ;
    
- horizontal en vertical, indiquant que le champ est du texte horizontal défini dans du texte vertical.
    
Pour obtenir une référence à la cellule ObjectKind par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Fields.ObjectKind[  *i*  ] où  *i*  = <1>, 2, 3... |
   
Pour obtenir une référence à la cellule ObjectKind à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionTextField** <br/> |
| Index de la ligne :  <br/> |**visRowField** +   *i* où *i* = 0, 1, 2... |
| Index de la cellule :  <br/> |**visFieldObjectKind** <br/> |
   

