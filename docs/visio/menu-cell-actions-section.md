---
title: Menu, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Définit le nom d’une option de menu qui s’affiche dans un menu contextuel ou de balise d’action pour une forme ou une page.
ms.openlocfilehash: 195af94c4c36bb3c29a4fadab3c68f8334742952
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789172"
---
# <a name="menu-cell-actions-section"></a>Menu, cellule (section Actions)

Définit le nom d’une option de menu qui s’affiche dans un menu contextuel ou de balise d’action pour une forme ou une page. 
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Notes

Pour insérer un séparateur dans le menu au-dessus de cette option, utilisez la cellule BeginGroup. Pour faire apparaître la commande au bas du menu, faites précéder son nom d'un caractère de pourcentage (%) .
  
Pour obtenir une référence à la cellule Menu par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Actions. *nom* . Actions Menuwhere.  *nom* est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule Menu par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction** +  *i* où i = 0, 1, 2,...  <br/> |
|Index de la cellule :  <br/> |**visActionMenu** <br/> |
   

