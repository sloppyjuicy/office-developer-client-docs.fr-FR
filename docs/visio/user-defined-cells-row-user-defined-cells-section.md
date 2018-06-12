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
ms.openlocfilehash: 45a9a033fe486a14e9881c3d79b79a129ecedc1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789977"
---
# <a name="user-defined-cells-row-user-defined-cells-section"></a>User-defined Cells, ligne (section User-defined Cells)

Contient la valeur et le message descriptif de toutes les cellules définies par l'utilisateur de votre solution. Une forme contient une ligne User-defined Cells pour chaque paire de cellules Value/Prompt.
  
Lignes User-defined Cells sont nommées User. *nom* et contiennent les cellules suivantes. Pour plus d’informations, consultez les rubriques de la cellule spécifique. 
  
|**Cell**|**Description**|
|:-----|:-----|
|[Valeur](value-cell-user-defined-cells-section.md) <br/> |Indique une valeur pour la cellule définie par l'utilisateur correspondante.  <br/> |
|[Prompt](prompt-cell-user-defined-cells-section.md) <br/> |Indique un message descriptif ou commentaire pour la cellule définie par l'utilisateur.  <br/> |
   
## <a name="remarks"></a>Notes

Les cellules définies par l'utilisateur servent à entrer des formules ou constantes auxquelles d'autres cellules ou modules complémentaires font référence. Les valeurs des cellules définies par l'utilisateur sont portables. Cela signifie que, si une forme qui fait référence à une cellule définie par l'utilisateur dans une forme est copiée dans une autre forme ne possédant pas la même cellule définie par l'utilisateur, la cellule est ajoutée à la forme.
  
 Vous pouvez ajouter autant d’utilisateur.  *nom de* lignes que vous le souhaitez, assigner des noms explicites aux lignes et définir des valeurs de cellule. Pour ajouter une ligne à une section User-defined Cells existante, cliquez sur une ligne, cliquez sur **Insérer une ligne** dans le menu contextuel. 
  
Vous pouvez référencer ces cellules par leur nom de ligne, qui s’affiche dans une fenêtre feuille ShapeSheet en texte rouge. Pour attribuer des noms explicites pour l’utilisateur. *nom de* lignes, cliquez sur la ligne, puis tapez un nom tel que *décalage* , par exemple, pour créer le nom de ligne User.décalage. Vous pouvez ensuite référencer la cellule Prompt à l’aide d’User.décalage.Prompt. 
  
Le nom de ligne que vous entrez doit être unique dans la section.
  

