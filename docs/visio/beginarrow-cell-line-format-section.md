---
title: BeginArrow, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
ms.localizationpriority: medium
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de trait à son premier sommet. Entrez un nombre compris entre 0 et 45 ou la fonction UTILISATION avec le nom d'une extrémité de trait personnalisée ou utilisez la boîte de dialogue Trait.
ms.openlocfilehash: 9d52213052324d4ae3f45ca5f813e71330b7bbb6
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522645"
---
# <a name="beginarrow-cell-line-format-section"></a>BeginArrow, cellule (section Line Format)

Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de trait à son premier sommet. Entrez un nombre compris entre 0 et 45 ou la fonction UTILISATION avec le nom d'une extrémité de trait personnalisée ou utilisez la boîte de dialogue **Trait**. 
  
|**Valeur**|**Description**|
|:-----|:-----|
| 0  <br/> | Pas de pointe |
| 1 - 45  <br/> | Styles de pointes de flèches assortis correspondant aux entrées indexées de la boîte de dialogue **Trait**. |
   
## <a name="remarks"></a>Remarques

La taille de la pointe de flèche est définie dans la cellule BeginArrowSize.
  
Pour obtenir une référence à la cellule BeginArrow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | BeginArrow  <br/> |
   
Pour obtenir une référence à la cellule BeginArrow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowLine** <br/> |
| **Index de la cellule :**  <br/> |**visLineBeginArrow** <br/> |
   

