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
ms.openlocfilehash: c073184b58e8c5a352615c01fc667f60b2bc9e7b
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405085"
---
# <a name="invisible-cell-hyperlinks-section"></a>Invisible, cellule (section Hyperlinks)

Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Le lien hypertexte n'apparaît pas comme un élément de menu dans le menu contextuel. |
|FALSE  <br/> |Le lien hypertexte apparaît comme un élément de menu dans le menu contextuel (valeur par défaut). |
   
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Invisible par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |Lien hypertexte. *nom*  . Invisible où Hyperlink  *.name*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule Invisible à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionHyperlink** <br/> |
|**Index de la ligne :**  <br/> |**visRow1stHyperlink** +   *i* où *i* = 0, 1, 2... |
|**Index de la cellule :**  <br/> |**visHLinkInvisible** <br/> |
   

