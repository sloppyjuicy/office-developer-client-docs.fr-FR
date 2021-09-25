---
title: SortKey, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
ms.localizationpriority: medium
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Numéro qui détermine l’ordre des actions qui apparaissent dans un menu contextuel ou de balise d’action.
ms.openlocfilehash: 563bb5213d2fe1e43c16648ecef0955c779a4348
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598009"
---
# <a name="sortkey-cell-actions-section"></a>SortKey, cellule (section Actions)

Numéro qui détermine l’ordre des actions qui apparaissent dans un menu contextuel ou de balise d’action.
  
> [!NOTE]
> Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ». 
  
## <a name="remarks"></a>Remarques

Les actions d’un menu contextuel ou de balise d’action y apparaissent triées de la plus basse à la plus élevée, celles avec les numéros les plus bas figurant en haut du menu. Si deux lignes d’action ont la même valeur de cellule SortKey, le classement est déterminé par l’ordre physique des lignes. La valeur par défaut est 0 (zéro).
  
Pour obtenir une référence à la cellule SortKey à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |Actions. *nom*  . SortKeywhere Actions.  *name*  est le nom de la ligne Actions  <br/> |
   
Pour obtenir une référence à la cellule SortKey par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionAction** <br/> |
|Index de la ligne :  <br/> |**visRowAction**  +   *i* où *i* = 0, 1, 2...  <br/> |
|Index de la cellule :  <br/> |**visActionSortKey** <br/> |
   

