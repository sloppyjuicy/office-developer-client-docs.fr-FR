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
ms.openlocfilehash: 0b8c22357c6eb6ac6b5d0fc43117f0749dd1b106
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554557"
---
# <a name="intersectx-function"></a>Fonction INTERSECTX

Renvoie la  *coordonnée x*  (dans le système de coordonnées local) du point où deux lignes se coupent. 
  
## <a name="syntax"></a>Syntaxe

INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _x_ d’un point sur la première ligne.  <br/> |
| _y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _y_ d’un point sur la première ligne.  <br/> |
| _angle1_ <br/> |Obligatoire  <br/> |**Number** <br/> | Valeur de la cellule Angle de la première ligne.  <br/> |
| _x2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _x_ d’un point sur la deuxième ligne.  <br/> |
| _y2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _y_ d’un point sur la deuxième ligne.  <br/> |
| _angle2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Valeur de la cellule Angle de la deuxième ligne.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Chaque ligne est définie par un point (*x,y*) et un angle. 
  
Microsoft Visio utilise cette fonction dans la cellule PinX d’une forme collée à un repère retourné. 
  
Si les lignes ne se coupent pas, la fonction renvoie une erreur Division par zéro (#DIV/0) que Visio ignore en restaurant la dernière valeur connue associée au point. 
  
## <a name="example"></a>Exemple

INTERSECTX(VertGuide! PinX,VertGuide! PinY,VertGuide! Angle, HorzGuide ! PinX,HorzGuide! PinY,HorzGuide! Angle) 
  
Renvoie la  *coordonnée x*  du point d’intersection de VertGuide et HorzGuide en unités de page. 
  

