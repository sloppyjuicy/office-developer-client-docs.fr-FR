---
title: Actions, ligne (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60017
ms.localizationpriority: medium
ms.assetid: 29a7464a-b9d4-a8ea-161b-3044de32ed23
description: Contient des cellules qui spécifient les actions associées à une commande personnalisée dans un menu de raccourci ou de balise d’action. La section Actions contient une ligne Actions pour chaque action.
ms.openlocfilehash: f0271ea3097dd77b7a0c9f3a0edc70b5cac727d1
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774635"
---
# <a name="actions-row-actions-section"></a>Actions, ligne (section Actions)

Contient des cellules qui spécifient les actions associées à une commande personnalisée dans un menu de raccourci ou de balise d’action. La section Actions contient une ligne Actions pour chaque action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
Les lignes Actions sont nommées Actions. *et*  contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |Contient la formule à exécuter lorsqu’un utilisateur choisit une option dans un menu contextuel ou de balise d’action. |
|[Menu](menu-cell-actions-section.md) <br/> |Définit le nom de l’élément de menu qui apparaît dans une balise d’action ou un menu raccourci. |
|[TagName](tagname-cell-actions-section.md) <br/> |Nom logique de la balise d’action dans laquelle cette action doit apparaître. |
|[ButtonFace](buttonface-cell-actions-section.md) <br/> |Identifie l’icône qui s’affiche en regard d’une option de menu contextuel ou de balise d’action. |
|[SortKey](sortkey-cell-actions-section.md) <br/> |Numéro qui détermine l’ordre des options dans un menu contextuel ou de balise d’action. |
|[Checked](checked-cell-actions-section.md) <br/> |Indique si l’élément de menu est vérifié dans une balise d’action ou un menu raccourci. |
|[Disabled](disabled-cell-actions-section.md) <br/> |Indique si une option d’un menu contextuel ou de balise d’action est désactivée. |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |Indique si l'option de menu est en lecture seule (il est impossible de cliquer dessus). |
|[Invisible](invisible-cell-actions-section.md) <br/> |Indique si l’option de menu est visible dans le menu contextuel ou de balise d’action. |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |Indique s’il faut insérer un séparateur dans le menu, au-dessus de l’élément de menu. |
   
## <a name="remarks"></a>Remarques

 Vous pouvez ajouter autant de lignes Actions.  *nommez*  les lignes selon vos besoins, attribuez des noms significatifs aux lignes et définissez des valeurs de cellule. Pour ajouter une commande personnalisée à une section Actions existante, cliquez avec le bouton droit de la souris, puis cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez désigner ces cellules à l’aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet. Pour assigner un nom parlant à une ligne Actions. *name*  row, click the row, and then type a name such as  *Custom*  , for example, to create the row name Actions.Custom. Vous pouvez alors faire référence à la cellule Menu en utilisant Actions.Personnalisée.Menu. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

