---
title: NURBS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
ms.localizationpriority: medium
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Renvoie une ligne B-spline rationnelle nonuniforme (NURBS). Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.
ms.openlocfilehash: daaa2d72473d16f94f823ba3d507161b6f14bc99
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62784908"
---
# <a name="nurbs-function"></a>Fonction NURBS

Renvoie une ligne B-spline rationnelle nonuniforme (NURBS). Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.
  
## <a name="syntax"></a>Syntaxe

NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Requis  <br/> |**chaîne** <br/> | Dernier nœud |
| _degré_ <br/> |Requis  <br/> |**Numérique** <br/> |Degré de la courbe Spline |
| _xType_ <br/> |Requis  <br/> |**Numérique** <br/> |Indique comment interpréter les  _données d’entrée x_ . Si  _xType est_ 0, toutes les  _données d’entrée x_ sont interprétées comme un pourcentage de width. Si  _xType est_ 1, toutes les  _données d’entrée x_ sont interprétées comme des coordonnées locales. |
| _yType_ <br/> |Requis  <br/> |**Numérique** <br/> |Indique comment interpréter les données d’entrée  _y_ . Si  _yType est_ 0, toutes les  _données_ d’entrée y sont interprétées comme un pourcentage de height. Si  _yType est_ 1, toutes les données d’entrée  _y_ sont interprétées comme des coordonnées locales. |
| _x1_ <br/> |Requis  <br/> |**String** <br/> |Coordonnée x. |
| _y1_ <br/> |Requis  <br/> |**String** <br/> |Coordonnée y. |
| _nœud1_ <br/> |Requis  <br/> |**String** <br/> |Nœud sur la courbe B-spline |
| _weight1_ <br/> |Requis  <br/> |**String** <br/> |Épaisseur sur la courbe B-spline |
   
## <a name="remarks"></a>Remarques

Pour chaque argument  *x*  , il doit y avoir un argument  *y*  ; Sinon, une erreur est renvoyée. 
  
Vous devez spécifier au moins *un argument* *x*, *y*, *nœud* et poids ; sinon, Visio renvoie une erreur. 
  

