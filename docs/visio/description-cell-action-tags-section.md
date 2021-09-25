---
title: Description, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
ms.localizationpriority: medium
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise.
ms.openlocfilehash: f1e5da6f083d6063403a24df2c980807b441b7b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586557"
---
# <a name="description-cell-action-tags-section"></a>Description Cell (Action Tags Section)

Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise.
  
## <a name="remarks"></a>Remarques

Pour faire référence à la cellule Description par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTags.  *nom*  . Description où SmartTags. *name est*  le nom de la ligne de balise d’action  <br/> |
   
Pour faire référence à la cellule Description à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagDescription** <br/> |
   

