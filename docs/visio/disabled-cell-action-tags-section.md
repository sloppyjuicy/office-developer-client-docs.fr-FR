---
title: Disabled, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Indique si la balise d’action s’affiche dans la fenêtre de dessin.
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788472"
---
# <a name="disabled-cell-action-tags-section"></a>Disabled, cellule (section Action Tags)

Indique si la balise d’action s’affiche dans la fenêtre de dessin.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
|**Valeur**|**Description**|
|:-----|:-----|
| TRUE  <br/> | La balise d’action est désactivée.  <br/> |
| FALSE  <br/> | La balise d’action est activée (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Note

Lorsqu’une balise d’action est désactivée, elle ne s’affiche plus du tout tant qu’elle n’est pas réactivée. 
  
Pour obtenir une référence à la cellule Disabled par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Balises actives.  *nom* . Désactivé où SmartTags. *nom* est le nom de la ligne de balise d’action  <br/> |
   
Pour obtenir une référence à la cellule Disabled par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionSmartTag** <br/> |
| Index de la ligne :  <br/> |**visRowSmartTag** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visSmartTagDisabled** <br/> |
   

