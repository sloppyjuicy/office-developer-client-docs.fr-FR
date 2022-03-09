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
ms.openlocfilehash: e53f9ecaab78b20ffd103e0142ba5dfd3385cf80
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404522"
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
  
||Valeur |
|:-----|:-----|
|**Nom de cellule :**  <br/> |LineCap  <br/> |
   
Pour obtenir une référence à la cellule LineCap à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
|**Index de la section :**  <br/> |**visSectionObject** <br/> |
|**Index de la ligne :**  <br/> |**visRowLine** <br/> |
|**Index de la cellule :**  <br/> |**visLineEndCap** <br/> |
   

