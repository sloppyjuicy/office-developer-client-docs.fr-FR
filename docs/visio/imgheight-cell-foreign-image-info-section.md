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
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344932"
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
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowForeign** <br/> |
| Index de la cellule :  <br/> |**visFrgnImgHeight** <br/> |
   

