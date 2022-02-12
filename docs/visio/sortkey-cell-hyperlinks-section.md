---
title: SortKey, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
ms.localizationpriority: medium
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Nombre qui détermine l'ordre des liens hypertexte apparaissant dans un menu contextuel.
ms.openlocfilehash: db6ed0d7962478a13306703b4c946ce93f00c1ca
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62775258"
---
# <a name="sortkey-cell-hyperlinks-section"></a>SortKey, cellule (section Hyperlinks)

Nombre qui détermine l'ordre des liens hypertexte apparaissant dans un menu contextuel.
  
## <a name="remarks"></a>Remarques

Les liens hypertexte d'un menu contextuel apparaissent dans le menu dans l'ordre croissant, les numéros les plus petits figurant en haut du menu. Si deux lignes de lien hypertexte ont la même valeur de cellule SortKey, le classement est déterminé par l'ordre physique des lignes. La valeur par défaut est 0 (zéro). 
  
Pour obtenir une référence à la cellule SortKey par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Lien hypertexte. *nom*  . SortKey où Hyperlink  *.name*  est le nom de la ligne  <br/> |
   
Pour obtenir une référence à la cellule SortKey par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionHyperlink** <br/> |
|Index de la ligne :  <br/> |**visRow1stHyperlink** +   *i* où *i* = 0, 1, 2... |
|Index de la cellule :  <br/> |**visHLinkSortKey** <br/> |
   

