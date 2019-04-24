---
title: OnPage, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Indique si le dessin est imprimé sur un nombre spécifique de page d'impression.
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360983"
---
# <a name="onpage-cell-print-properties-section"></a>OnPage, cellule (section Print Properties)

Indique si le dessin est imprimé sur un nombre spécifique de page d'impression. 
  
|**Value**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Ajuste la page de dessin sur un nombre défini de pages d'impression.  <br/> |
|FALSE  <br/> |N'ajuste pas la page de dessin sur un nombre défini de pages d'impression (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Remarques

Si la cellule OnPage est définie sur TRUE, Microsoft Visio utilise les cellules PagesX et PagesY pour déterminer le nombre de pages d’impression sur lesquelles ajuster le dessin. Les valeurs des cellules ScaleX et ScaleY sont ignorées. Ce paramètre peut être considéré comme un paramètre de « mise à l’échelle automatique ».
  
Cette valeur correspond à l'option **ajuster** sur sous l'onglet Configuration de l' **impression** de la boîte de dialogue **mise en page** (sous l'onglet **création** , cliquez sur la flèche mise en **page** ). 
  
Pour obtenir une référence à la cellule OnPage par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |OnPage  <br/> |
   
Pour obtenir une référence à la cellule OnPage à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**Définis** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesOnPage** <br/> |
   

