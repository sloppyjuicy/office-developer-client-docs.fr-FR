---
title: Description, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise.
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360229"
---
# <a name="description-cell-action-tags-section"></a>Description Cell (Action Tags Section)

Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise.
  
## <a name="remarks"></a>Remarques

Pour faire référence à la cellule Description par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTag.  *nom* . Description où SmartTags. *Name* est le nom de la ligne de balise d'action  <br/> |
   
Pour faire référence à la cellule Description à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagDescription** <br/> |
   

