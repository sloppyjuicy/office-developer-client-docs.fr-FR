---
title: BeginArrow, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Indique si un trait comporte une pointe de flèche ou autre format d’extrémité de trait à son premier sommet. Entrez un nombre compris entre 0 et 45 ou la fonction utilisation avec le nom d’une extrémité de trait personnalisé, ou utilisez la boîte de dialogue trait.
ms.openlocfilehash: c6d5a66d76cfea61b1c9923c5b904dadec5495f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788041"
---
# <a name="beginarrow-cell-line-format-section"></a>BeginArrow, cellule (section Line Format)

Indique si un trait comporte une pointe de flèche ou autre format d’extrémité de trait à son premier sommet. Entrez un nombre compris entre 0 et 45 ou la fonction utilisation avec le nom d’une extrémité de trait personnalisé, ou utilisez la boîte de dialogue **trait** . 
  
|**Valeur**|**Description**|
|:-----|:-----|
| 0  <br/> | Pas de pointe  <br/> |
| 1 - 45  <br/> | Styles de pointes de flèches assortis correspondant aux entrées indexées de la boîte de dialogue **trait** .  <br/> |
   
## <a name="remarks"></a>Notes

La taille de la pointe de flèche est définie dans la cellule BeginArrowSize.
  
Pour obtenir une référence à la cellule BeginArrow par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | BeginArrow  <br/> |
   
Pour obtenir une référence à la cellule BeginArrow par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowLine** <br/> |
| Index de la cellule :  <br/> |**visLineBeginArrow** <br/> |
   

