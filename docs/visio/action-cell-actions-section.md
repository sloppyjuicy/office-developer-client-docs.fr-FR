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
ms.openlocfilehash: cb75bc42d7c0cfc60433883817f05723b1e1917e
ms.sourcegitcommit: 7b410a51d1e8c97e9cce8d4aa75074162b7d9485
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2022
ms.locfileid: "63448313"
---
# <a name="action-cell-actions-section"></a>Action, cellule (section Actions)

Contient la formule à exécuter lorsqu’un utilisateur choisit une commande de menu contextuel ou de balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

Une cellule Action n'est évaluée que lorsque l'action se produit, et non lorsque la formule est entrée.
  
Pour obtenir une référence à la cellule Action à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de cellule :**  <br/> | Actions.  *nom*  . Action où Actions. *name*  est le nom de la ligne actions  <br/> |
   
Pour obtenir une référence à la cellule Action à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionAction** <br/> |
| **Index de la ligne :**  <br/> |**visRowAction** +   *i* où *i* = 0, 1, 2... |
| **Index de la cellule :**  <br/> |**visActionAction** <br/> |
   

