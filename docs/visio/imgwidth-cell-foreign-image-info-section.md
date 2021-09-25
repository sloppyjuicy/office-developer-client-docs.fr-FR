---
title: ImgWidth, cellule (section Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm460
ms.localizationpriority: medium
ms.assetid: b57fb962-0b3e-f2e5-3b88-3edf33e40496
description: "Détermine la largeur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :"
ms.openlocfilehash: d09728bcefe1b3f8f795d53cf03b7c09f173e51c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554606"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>ImgWidth, cellule (section Foreign Image Info)

Détermine la largeur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :
  
= Largeur \* 1
  
Toute découpe de l'objet modifie le facteur par lequel la largeur est multipliée.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule ImgWidth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ImgWidth  <br/> |
   
Pour obtenir une référence à la cellule ImgWidth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowForeign** <br/> |
| Index de la cellule :  <br/> |**visFrgnImgWidth** <br/> |
   

