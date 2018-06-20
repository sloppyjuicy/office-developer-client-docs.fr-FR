---
title: LineCap, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Indique si l'extrémité du trait est arrondie, carrée ou étendue.
ms.openlocfilehash: 1bd427801e6d95ce6167fa9681da2c567307f072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788949"
---
# <a name="linecap-cell-line-format-section"></a>LineCap, cellule (section Line Format)

Indique si l'extrémité du trait est arrondie, carrée ou étendue.
  
|**Valeur**|**Style de fin de ligne**|
|:-----|:-----|
|0  <br/> |Arrondi  <br/> |
|1  <br/> |Carré  <br/> |
|2  <br/> |Étendu  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **flèches**, puis cliquez sur **Autres flèches**).
  
Pour obtenir une référence à la cellule LineCap par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |LineCap  <br/> |
   
Pour obtenir une référence à la cellule LineCap par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLineEndCap** <br/> |
   

