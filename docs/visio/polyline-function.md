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
ms.openlocfilehash: 40d5953162c17de0b70752b188c1de0e2b01b712
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380059"
---
# <a name="polyline-function"></a>Fonction POLYLINE

Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie PolyLineTo. 
  
## <a name="syntax"></a>Syntaxe

POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les  _données d’entrée x_ . Si  _xType est_ 0, les  _données x_ d’entrée sont interprétées comme un pourcentage de width. Si  _xType est_ 1, les  _données x_ d’entrée sont interprétées comme une coordonnée locale. |
| _yType_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les données  _d’entrée y_. Si  _yType est_ 0, les données  _y_ d’entrée sont interprétées comme un pourcentage de height. Si  _yType est_ 1, les données  _y_ d’entrée sont interprétées comme une coordonnée locale. |
| _x1_ <br/> |Obligatoire  <br/> |**Number** <br/> | Coordonnée  _x_. |
| _y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée  _y_. |
   
## <a name="remarks"></a>Remarques

Pour chaque argument  *x* , il doit y avoir un argument  *y* ; Sinon, une erreur est renvoyée. 
  
## <a name="example"></a>Exemple

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Renvoie un rectangle de dimensions Largeur x Hauteur. 
  

