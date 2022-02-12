---
title: INTERSECTY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
ms.localizationpriority: medium
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: Renvoie la coordonnée y (dans le système de coordonnées local) du point où deux lignes se coupent.
ms.openlocfilehash: 7687a64e00840186d4da3f7472f847d1c08f7ea2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62786846"
---
# <a name="intersecty-function"></a>Fonction INTERSECTY

Renvoie la  *coordonnée y*  (dans le système de coordonnées local) du point où deux lignes se coupent. 
  
## <a name="syntax"></a>Syntaxe

INTERSECTX(***x1** _, _*_y1_*_, _*_angle1_*_, _*_x2_*_, _*_y2_*_, _ *_angle2_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _x_ d’un point sur la première ligne. |
| _y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _y_ d’un point sur la première ligne. |
| _angle1_ <br/> |Requis  <br/> |**Number** <br/> | Valeur de la cellule Angle de la première ligne. |
| _x2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _x_ d’un point sur la deuxième ligne. |
| _y2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _y_ d’un point sur la deuxième ligne. |
| _angle2_ <br/> |Requis  <br/> |**Number** <br/> |Valeur de la cellule Angle de la deuxième ligne. |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Chaque ligne est définie par un point (*x,y*) et un angle. 
  
Microsoft Visio utilise cette fonction dans la cellule PinY d’une forme collée à un repère retourné. 
  
Si les lignes ne se coupent pas, la fonction renvoie une erreur Division par zéro (#DIV/0) que Visio ignore en restaurant la dernière valeur connue associée au point. 
  
## <a name="example"></a>Exemple

INTERSECTY(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide ! PinX,HorzGuide! PinY,HorzGuide! Angle) 
  
Renvoie la  *coordonnée y*  du point d’intersection de VertGuide et HorzGuide en unités de page. 
  

