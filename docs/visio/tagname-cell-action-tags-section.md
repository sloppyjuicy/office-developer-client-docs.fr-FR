---
title: TagName, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
ms.localizationpriority: medium
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Nom de la balise d’action utilisé comme référence pour associer la balise d’action à ses actions.
ms.openlocfilehash: 09bd43f69e1adb757ab71e34b232f79affa10e2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622752"
---
# <a name="tagname-cell-action-tags-section"></a>TagName, cellule (section Action Tags)

Nom de la balise d’action utilisé comme référence pour associer la balise d’action à ses actions.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

 La cellule TagName de la section Action Tags fonctionne avec la cellule TagName de la section Actions pour associer une balise d’action à ses actions. Les lignes de la section Actions ont également une cellule TagName, et ces lignes avec la même valeur de cellule TagName que cette cellule définissent les actions à prendre pour cette balise d’action. 
  
Pour obtenir une référence à la cellule TagName à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTags.  *nom*  . TagName où SmartTags. *name est*  le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule TagName par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagName** <br/> |
   

