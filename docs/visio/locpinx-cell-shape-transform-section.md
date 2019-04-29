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
description: "Représente la coordonnée x de l'axe de la forme (Centre de rotation) par rapport à l'origine de la forme. La formule par défaut permettant de déterminer LocPinX est la suivante :"
ms.openlocfilehash: 2eb5c328eed3c97652173670c426b83b8c358833
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439239"
---
# <a name="locpinx-cell-shape-transform-section"></a>LocPinX, cellule (section Shape Transform)

Représente la coordonnée *x* de l'axe de la forme (Centre de rotation) par rapport à l'origine de la forme. La formule par défaut permettant de déterminer LocPinX est la suivante : 
  
= Largeur \* 0,5
  
## <a name="remarks"></a>Remarques

Pour obtenir une référence à la cellule LocPinX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez : 
  
|||
|:-----|:-----|
| Nom de la cellule :  <br/> | LocPinX  <br/> |
   
Pour obtenir une référence à la cellule LocPinX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants : 
  
|||
|:-----|:-----|
| Index de la section :  <br/> |**Définis** <br/> |
| Index de la ligne :  <br/> |**visRowXFormOut** <br/> |
| Index de la cellule :  <br/> |**visXFormLocPinX** <br/> |
   

