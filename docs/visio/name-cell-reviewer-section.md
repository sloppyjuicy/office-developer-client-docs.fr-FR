---
title: Name, cellule (section Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Contient le nom du réviseur d’un document.
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417685"
---
# <a name="name-cell-reviewer-section"></a>Name, cellule (section Reviewer)

Contient le nom du réviseur d’un document.
  
## <a name="remarks"></a>Remarques

 Cette valeur est par défaut  le nom trouvé  dans la zone Nom d’utilisateur  sous l’onglet Général de la boîte de dialogue **Options Visio** (cliquez sur l’onglet Fichier, cliquez sur **Options,** puis sur **Général).** 
  
Pour obtenir une référence à la cellule Name par un nom à partir d’une autre formule ou d’un programme en faisant appel à la **propriété CellsU,** utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Reviewer.Name [  *i*  ] où  *i*  = <1>, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Name à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionReviewer** <br/> |
| Index de la ligne :  <br/> |**visRowReviewer**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visReviewerName** <br/> |
   

