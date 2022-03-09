---
title: POLYLINE, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
ms.localizationpriority: medium
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie PolyLineTo.
ms.openlocfilehash: 2fba0daef24db71a20dafb22fe0da018ed585c92
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405643"
---
# <a name="polyline-function"></a>Fonction POLYLINE

Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie PolyLineTo.
  
## <a name="syntax"></a>Syntaxe

POLYLINE(***xType** _, _*_yType_*_, _*_x1_*_, _*_y1_**...)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *xType* <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les données d’entrée *x*. Si *xType* a la valeur 0, les données *x* entrées sont interprétées comme un pourcentage de la cellule Width. Si *xType* a la valeur 1, les données *x* entrées sont interprétées comme une coordonnée locale. |
| *yType* <br/> |Obligatoire  <br/> |**Booléen** <br/> |Indique comment interpréter les données d’entrée *y*. Si *yType* a la valeur 0, les données *y* entrées sont interprétées comme un pourcentage de la cellule Height. Si *yType* a la valeur 1, les données *y* entrées sont interprétées comme une coordonnée locale. |
| *x1* <br/> |Obligatoire  <br/> |**Number** <br/> | Coordonnée *x*. |
| *y1* <br/> |Obligatoire  <br/> |**Number** <br/> |Coordonnée *y*. |

## <a name="remarks"></a>Remarques

Pour chaque argument  *x* , il doit y avoir un argument  *y* ; Sinon, une erreur est renvoyée.
  
## <a name="example"></a>Exemple

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)
  
Renvoie un rectangle de dimensions Largeur x Hauteur.
  