---
title: EndArrow, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
ms.localizationpriority: medium
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de ligne à son dernier sommet.
ms.openlocfilehash: 76fcad7fbecea6f249eb41ef3d933c5ea8f59257
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506959"
---
# <a name="endarrow-cell-line-format-section"></a>EndArrow, cellule (section Line Format)

Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de ligne à son dernier sommet.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Pas de pointe |
|1 - 45  <br/> |Styles de pointes de flèches assortis correspondant aux entrées indexées de la boîte de dialogue **Trait**. |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir cette valeur dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Flèches**, puis cliquez sur **Autres flèches**). La taille de la pointe de flèche est définie dans la cellule TailleFlècheFin.
  
Vous pouvez définir une extrémité de trait personnalisée à l'aide de la fonction USE dans cette cellule. 
  
Pour obtenir une référence à la cellule EndArrow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
|**Nom de la cellule :**  <br/> |EndArrow  <br/> |
   
Pour obtenir une référence à la cellule EndArrow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLine** <br/> |
|**Index de la cellule :**  <br/> |**visLineEndArrow** <br/> |
   

