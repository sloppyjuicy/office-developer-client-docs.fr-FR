---
title: ImgHeight, cellule (section Foreign Image Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: "Détermine la hauteur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :"
ms.openlocfilehash: 983bb919dbfada65b6d9af464ecfa17c04e970c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788820"
---
# <a name="imgheight-cell-foreign-image-info-section"></a>ImgHeight, cellule (section Foreign Image Info)

Détermine la hauteur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :
  
= Hauteur \* 1
  
## <a name="remarks"></a>Note

Pour obtenir une référence à la cellule ImgHeight par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | ImgHeight  <br/> |
   
Pour obtenir une référence à la cellule ImgHeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowForeign** <br/> |
| Index de la cellule :  <br/> |**visFrgnImgHeight** <br/> |
   

