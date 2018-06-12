---
title: EndArrow, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm320
localization_priority: Normal
ms.assetid: 2f9c11ba-a316-bc34-60d4-0a41b2af486f
description: Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de ligne à son dernier sommet.
ms.openlocfilehash: fa37e4896fdab0f2e8fee6d94aa38c72519a7e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788553"
---
# <a name="endarrow-cell-line-format-section"></a>EndArrow, cellule (section Line Format)

Indique si un trait comporte une pointe de flèche ou un autre format d'extrémité de ligne à son dernier sommet.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Pas de pointe  <br/> |
|1 - 45  <br/> |Styles de pointes de flèches assortis correspondant aux entrées indexées de la boîte de dialogue **trait** .  <br/> |
   
## <a name="remarks"></a>Note

Vous pouvez également définir cette valeur dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **flèches**, puis cliquez sur **Autres flèches**). La taille de la pointe de flèche est définie dans la cellule EndArrowSize.
  
Vous pouvez définir une extrémité de trait personnalisée à l'aide de la fonction USE dans cette cellule. 
  
Pour obtenir une référence à la cellule EndArrow par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |EndArrow  <br/> |
   
Pour obtenir une référence à la cellule EndArrow par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLineEndArrow** <br/> |
   

