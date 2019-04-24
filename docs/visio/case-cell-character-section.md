---
title: Case, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Détermine la casse du texte de la forme. Toutes les lettres capitales (majuscules) (1) et Capitales initiales uniquement (2) ne modifient pas l'apparence d'un texte qui a été entré tout en lettres capitales. Le texte doit avoir été entré en lettres minuscules pour que les effets de cette option soient visibles.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337232"
---
# <a name="case-cell-character-section"></a>Case, cellule (section Character)

Détermine la casse du texte de la forme. Toutes les lettres capitales (majuscules) (1) et Capitales initiales uniquement (2) ne modifient pas l'apparence d'un texte qui a été entré tout en lettres capitales. Le texte doit avoir été entré en lettres minuscules pour que les effets de cette option soient visibles.
  
|**Value**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Casse normale  <br/> |**visCaseNormal** <br/> |
| 0,1  <br/> | Toutes les lettres en capitales (majuscules)  <br/> |**visCaseAllCaps** <br/> |
| n°2  <br/> | Capitales initiales uniquement  <br/> |**visCaseInitialCaps** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Case par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char. case [ *i* ] où *i* = <1>, 2, 3,...  <br/> |
   
Pour obtenir une référence à la cellule Case à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +  *i* où *i* = 0, 1, 2,...  <br/> |
| Index de la cellule :  <br/> |**visCharacterCase** <br/> |
   

