---
title: Action, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
ms.localizationpriority: medium
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Contient la formule à exécuter lorsqu’un utilisateur choisit une commande de menu contextuel ou de balise d’action.
ms.openlocfilehash: 8e1aec829904719f71dde6e87905784e78bd0a1d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608696"
---
# <a name="action-cell-actions-section"></a>Action, cellule (section Actions)

Contient la formule à exécuter lorsqu’un utilisateur choisit une commande de menu contextuel ou de balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

Une cellule Action n'est évaluée que lorsque l'action se produit, et non lorsque la formule est entrée.
  
Pour obtenir une référence à la cellule Action à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de cellule :  <br/> | Actions.  *nom*  . Action où Actions. *name*  est le nom de la ligne actions  <br/> |
   
Pour obtenir une référence à la cellule Action à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionAction** <br/> |
| Index de la ligne :  <br/> |**visRowAction**  +   *i* où *i* = 0, 1, 2...  <br/> |
| Index de la cellule :  <br/> |**visActionAction** <br/> |
   

