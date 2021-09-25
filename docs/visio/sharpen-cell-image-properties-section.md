---
title: Sharpen, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
ms.localizationpriority: medium
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: Améliore la netteté d'une image bitmap. La valeur par défaut est 0 %. L'accentuation d'une image consiste essentiellement à augmenter le contraste de pixels adjacents.
ms.openlocfilehash: 1728192737ab8dcfc6f124abfa2c3040a947347d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559555"
---
# <a name="sharpen-cell-image-properties-section"></a>Sharpen, cellule (section Image Properties)

Améliore la netteté d'une image bitmap. La valeur par défaut est 0 %. L'accentuation d'une image consiste essentiellement à augmenter le contraste de pixels adjacents.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule Sharpen par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | Accentuer  <br/> |
   
Pour obtenir une référence à la cellule Sharpen par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowImage** <br/> |
| Index de la cellule :  <br/> |**visImageSharpen** <br/> |
   

