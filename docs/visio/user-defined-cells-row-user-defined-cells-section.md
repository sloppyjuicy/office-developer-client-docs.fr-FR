---
title: User-defined Cells, ligne (section User-defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3060
localization_priority: Normal
ms.assetid: 6c48b9b3-5c62-7d5a-1c8f-fe96606f4dea
description: Contient la valeur et le message descriptif de toutes les cellules définies par l'utilisateur de votre solution. Une forme contient une ligne User-defined Cells pour chaque paire de cellules Value/Prompt.
ms.openlocfilehash: 01e2da8ef1e97e8a911df605ab6cf1e9f8a853eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420688"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>User-defined Cells Row (User-defined Cells Section)

Contient la valeur et le message descriptif de toutes les cellules définies par l'utilisateur de votre solution. Une forme contient une ligne User-defined Cells pour chaque paire de cellules Value/Prompt.
  
Les lignes User-defined Cells sont nommées User. *et*  contiennent les cellules suivantes. Pour plus de détails, consultez les rubriques spécifiques aux cellules. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[Valeur](value-cell-user-defined-cells-section.md) <br/> |Indique une valeur pour la cellule définie par l'utilisateur correspondante.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Indique un message descriptif ou commentaire pour la cellule définie par l'utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Les cellules définies par l'utilisateur servent à entrer des formules ou constantes auxquelles d'autres cellules ou modules complémentaires font référence. Les valeurs des cellules définies par l'utilisateur sont portables. Cela signifie que, si une forme qui fait référence à une cellule définie par l'utilisateur dans une forme est copiée dans une autre forme ne possédant pas la même cellule définie par l'utilisateur, la cellule est ajoutée à la forme.
  
 Vous pouvez ajouter autant de lignes User.  *nommez*  les lignes selon vos besoins, attribuez des noms significatifs aux lignes et définissez des valeurs de cellule. Pour ajouter une ligne à une section User-defined Cells existante, cliquez avec le bouton droit de la souris, puis cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez désigner ces cellules à l'aide de leur nom de ligne, qui apparaît en rouge dans la fenêtre Feuille ShapeSheet. Pour assigner des noms parlants aux lignes User. *name*  rows, click the row, and then type a name such as  *Offset*  , for example, to create the row name User.Offset. Vous pouvez alors faire référence à la cellule Prompt en utilisant User.Décalage.Prompt. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

