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
ms.openlocfilehash: 628aa10aa07f3ab5c3cfb20adbcf67374bcd5f40
ms.sourcegitcommit: 4164855836af53a068bbbc5b5d126f83ee83e324
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2022
ms.locfileid: "63427188"
---
# <a name="imgwidth-cell-foreign-image-info-section"></a>ImgWidth, cellule (section Foreign Image Info)

Détermine la largeur de l'image de l'objet à l'intérieur de ses bordures. La formule par défaut est la suivante :
  
= Largeur \* 1
  
Toute découpe de l'objet modifie le facteur par lequel la largeur est multipliée.
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule ImgWidth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
||Valeur |
|:-----|:-----|
| **Nom de la cellule :**  <br/> | ImgWidth  <br/> |
   
Pour obtenir une référence à la cellule ImgWidth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
||Valeur |
|:-----|:-----|
| **Index de la section :**  <br/> |**visSectionObject** <br/> |
| **Index de la ligne :**  <br/> |**visRowForeign** <br/> |
| **Index de la cellule :**  <br/> |**visFrgnImgWidth** <br/> |
   

