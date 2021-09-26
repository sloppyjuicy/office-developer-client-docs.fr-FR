---
title: Initials, cellule (section Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
ms.localizationpriority: medium
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Contient les initiales du réviseur d’un document.
ms.openlocfilehash: e3f76685631ca6ddba1848d8ecd57533755ecf84
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618804"
---
# <a name="initials-cell-reviewer-section"></a>Initials, cellule (section Reviewer)

Contient les initiales du réviseur d’un document.
  
## <a name="remarks"></a>Remarques

Cette valeur est par défaut les initiales  de la zone **Initiales** de l’onglet  Général de la boîte de dialogue **Options Visio** (cliquez sur l’onglet Fichier, cliquez sur **Options,** puis sur **Général).** 
  
Pour obtenir une référence à la cellule Initials par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Reviewer.Initials [  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Initials à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionReviewer** <br/> |
| Index de la ligne :  <br/> |**visRowReviewer**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visReviewerInitials** <br/> |
   

