---
title: LocPinY, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
ms.localizationpriority: medium
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Représente la coordonnée y de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinY est la suivante :'
ms.openlocfilehash: 3e9ff2fd0daf3f75e1e1b341a37836e0ccc70831
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623361"
---
# <a name="locpiny-cell-shape-transform-section"></a>LocPinY, cellule (section Shape Transform)

Représente la  *coordonnée y*  de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinY est la suivante : 
  
= Hauteur \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LocPinY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LocPinY  <br/> |
   
Pour obtenir une référence à la cellule LocPinY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormLocPinY** <br/> |
   

