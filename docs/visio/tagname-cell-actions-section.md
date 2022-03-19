---
title: TagName, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
ms.localizationpriority: medium
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Contient le nom de la balise d’action à laquelle cette action est associée.
ms.openlocfilehash: 87ccf12eafd2477e29d416daaa3e2ba8c08c4365
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634484"
---
# <a name="tagname-cell-actions-section"></a>TagName, cellule (section Actions)

Contient le nom de la balise d’action à laquelle cette action est associée.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

La cellule TagName de la section Actions fonctionne avec la cellule TagName de la section Action Tags pour associer une balise d’action à ses actions. 
  
- Si la cellule TagName d’une ligne Actions est vide, l’action apparaît dans un menu raccourci, et non dans un menu de balise d’action.
    
- Si une valeur de cellule TagName dans la ligne Actions correspond à la valeur de cellule TagName dans une ligne Smart Tags, l’action apparaît dans le menu de balise d’action.
    
- Si la cellule TagName d’une action a une valeur mais qu’elle ne correspond à la valeur TagName dans aucune ligne de balise de forme, cette action n’apparaît dans aucun menu de balise d’action ou menu raccourci.
    
- Si plusieurs lignes Smart Tags contiennent la même valeur TagName, elles présentent toutes les mêmes actions.
    
Pour obtenir une référence à la cellule TagName par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Actions. *nom*  . Actions TagNamewhere.  *name*  est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule TagName par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionAction** <br/> |
|**Index de la ligne :**  <br/> |**visRowAction** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visActionTagName** <br/> |
   

