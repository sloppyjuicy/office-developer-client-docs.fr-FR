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
ms.openlocfilehash: 32e411b476bdd943e2294b7ba9943653ff0ce41c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577800"
---
# <a name="pagebottommargin-cell-print-properties-section"></a>PageBottomMargin, cellule (section Print Properties)

Indique la marge au bas de la page d'impression.
  
## <a name="remarks"></a>Remarques

Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 13 mm, la marge est de 13 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page. 
  
Pour obtenir une référence à la cellule PageBottomMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageBottomMargin  <br/> |
   
Pour obtenir une référence à la cellule PageBottomMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
| Index de la cellule :  <br/> |**visPrintPropertiesBottomMargin** <br/> |
   

