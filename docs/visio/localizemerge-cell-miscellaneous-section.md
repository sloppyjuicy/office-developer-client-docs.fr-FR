---
title: LocalizeMerge, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Détermine si les formes sont localisées lors de leur copie d'un document à l'autre.
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788976"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>LocalizeMerge, cellule (section Miscellaneous)

Détermine si les formes sont localisées lors de leur copie d'un document à l'autre.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Localise une forme dans la langue du document de destination.  <br/> |
| FALSE  <br/> | Ne localise pas une forme en fonction de la langue du document de destination (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule LocalizeMerge par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LocalizeMerge  <br/> |
   
Pour obtenir une référence à la cellule LocalizeMerge par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visObjLocalizeMerge** <br/> |
   

