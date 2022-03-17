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
ms.openlocfilehash: 3e7e0d7b240464db0611f242de4609d1024bd8b3
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522708"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>LocalizeMerge, cellule (section Miscellaneous)

Détermine si les formes sont localisées lors de leur copie d'un document à l'autre.
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | Localise une forme dans la langue du document de destination. |
| FALSE  <br/> | Ne localisez pas une forme en fonction de la langue du document de destination (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LocalizeMerge par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | LocalizeMerge  <br/> |
   
Pour obtenir une référence à la cellule LocalizeMerge à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowMisc** <br/> |
| **Index de la cellule :**  <br/> |**visObjLocalizeMerge** <br/> |
   

