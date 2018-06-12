---
title: PageRightMargin, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60062
localization_priority: Normal
ms.assetid: f864c759-ed94-8ab7-d664-cc04b3ed743e
description: Indique la marge de droite de la page d'impression.
ms.openlocfilehash: 951a16ff20e294b68ed5447d330f4e7cbc100c82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789209"
---
# <a name="pagerightmargin-cell-print-properties-section"></a>PageRightMargin, cellule (section Print Properties)

Indique la marge de droite de la page d'impression.
  
## <a name="remarks"></a>Note

Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 6,35 mm, la marge est de 6,35 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page. 
  
Pour obtenir une référence à la cellule PageRightMargin par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageRightMargin  <br/> |
   
Pour obtenir une référence à la cellule PageRightMargin par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
| Index de la cellule :  <br/> |**visPrintPropertiesRightMargin** <br/> |
   

