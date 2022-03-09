---
title: SETF, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
ms.localizationpriority: medium
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Définit la formule d’une cellule.
ms.openlocfilehash: 06e5e9c51a1ca96e22834881e4f09e76df0be17e
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404642"
---
# <a name="setf-function"></a>Fonction SETF

Définit la formule d’une cellule.
  
## <a name="syntax"></a>Syntaxe

SETF( GETREF(***cell** _ ), _ *_formula_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *cell* <br/> |Requis  <br/> |**String** <br/> |Cellule dont la formule doit être définie. |
| *formula* <br/> |Requis  <br/> |**String** <br/> |Formule à utiliser |

## <a name="remarks"></a>Remarques

À l’évaluation, le résultat de l’expression dans *formula* devient la nouvelle formule dans l’argument *cell*. Si la *formula* est entourée de guillemets, l’expression ainsi citée s’inscrit dans *cell*. Pour que l’argument _cell_ soit interprété comme une chaîne de caractères, entourez l’argument _formula_ de trois paires de guillemets.
  
La cellule cible doit être définie à l’aide d’une référence GETREF() ou sous forme de chaîne pour éviter la circularité. Il est préférable d’utiliser GETREF, car Microsoft Visio peut ajuster les références lorsque la forme est déplacée vers un autre document.
  
Si l’argument *cell* n’est pas défini à l’aide de GETREF ou sous forme de chaîne, la fonction renvoie une erreur. Aucune formule n’est alors modifiée. Si l’argument *formula* contient une erreur de syntaxe, la fonction renvoie une erreur et la formule dans la *cell* n’est pas modifiée.
  
## <a name="example-1"></a>Exemple 1

SETF( GETREF(Scratch.A1), 1,5 en \* 6 + 1 pi)
  
Cette commande donne à la formule Scratch.A1 une valeur de 533,4 millimètres.
  
## <a name="example-2"></a>Exemple 2

SETF( GETREF(Scratch.A1), « 1,5 en \* 6 + 1 m »)
  
Définit la formule de Scratch. A1 à l’expression 1,5 in6\*+1 m.
  
## <a name="example-3"></a>Exemple 3

SETF(GETREF(Scratch.A1), """Dites """"ahh""""""")
  
Donne pour valeur à la cellule Scratch.A1 la chaîne "Dites ""ahh""" ce qui revient à Dites "ahh".
  