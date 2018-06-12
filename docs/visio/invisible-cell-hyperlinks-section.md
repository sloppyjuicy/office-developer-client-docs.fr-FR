---
title: Invisible, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page.
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788848"
---
# <a name="invisible-cell-hyperlinks-section"></a>Invisible, cellule (section Hyperlinks)

Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le lien hypertexte n'apparaît pas comme un élément de menu dans le menu contextuel.  <br/> |
|FALSE  <br/> |Le lien hypertexte apparaît comme un élément de menu dans le menu contextuel (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule Invisible par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Lien hypertexte. *nom* . Invisible, où le lien hypertexte *.name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule Invisible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionHyperlink** <br/> |
|Index de la ligne :  <br/> |**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visHLinkInvisible** <br/> |
   

