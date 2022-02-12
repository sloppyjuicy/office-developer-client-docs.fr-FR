---
title: Case, cellule (section Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
ms.localizationpriority: medium
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Détermine la casse du texte de la forme. Toutes les lettres capitales (majuscules) (1) et Capitales initiales uniquement (2) ne modifient pas l'apparence d'un texte qui a été entré tout en lettres capitales. Le texte doit avoir été entré en lettres minuscules pour que les effets de cette option soient visibles.
ms.openlocfilehash: 839b1f92f62493e20f53d1549019028408aaf952
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782415"
---
# <a name="case-cell-character-section"></a>Case, cellule (section Character)

Détermine la casse du texte de la forme. Toutes les lettres capitales (majuscules) (1) et Capitales initiales uniquement (2) ne modifient pas l'apparence d'un texte qui a été entré tout en lettres capitales. Le texte doit avoir été entré en lettres minuscules pour que les effets de cette option soient visibles.
  
|**Valeur**|**Description**|**Constante d'automation**|
|:-----|:-----|:-----|
| 0  <br/> | Casse normale  <br/> |**visCaseNormal** <br/> |
| 1  <br/> | Toutes les lettres en capitales (majuscules)  <br/> |**visCaseAllCaps** <br/> |
| 2  <br/> | Capitales initiales uniquement  <br/> |**visCaseInitialCaps** <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Case par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Char.Case[  *i*  ] où  *i*  = <1>, 2, 3, ... |
   
Pour obtenir une référence à la cellule Case à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionCharacter** <br/> |
| Index de la ligne :  <br/> |**visRowCharacter** +   *i* où *i* = 0, 1, 2, ... |
| Index de la cellule :  <br/> |**visCharacterCase** <br/> |
   

