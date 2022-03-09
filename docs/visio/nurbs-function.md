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
ms.openlocfilehash: 426464da63ff6d28ccf7512676b2f7ddee351b59
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376993"
---
# <a name="nurbs-function"></a>Fonction NURBS

Renvoie une ligne B-spline rationnelle nonuniforme (NURBS). Cette fonction est utilisée dans la cellule E des lignes de géométrie NURBSTo.
  
## <a name="syntax"></a>Syntaxe

NURBS(***knotLast** _, _*_degree_*_, _*_xType_*_, _*_yType_*_, _*_x1_*_, _*_y1_*_, _*_nœud1_*_, _*_weight1_**, ...)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *knotLast* <br/> |Requis  <br/> |**chaîne** <br/> | Dernier nœud |
| *degré* <br/> |Obligatoire  <br/> |**Numérique** <br/> |Degré de la courbe Spline |
| *xType* <br/> |Obligatoire  <br/> |**Numérique** <br/> |Indique comment interpréter les  *données d’entrée x* . Si _xType_ a la valeur 0, toutes les données d’entrée _x_ sont interprétées comme un pourcentage de la cellule Width. Si _xType_ a la valeur 1, toutes les données d’entrée _x_ sont interprétées comme des coordonnées locales. |
| *yType* <br/> |Obligatoire  <br/> |**Numérique** <br/> |Indique comment interpréter les données d’entrée  *y* . Si _yType_ a la valeur 0, toutes les données d’entrée _y_ sont interprétées comme un pourcentage de la cellule Height. Si _yType_ a la valeur 1, toutes les données d’entrée _y_ sont interprétées comme des coordonnées locales. |
| *x1* <br/> |Obligatoire  <br/> |**String** <br/> |Coordonnée x. |
| *y1* <br/> |Requis  <br/> |**String** <br/> |Coordonnée y. |
| *nœud1* <br/> |Obligatoire  <br/> |**String** <br/> |Nœud sur la courbe B-spline |
| *weight1* <br/> |Requis  <br/> |**String** <br/> |Épaisseur sur la courbe B-spline |

## <a name="remarks"></a>Remarques

Pour chaque argument  *x* , il doit y avoir un argument  *y* ; Sinon, une erreur est renvoyée.
  
Vous devez spécifier au moins *un argument* *x*, *y*, *nœud* et poids ; sinon, Visio renvoie une erreur.
  