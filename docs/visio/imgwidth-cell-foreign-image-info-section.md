---
title: ImgWidth, cellule (section Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
localization_priority: Normal
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: "Détermine la largeur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :"
ms.openlocfilehash: 3aab65d27d426287060f7572dad15174acb93199
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788818"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>ImgWidth, cellule (section Foreign Image Info)

Détermine la largeur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :
  
= Largeur \* 1
  
Toute découpe de l'objet modifie le facteur par lequel la largeur est multipliée.
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule ImgWidth par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ImgWidth  <br/> |
   
Pour obtenir une référence à la cellule ImgWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowForeign** <br/> |
| Index de la cellule :  <br/> |**visFrgnImgWidth** <br/> |
   

