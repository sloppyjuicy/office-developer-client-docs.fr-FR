---
title: POLYLINE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
ms.localizationpriority: medium
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie PolyLineTo.
ms.openlocfilehash: 9d14021acd8e2a8086d44e7cf59a766ce41a6dcc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608087"
---
# <a name="polyline-function"></a>Fonction POLYLINE

Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie PolyLineTo. 
  
## <a name="syntax"></a>Syntaxe

POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les _données d’entrée x._ Si  _xType est_ 0, les  _données x_ d’entrée sont interprétées comme un pourcentage de la largeur. Si  _xType est_ 1, les  _données x_ d’entrée sont interprétées comme une coordonnée locale.  <br/> |
| _yType_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les données _d’entrée y._ Si  _yType est_ 0, l’entrée  _y_-data est interprétée comme un pourcentage de height. Si  _yType est_ 1, l’entrée  _y_-data est interprétée comme une coordonnée locale.  <br/> |
| _x1_ <br/> |Obligatoire  <br/> |**Number** <br/> | Coordonnée _x._  <br/> |
| _y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée _y._  <br/> |
   
## <a name="remarks"></a>Remarques

Pour chaque argument  *x,*  il doit y avoir un argument  *y*  ; Sinon, une erreur est renvoyée. 
  
## <a name="example"></a>Exemple

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Renvoie un rectangle de dimensions Largeur x Hauteur. 
  

