---
title: PageBottomMargin, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60060
ms.localizationpriority: medium
ms.assetid: 7a97e97c-278d-2e1e-6c4f-f5f32e2cdeb0
description: Indique la marge au bas de la page d'impression.
ms.openlocfilehash: 4f1a2e626ea87dee9dc421ba9e1b7a4acb268012
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63426915"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>PageBottomMargin, cellule (section Print Properties)

Indique la marge au bas de la page d'impression.
  
## <a name="remarks"></a>Remarques

Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 13 mm, la marge est de 13 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page. 
  
Pour obtenir une référence à la cellule PageBottomMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | PageBottomMargin  <br/> |
   
Pour obtenir une référence à la cellule PageBottomMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowPrintProperties** <br/> |
| **Index de la cellule :**  <br/> |**visPrintPropertiesBottomMargin** <br/> |
   

