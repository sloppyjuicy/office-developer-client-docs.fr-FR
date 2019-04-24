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
description: Renvoie une courbe B-spline rationnelle inuniforme (NURBS). Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340123"
---
# <a name="nurbs-function"></a>Fonction NURBS

Renvoie une courbe B-spline rationnelle inuniforme (NURBS). Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.
  
## <a name="syntax"></a>Syntaxe

NURBS (* * *knotLast* * *, * * *degree* * *, * ** xtype* * *, * * *yType* * *, * ** x1* * *, * * *Y1* * *, * * *knot1* * *, * * *Weight1* * *,...) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Obligatoire  <br/> |**chaîne** <br/> | Dernier nœud  <br/> |
| _degré_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Degré de la courbe Spline  <br/> |
| _xType_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Indique comment interpréter les données _x_ d'entrée. Si _xtype_ a la valeur 0, toutes les données d'entrée _x_ sont interprétées comme un pourcentage de la largeur. Si _xtype_ a la forme 1, toutes les données _x_ d'entrée sont interprétées comme des coordonnées locales.  <br/> |
| _yType_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Indique comment interpréter les données d'entrée _y_ . Si _yType_ a la valeur 0, toutes les données _y_ d'entrée sont interprétées comme un pourcentage de la hauteur. Si _yType_ a la valeurs 1, toutes les données _y_ d'entrée sont interprétées comme des coordonnées locales.  <br/> |
| _mâle_ <br/> |Obligatoire  <br/> |**String** <br/> |Coordonnée x.  <br/> |
| _Y1_ <br/> |Obligatoire  <br/> |**String** <br/> |Coordonnée y.  <br/> |
| _knot1_ <br/> |Obligatoire  <br/> |**String** <br/> |Nœud sur la courbe B-spline  <br/> |
| _Weight1_ <br/> |Obligatoire  <br/> |**String** <br/> |Épaisseur sur la courbe B-spline  <br/> |
   
## <a name="remarks"></a>Remarques

Pour chaque argument *x* , il doit y avoir un argument *y* ; Sinon, une erreur est renvoyée. 
  
Vous devez spécifier au moins un argument *x*, *y*, *nœud* et *poids* ; dans le cas contraire, Visio renvoie une erreur. 
  

