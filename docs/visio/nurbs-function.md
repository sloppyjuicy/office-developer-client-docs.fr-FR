---
title: NURBS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Renvoie une ligne B-spline rationnelle nonuniforme (NURBS). Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438455"
---
# <a name="nurbs-function"></a>Fonction NURBS

Renvoie une ligne B-spline rationnelle nonuniforme (NURBS). Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.
  
## <a name="syntax"></a>Syntaxe

NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Obligatoire  <br/> |**chaîne** <br/> | Dernier nœud  <br/> |
| _degré_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Degré de la courbe Spline  <br/> |
| _xType_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Indique comment interpréter les _données d’entrée x._ Si  _xType est_ 0, toutes les  _données d’entrée x_ sont interprétées comme un pourcentage de la largeur. Si  _xType est_ 1, toutes les  _données d’entrée x_ sont interprétées comme des coordonnées locales.  <br/> |
| _yType_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Indique comment interpréter les données _d’entrée y._ Si  _yType est_ 0, toutes les données d’entrée  _y_ sont interprétées comme un pourcentage de height. Si  _yType est_ 1, toutes les données d’entrée  _y_ sont interprétées comme des coordonnées locales.  <br/> |
| _x1_ <br/> |Obligatoire  <br/> |**String** <br/> |Coordonnée x.  <br/> |
| _y1_ <br/> |Obligatoire  <br/> |**String** <br/> |Coordonnée y.  <br/> |
| _nœud1_ <br/> |Obligatoire  <br/> |**String** <br/> |Nœud sur la courbe B-spline  <br/> |
| _weight1_ <br/> |Obligatoire  <br/> |**String** <br/> |Épaisseur sur la courbe B-spline  <br/> |
   
## <a name="remarks"></a>Remarques

Pour chaque argument  *x,*  il doit y avoir un argument  *y*  ; Sinon, une erreur est renvoyée. 
  
Vous devez spécifier au moins un *argument* *x*, *y*, *nœud* et poids ; sinon, Visio renvoie une erreur. 
  

