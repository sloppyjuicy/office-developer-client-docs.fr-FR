---
title: LocPinY, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm685
localization_priority: Normal
ms.assetid: a29c5d4e-d3d6-d984-495a-4b0b130352ef
description: 'Représente la valeur y-coordonnées de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinY est la suivante :'
ms.openlocfilehash: 8d98906e8082af0fc54bc01fe3a8537b66ac56b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789035"
---
# <a name="locpiny-cell-shape-transform-section"></a>LocPinY, cellule (section Shape Transform)

Représente la valeur *y* -coordonnées de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinY est la suivante : 
  
= Hauteur \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LocPinY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LocPinY  <br/> |
   
Pour obtenir une référence à la cellule LocPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormLocPinY** <br/> |
   

