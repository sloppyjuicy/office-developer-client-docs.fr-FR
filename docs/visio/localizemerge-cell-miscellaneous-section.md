---
title: LocalizeMerge, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
ms.localizationpriority: medium
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Détermine si les formes sont localisées lors de leur copie d'un document à l'autre.
ms.openlocfilehash: 9f2e3e689814891f1a8cd4c69d7656fe6d1b22c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615878"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>LocalizeMerge, cellule (section Miscellaneous)

Détermine si les formes sont localisées lors de leur copie d'un document à l'autre.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Localise une forme dans la langue du document de destination.  <br/> |
| FALSE  <br/> | Ne localisez pas une forme en fonction de la langue du document de destination (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LocalizeMerge par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LocalizeMerge  <br/> |
   
Pour obtenir une référence à la cellule LocalizeMerge à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowMisc** <br/> |
| Index de la cellule :  <br/> |**visObjLocalizeMerge** <br/> |
   

