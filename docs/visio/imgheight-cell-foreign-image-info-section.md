---
title: ImgHeight, cellule (section Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
ms.localizationpriority: medium
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: "Détermine la hauteur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :"
ms.openlocfilehash: 927b614e7e0b8113c96f7965c5f9b84b9a6c5b78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628163"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>ImgHeight, cellule (section Foreign Image Info)

Détermine la hauteur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :
  
= Hauteur \* 1
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule ImgHeight par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ImgHeight  <br/> |
   
Pour obtenir une référence à la cellule ImgHeight à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowForeign** <br/> |
| Index de la cellule :  <br/> |**visFrgnImgHeight** <br/> |
   

