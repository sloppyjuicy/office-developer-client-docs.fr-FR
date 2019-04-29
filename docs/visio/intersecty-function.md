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
description: Renvoie la coordonnée y (dans le système de coordonnées locales) du point d'intersection de deux lignes.
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426099"
---
# <a name="intersecty-function"></a>Fonction INTERSECTY

Renvoie la coordonnée *y* (dans le système de coordonnées locales) du point d'intersection de deux lignes. 
  
## <a name="syntax"></a>Syntaxe

INTERSECTX (* * *x1* * *, * * *Y1* * *, * * *angle1* * *, * * *x2* * *, * * *Y2* * *, * * *angle2* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _mâle_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée _x_d'un point sur la première ligne.  <br/> |
| _Y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée _y_d'un point sur la première ligne.  <br/> |
| _angle1_ <br/> |Obligatoire  <br/> |**Number** <br/> | Valeur de la cellule Angle de la première ligne.  <br/> |
| _ports_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée _x_d'un point sur la deuxième ligne.  <br/> |
| _Y2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée _y_d'un point sur la deuxième ligne.  <br/> |
| _angle2_ <br/> |Obligatoire  <br/> |**Number** <br/> |Valeur de la cellule Angle de la deuxième ligne.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Chaque ligne est définie par un point (*x,y*) et un angle. 
  
Microsoft Visio utilise cette fonction dans la cellule PinY d’une forme collée à un repère retourné. 
  
Si les lignes ne se coupent pas, la fonction renvoie une erreur Division par zéro (#DIV/0) que Visio ignore en restaurant la dernière valeur connue associée au point. 
  
## <a name="example"></a>Exemple

INTERSECTION (RepèreVert! PinX, RepèreVert! PinY, RepèreVert! Angle, RepèreHoriz! PinX, RepèreHoriz! PinY, RepèreHoriz! Angle 
  
Renvoie la coordonnée *y* du point d'intersection de RepèreVert et RepèreHoriz dans les unités de page. 
  

