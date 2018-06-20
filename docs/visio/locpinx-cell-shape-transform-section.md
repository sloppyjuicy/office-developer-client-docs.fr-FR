---
title: LocPinX, cellule (section Shape Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm680
localization_priority: Normal
ms.assetid: b82feade-5793-8a6e-3ff4-69a4cbdd2cf9
description: 'Représente le x-coordonnées de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinX est la suivante :'
ms.openlocfilehash: 17f7b0fde9a54f6596f2f87f866d30b908e062b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789048"
---
# <a name="locpinx-cell-shape-transform-section"></a>LocPinX, cellule (section Shape Transform)

Représente le *x* -coordonnées de l’axe de la forme (centre de rotation) par rapport à l’origine de la forme. La formule par défaut permettant de déterminer LocPinX est la suivante : 
  
= Largeur \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LocPinX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LocPinX  <br/> |
   
Pour obtenir une référence à la cellule LocPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**visSectionObject** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormLocPinX** <br/> |
   

