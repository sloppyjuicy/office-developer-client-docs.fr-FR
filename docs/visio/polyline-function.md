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
description: Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426295"
---
# <a name="polyline-function"></a>Fonction POLYLINE

Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie PolyLineTo. 
  
## <a name="syntax"></a>Syntaxe

POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les _données d’entrée x._ Si  _xType est_ 0, les  _données x_ d’entrée sont interprétées comme un pourcentage de width. Si  _xType est_ 1, les  _données x_ d’entrée sont interprétées comme une coordonnée locale.  <br/> |
| _yType_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les données _d’entrée y._ Si  _yType est_ 0, l’entrée  _y_-data est interprétée comme un pourcentage de height. Si  _yType est_ 1, l’entrée  _y_-data est interprétée comme une coordonnée locale.  <br/> |
| _x1_ <br/> |Obligatoire  <br/> |**Number** <br/> | Coordonnée _x._  <br/> |
| _y1_ <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée _y._  <br/> |
   
## <a name="remarks"></a>Remarques

Pour chaque argument  *x,*  il doit y avoir un argument  *y*  ; Sinon, une erreur est renvoyée. 
  
## <a name="example"></a>Exemple

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
Renvoie un rectangle de dimensions Largeur x Hauteur. 
  

