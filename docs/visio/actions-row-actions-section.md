---
title: Actions, ligne (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60017
localization_priority: Normal
ms.assetid: 29a7464a-b9d4-a8ea-161b-3044de32ed23
description: Contient les cellules qui spécifient les actions associées à une commande personnalisée dans un menu contextuel ou action de la balise. La section Actions contient une ligne Actions pour chaque action.
ms.openlocfilehash: f25ab75fe2bec35b09d2910ef731d11264224b7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788006"
---
# <a name="actions-row-actions-section"></a>Actions, ligne (section Actions)

Contient les cellules qui spécifient les actions associées à une commande personnalisée dans un menu contextuel ou action de la balise. La section Actions contient une ligne Actions pour chaque action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
Lignes actions sont nommées Actions. *nom* et contiennent les cellules suivantes. Pour plus d’informations, consultez les rubriques de la cellule spécifique. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |Contient la formule à exécuter lorsqu’un utilisateur choisit un élément dans un menu contextuel ou action de la balise.  <br/> |
|[Menu](menu-cell-actions-section.md) <br/> |Définit le nom de l’élément de menu qui s’affiche dans un menu contextuel ou de balise d’action.  <br/> |
|[TagName](tagname-cell-actions-section.md) <br/> |Nom logique de la balise d’action dans laquelle cette action doit apparaître.  <br/> |
|[ButtonFace](buttonface-cell-actions-section.md) <br/> |Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action.  <br/> |
|[SortKey](sortkey-cell-actions-section.md) <br/> |Numéro qui détermine l’ordre des options dans un menu contextuel ou de balise d’action.  <br/> |
|[Checked](checked-cell-actions-section.md) <br/> |Indique si l’élément de menu est cochée dans un menu contextuel ou de balise d’action.  <br/> |
|[Désactivé](disabled-cell-actions-section.md) <br/> |Indique si une option d’un menu contextuel ou de balise d’action est désactivée.  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |Indique si l'option de menu est en lecture seule (il est impossible de cliquer dessus).  <br/> |
|[Invisible](invisible-cell-actions-section.md) <br/> |Indique si l’option de menu est visible dans le menu contextuel ou de balise d’action.  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |Indique s’il faut insérer un séparateur dans le menu au-dessus de l’élément de menu.  <br/> |
   
## <a name="remarks"></a>Remarques

 Vous pouvez ajouter autant d’Actions.  *nom de* lignes que vous le souhaitez, assigner des noms explicites aux lignes et définir des valeurs de cellule. Pour ajouter une commande personnalisée à une section Actions existante, cliquez sur une ligne, cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez référencer ces cellules par leur nom de ligne, qui s’affiche dans une fenêtre feuille ShapeSheet en texte rouge. Pour attribuer un nom significatif à une ligne Actions. *nom de* ligne, cliquez sur la ligne, puis tapez un nom tel que *personnalisé* , par exemple, pour créer le nom de ligne Actions.personnalisée. Vous pouvez ensuite référencer la cellule Menu à l’aide d’actions.personnalisée.menu. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

