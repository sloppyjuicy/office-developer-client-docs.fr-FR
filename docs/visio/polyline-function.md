---
title: POLYLINE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie de PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348278"
---
# <a name="polyline-function"></a>Fonction POLYLINE

Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie de PolyLineTo. 
  
## <a name="syntax"></a>Syntaxe

PolyLINE (* * *xtype* * *, * * *yType* * *, * * *x1* * *, * * *Y1* * *...) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les données _x_ d'entrée. Si _xtype_ a la valeur 0, les données _x_d'entrée sont interprétées comme un pourcentage de la largeur. Si _xtype_ a la 1, les données _x_d'entrée sont interprétées comme une coordonnée locale.  <br/> |
| _yType_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les données de l'entrée _y_. Si _yType_ a la valeur 0, les données _y_entrées sont interprétées comme un pourcentage de la hauteur. Si _yType_ a la valeurs 1, les données _y_entrées sont interprétées comme une coordonnée locale.  <br/> |
| _mâle_ <br/> |Obligatoire  <br/> |**Number** <br/> | Coordonnée _x_.  <br/> |
| _Y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée _y_.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour chaque argument *x* , il doit y avoir un argument *y* ; Sinon, une erreur est renvoyée. 
  
## <a name="example"></a>Exemple

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Renvoie un rectangle de dimensions Largeur x Hauteur. 
  

