---
title: Initials, cellule (section Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Contient les initiales du réviseur d’un document.
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788842"
---
# <a name="initials-cell-reviewer-section"></a>Initials, cellule (section Reviewer)

Contient les initiales du réviseur d’un document.
  
## <a name="remarks"></a>Remarques

La valeur par défaut aux initiales qui apparaissent dans la zone **initiales** sous l’onglet **Général** dans la boîte de dialogue **Options Visio** (cliquez sur l’onglet **fichier** , cliquez sur **Options**, puis cliquez sur **Général** ). 
  
Pour obtenir une référence à la cellule Initials par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Reviewer.Initials [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Initials par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionReviewer** <br/> |
| Index de la ligne :  <br/> |**visRowReviewer** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visReviewerInitials** <br/> |
   

