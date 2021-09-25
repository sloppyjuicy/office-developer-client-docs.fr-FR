---
title: Invisible, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
ms.localizationpriority: medium
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page.
ms.openlocfilehash: b0c353f30f4438957334ec79090e3598a84e970e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582602"
---
# <a name="invisible-cell-hyperlinks-section"></a>Invisible, cellule (section Hyperlinks)

Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le lien hypertexte n'apparaît pas comme un élément de menu dans le menu contextuel.  <br/> |
|FALSE  <br/> |Le lien hypertexte apparaît comme un élément de menu dans le menu contextuel (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Invisible par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Lien hypertexte. *nom*  . Invisible où Hyperlink  *.name*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Invisible à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionHyperlink** <br/> |
|Index de la ligne :  <br/> |**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visHLinkInvisible** <br/> |
   

