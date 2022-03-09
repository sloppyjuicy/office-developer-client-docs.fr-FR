---
title: INTERSECTX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
ms.localizationpriority: medium
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Renvoie la coordonnée x (dans le système de coordonnées local) du point où deux lignes se coupent.
ms.openlocfilehash: 3195fc8b9360f7ec1caac5afd2807388d9c001f8
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368558"
---
# <a name="intersectx-function"></a>Fonction INTERSECTX

Renvoie la  *coordonnée x*  (dans le système de coordonnées local) du point où deux lignes se coupent. 
  
## <a name="syntax"></a>Syntaxe

INTERSECTX(***x1** _, _*_y1_*_, _*_angle1_*_, _*_x2_*_, _*_y2_*_, _ *_angle2_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _x_ d’un point sur la première ligne. |
| _y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _y_ d’un point sur la première ligne. |
| _angle1_ <br/> |Obligatoire  <br/> |**Number** <br/> | Valeur de la cellule Angle de la première ligne. |
| _x2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _x_ d’un point sur la deuxième ligne. |
| _y2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _y_ d’un point sur la deuxième ligne. |
| _angle2_ <br/> |Requis  <br/> |**Number** <br/> |Valeur de la cellule Angle de la deuxième ligne. |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Chaque ligne est définie par un point (*x,y*) et un angle. 
  
Microsoft Visio utilise cette fonction dans la cellule PinX d’une forme collée à un repère retourné. 
  
Si les lignes ne se coupent pas, la fonction renvoie une erreur Division par zéro (#DIV/0) que Visio ignore en restaurant la dernière valeur connue associée au point. 
  
## <a name="example"></a>Exemple

INTERSECTX(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide ! PinX,HorzGuide! PinY,HorzGuide! Angle) 
  
Renvoie la  *coordonnée x*  du point d’intersection de VertGuide et HorzGuide en unités de page. 
  

