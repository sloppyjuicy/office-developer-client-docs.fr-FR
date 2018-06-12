---
title: INTERSECTY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Renvoie la valeur y-coordonnée (dans le système de coordonnées local) du point d’intersectent de deux lignes.
ms.openlocfilehash: c3c0e9afef317ed4c647f1d236c4c3a29c6cdaa6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788837"
---
# <a name="intersecty-function"></a>INTERSECTY, fonction

Renvoie la valeur *y* -coordonnée (dans le système de coordonnées local) du point d’intersectent de deux lignes. 
  
## <a name="syntax"></a>Syntaxe

INTERSECTX (** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Obligatoire  <br/> |**Number** <br/> |_X_-coordonnées d’un point sur la première ligne.  <br/> |
| _y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |La valeur _y_-coordonnées d’un point sur la première ligne.  <br/> |
| _angle1_ <br/> |Obligatoire  <br/> |**Number** <br/> | Valeur de la cellule Angle de la première ligne.  <br/> |
| _x2_ <br/> |Obligatoire  <br/> |**Number** <br/> |_X_-coordonnées d’un point sur la deuxième ligne.  <br/> |
| _y2_ <br/> |Obligatoire  <br/> |**Number** <br/> |La valeur _y_-coordonnées d’un point sur la deuxième ligne.  <br/> |
| _angle2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Valeur de la cellule Angle de la deuxième ligne.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Note

Chaque ligne est définie par un point (*x, y*) et un angle. 
  
Microsoft Visio utilise cette fonction dans la cellule PinY d’une forme collée à un repère retourné. 
  
Si les lignes ne se coupent pas, la fonction renvoie une erreur Division par zéro (#DIV/0) que Visio ignore en restaurant la dernière valeur connue associée au point. 
  
## <a name="example"></a>Exemple

INTERSECTY (RepèreVert ! PinX, RepèreVert ! PinY, RepèreVert ! Angle, RepèreHoriz ! PinX, RepèreHoriz ! PinY, RepèreHoriz ! Angle) 
  
Renvoie la valeur *y* -coordonnées du point d’intersection de RepèreVert et RepèreHoriz en unités de page. 
  

