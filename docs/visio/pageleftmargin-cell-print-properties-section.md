---
title: PageLeftMargin, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60061
ms.localizationpriority: medium
ms.assetid: 7ecdfc37-c9d4-2fde-ed3e-be81657c24e2
description: Indique la marge de gauche de la page d'impression.
ms.openlocfilehash: 6f4728e1dfea50ce0fb8c5d56b1778048c14841d
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455467"
---
# <a name="pageleftmargin-cell-print-properties-section"></a>PageLeftMargin, cellule (section Print Properties)

Indique la marge de gauche de la page d'impression.
  
## <a name="remarks"></a>Remarques

Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 6,35 mm, la marge est de 6,35 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page. 
  
Pour obtenir une référence à la cellule PageLeftMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | PageLeftMargin  <br/> |
   
Pour obtenir une référence à la cellule PageLeftMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPrintProperties** <br/> |
| **Index de la cellule :**  <br/> |**visPrintPropertiesLeftMargin** <br/> |
   

