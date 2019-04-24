---
title: TagName, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Nom de la balise d’action utilisé comme référence pour associer la balise d’action à ses actions.
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332395"
---
# <a name="tagname-cell-action-tags-section"></a>TagName, cellule (section Action Tags)

Nom de la balise d’action utilisé comme référence pour associer la balise d’action à ses actions.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

 La cellule TagName de la section Action Tags fonctionne avec la cellule TagName de la section Actions pour associer une balise d’action à ses actions. Les lignes de la section actions ont également une cellule TagName, et les lignes avec la même valeur de cellule TagName que cette cellule définissent les actions à effectuer pour cette balise d'action. 
  
Pour obtenir une référence à la cellule TagName à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | SmartTag.  *nom* . TagName où SmartTags. *Name* est le nom de la ligne de balise d'action  <br/> |
   
Pour obtenir une référence à la cellule TagName par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagName** <br/> |
   

