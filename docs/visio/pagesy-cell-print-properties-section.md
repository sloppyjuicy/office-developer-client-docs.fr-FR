---
title: PagesY, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033790
ms.localizationpriority: medium
ms.assetid: 396a0f3e-dbbb-3f5b-3c5d-f7dd454a765f
description: Détermine le nombre de pages d'impression sur lesquelles ajuster verticalement la page de dessin.
ms.openlocfilehash: 190cd49ff521a11c3daa70981bb17794a9a7b10b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627771"
---
# <a name="pagesy-cell-print-properties-section"></a>PagesY, cellule (section Print Properties)

Détermine le nombre de pages d'impression sur lesquelles ajuster verticalement la page de dessin. 
  
## <a name="remarks"></a>Remarques

Cette valeur n'est utilisée que lorsque la cellule OnPage est définie sur TRUE. 
  
Pour obtenir une référence à la cellule PagesY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | PagesY  <br/> |
   
Pour obtenir une référence à la cellule PagesY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPrintProperties** <br/> |
| Index de la cellule :  <br/> |**visPrintPropertiesPagesY** <br/> |
   

