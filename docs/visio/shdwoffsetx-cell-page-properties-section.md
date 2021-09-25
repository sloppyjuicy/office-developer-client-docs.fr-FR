---
title: ShdwOffsetX, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
ms.localizationpriority: medium
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Détermine, en unités de page, la distance du décalage horizontal entre l'ombre d'une forme et la forme.
ms.openlocfilehash: 2f0bb37cb7f79f5721a5e4a7a0b98aacd5cdd99f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607660"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a>ShdwOffsetX, cellule (section Page Properties)

Détermine, en unités de page, la distance du décalage horizontal entre l'ombre d'une forme et la forme.
  
## <a name="remarks"></a>Remarques

Cette valeur est définie dans la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**). Elle est indépendante de l’échelle du dessin. Si le dessin est mis à l’échelle, le décalage de l’ombre reste le même. 
  
Pour obtenir une référence à la cellule ShdwOffsetX par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ShdwOffsetX  <br/> |
   
Pour obtenir une référence à la cellule ShdwOffsetX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowPage** <br/> |
| Index de la cellule :  <br/> |**visPageShdwOffsetX** <br/> |
   

