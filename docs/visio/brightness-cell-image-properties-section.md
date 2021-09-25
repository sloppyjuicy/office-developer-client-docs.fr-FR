---
title: Brightness, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
ms.localizationpriority: medium
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: Règle la luminosité d'une image bitmap. Réduisez la luminosité de l'image en entrant une valeur comprise entre 0 et 49 % ou augmentez-la en entrant une valeur comprise entre 51 et 100 %. La valeur par défaut est 50 %.
ms.openlocfilehash: 41615007b66a0b148c9166ee76126b935a5327c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578143"
---
# <a name="brightness-cell-image-properties-section"></a>Brightness, cellule (section Image Properties)

Règle la luminosité d'une image bitmap. Réduisez la luminosité de l'image en entrant une valeur comprise entre 0 et 49 % ou augmentez-la en entrant une valeur comprise entre 51 et 100 %. La valeur par défaut est 50 %.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Brightness par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Brightness  <br/> |
   
Pour obtenir une référence à la cellule Brightness à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowImage** <br/> |
| Index de la cellule :  <br/> |**visImageBrightness** <br/> |
   

