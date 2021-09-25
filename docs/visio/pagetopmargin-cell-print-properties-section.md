---
title: PageTopMargin, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033785
ms.localizationpriority: medium
ms.assetid: 2ba0fd22-65a6-6cb6-da00-08f391705544
description: Indique la marge en haut de la page d'impression.
ms.openlocfilehash: 6b91f219f28f148aa6e341668d0ba0bd25437272
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577772"
---
# <a name="pagetopmargin-cell-print-properties-section"></a>PageTopMargin, cellule (section Print Properties)

Indique la marge en haut de la page d'impression.
  
## <a name="remarks"></a>Remarques

Cette valeur représente des unités physiques et n'est pas affectée par les unités d'échelle ou de dessin. Par exemple, si cette cellule a une valeur de 6,35 mm, la marge est de 6,35 mm, même si les unités de page sont des cm. Si les unités ne sont pas explicitement mentionnées, cette valeur s'exprime par défaut en unités de page. 
  
Pour obtenir une référence à la cellule PageTopMargin par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PageTopMargin  <br/> |
   
Pour obtenir une référence à la cellule PageTopMargin à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
| Index de la cellule :  <br/> |**visPrintPropertiesTopMargin** <br/> |
   

