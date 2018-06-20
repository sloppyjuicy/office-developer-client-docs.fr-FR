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
ms.openlocfilehash: 6bc1629c51fc4dcb3fe7e2d6576e8f1f096144ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789163"
---
# <a name="name-cell-reviewer-section"></a>Name, cellule (section Reviewer)

Contient le nom du réviseur d’un document.
  
## <a name="remarks"></a>Remarques

 La valeur par défaut au nom trouvé dans la zone **nom d’utilisateur** sous l’onglet **Général** de la boîte de dialogue **Options Visio** (cliquez sur l’onglet **fichier** , cliquez sur **Options**, puis cliquez sur **Général**). 
  
Pour obtenir une référence à la cellule Name par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Reviewer.Name [ *i* ] où *i* = < 1 >, 2, 3...  <br/> |
   
Pour obtenir une référence à la cellule Name par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionReviewer** <br/> |
| Index de la ligne :  <br/> |**visRowReviewer** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visReviewerName** <br/> |
   

