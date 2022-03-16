---
title: INTERSECTX, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
ms.localizationpriority: medium
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: Renvoie la coordonnée x (dans le système de coordonnées local) du point où deux lignes se coupent.
ms.openlocfilehash: 4fdbe890b231303b881ae80d2fae991802a9d743
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63505988"
---
# <a name="intersectx-function"></a>Fonction INTERSECTX

Renvoie la  *coordonnée x*  (dans le système de coordonnées local) du point où deux lignes se coupent.
  
## <a name="syntax"></a>Syntaxe

INTERSECTX(***x1** _, _*_y1_*_, _*_angle1_*_, _*_x2_*_, _*_y2_*_, _ *_angle2_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *x1* <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  *x* d’un point sur la première ligne. |
| *y1* <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  *y* d’un point sur la première ligne. |
| *angle1* <br/> |Requis  <br/> |**Number** <br/> | Valeur de la cellule Angle de la première ligne. |
| *x2* <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  *x* d’un point sur la deuxième ligne. |
| *y2* <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  *y* d’un point sur la deuxième ligne. |
| *angle2* <br/> |Requis  <br/> |**Number** <br/> |Valeur de la cellule Angle de la deuxième ligne. |

### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Chaque ligne est définie par un point (*x,y*) et un angle.
  
Microsoft Visio utilise cette fonction dans la cellule PinX d’une forme collée à un repère retourné.
  
Si les lignes ne se coupent pas, la fonction renvoie une erreur Division par zéro (#DIV/0) que Visio ignore en restaurant la dernière valeur connue associée au point.
  
## <a name="example"></a>Exemple

INTERSECTX(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide ! PinX,HorzGuide! PinY,HorzGuide! Angle)
  
Renvoie la  *coordonnée x*  du point d’intersection de VertGuide et HorzGuide en unités de page.
  