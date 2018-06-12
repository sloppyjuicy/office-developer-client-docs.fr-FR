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
ms.openlocfilehash: 5b695ccf6fa2364809e2f5124b9f55ea6aab50e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789182"
---
# <a name="onpage-cell-print-properties-section"></a>OnPage, cellule (section Print Properties)

Indique si le dessin est imprimé sur un nombre spécifique de page d'impression. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|TRUE  <br/> |Ajuste la page de dessin sur un nombre défini de pages d’impression.  <br/> |
|FALSE  <br/> |N'ajuste pas la page de dessin sur un nombre défini de pages d'impression (valeur par défaut).  <br/> |
   
## <a name="remarks"></a>Note

Si la cellule OnPage est définie sur TRUE, Microsoft Visio utilise les cellules PagesX et PagesY pour déterminer le nombre de pages d’impression sur lesquelles ajuster le dessin. Les valeurs des cellules ScaleX et ScaleY sont ignorées. Ce paramètre peut être considéré comme un paramètre de « mise à l’échelle automatique ».
  
Cette valeur correspond à l’option **Ajuster** sur l’onglet **Configuration de l’impression** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ). 
  
Pour obtenir une référence à la cellule OnPage par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
|Nom de la cellule :  <br/> |OnPage  <br/> |
   
Pour obtenir une référence à la cellule OnPage par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
|Index de la section :  <br/> |**visSectionObject** <br/> |
|Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
|Index de la cellule :  <br/> |**visPrintPropertiesOnPage** <br/> |
   

