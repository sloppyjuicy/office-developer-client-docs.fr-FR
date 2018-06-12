---
title: Action, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Contient la formule à exécuter lorsqu’un utilisateur choisit une commande de menu contextuel ou de balise d’action.
ms.openlocfilehash: 123b05f9a08c4ffa656e08a51f019f888cf83ed4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787996"
---
# <a name="action-cell-actions-section"></a>Action, cellule (section Actions)

Contient la formule à exécuter lorsqu’un utilisateur choisit une commande de menu contextuel ou de balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Notes

Une cellule Action n'est évaluée que lorsque l'action se produit, et non lorsque la formule est entrée.
  
Pour obtenir une référence à la cellule Action par un nom à partir d’une autre formule ou d’un programme à l’aide de la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Actions.  *nom* . Action où Actions. *nom* est le nom de la ligne actions  <br/> |
   
Pour obtenir une référence à la cellule Action par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionAction** <br/> |
| Index de la ligne :  <br/> |**visRowAction** +  *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visActionAction** <br/> |
   

