---
title: LineCap, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
ms.localizationpriority: medium
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: Indique si l'extrémité du trait est arrondie, carrée ou étendue.
ms.openlocfilehash: b062ff673d561a7c328b361fea8da0c4f67024c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615899"
---
# <a name="linecap-cell-line-format-section"></a>LineCap, cellule (section Line Format)

Indique si l'extrémité du trait est arrondie, carrée ou étendue.
  
|**Valeur**|**Style de l'extrémité du trait**|
|:-----|:-----|
|0  <br/> |Arrondi  <br/> |
|1  <br/> |Square  <br/> |
|2  <br/> |Étendue  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **Trait** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Trait**, pointez sur **Flèches**, puis cliquez sur **Autres flèches**).
  
Pour obtenir une référence à la cellule LineCap par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de cellule :  <br/> |LineCap  <br/> |
   
Pour obtenir une référence à la cellule LineCap à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowLine** <br/> |
|Index de la cellule :  <br/> |**visLineEndCap** <br/> |
   

