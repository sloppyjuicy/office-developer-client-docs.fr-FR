---
title: SortKey, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Nombre qui détermine l'ordre des liens hypertexte apparaissant dans un menu contextuel.
ms.openlocfilehash: 03596918924b04a776eb7ffd2f16db1c57de8194
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789793"
---
# <a name="sortkey-cell-hyperlinks-section"></a>SortKey, cellule (section Hyperlinks)

Nombre qui détermine l'ordre des liens hypertexte apparaissant dans un menu contextuel.
  
## <a name="remarks"></a>Note

Les liens hypertexte d'un menu contextuel apparaissent dans le menu dans l'ordre croissant, les numéros les plus petits figurant en haut du menu. Si deux lignes de lien hypertexte ont la même valeur de cellule SortKey, le classement est déterminé par l'ordre physique des lignes. La valeur par défaut est 0 (zéro). 
  
Pour obtenir une référence à la cellule SortKey par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |Lien hypertexte. *nom* . SortKey, où le lien hypertexte *.name* est le nom de ligne  <br/> |
   
Pour obtenir une référence à la cellule SortKey par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionHyperlink** <br/> |
|Index de la ligne :  <br/> |**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visHLinkSortKey** <br/> |
   

