---
title: Menu, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
ms.localizationpriority: medium
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Définit le nom d’une option de menu qui s’affiche dans un menu contextuel ou de balise d’action pour une forme ou une page.
ms.openlocfilehash: 07edf16e0b80a4bf235f9adaa1b26c9a85adacd5
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369804"
---
# <a name="menu-cell-actions-section"></a>Menu, cellule (section Actions)

Définit le nom d’une option de menu qui s’affiche dans un menu contextuel ou de balise d’action pour une forme ou une page.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».
  
## <a name="remarks"></a>Remarques

Pour insérer un séparateur dans le menu au-dessus de cette option, utilisez la cellule BeginGroup. Pour afficher la commande en bas du menu, préfixez le nom avec un caractère de pourcentage (%).
  
Pour obtenir une référence à la cellule Menu par un nom à partir d’une autre formule ou d’un programme en faisant appel à la **propriété CellsU** , utilisez :
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Actions. *nom*  . Menu où actions. *nom* est le nom de la ligne Actions.  <br/> |

Pour obtenir une référence à la cellule Menu à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +   *i* où i = 0, 1, 2, ... |
|Index de la cellule :  <br/> |**visActionMenu** <br/> |
