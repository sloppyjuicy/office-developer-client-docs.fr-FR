---
title: CEILING, fonction
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
ms.localizationpriority: medium
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Arrondit un nombre de 0 (zéro) à l’instance suivante de plusieurs. Si plusieurs n’est pas spécifié, le nombre est arrondi de 0 à l’integer suivant.
ms.openlocfilehash: 58ea588d06ba8842d122f694245150c42b680406
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405008"
---
# <a name="ceiling-function"></a>Fonction CEILING

Arrondit un nombre de 0 (zéro) à l’instance suivante de _plusieurs_. Si _plusieurs_ n’est pas spécifié, le nombre est arrondi de 0 à l’integer suivant.
  
## <a name="syntax"></a>Syntaxe

CEILING(***number** _, _ *_multiple_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Number** <br/> |Nombre à arrondir. |
| _multiple_ <br/> |Requis  <br/> |**Number** <br/> |Multiple à arrondir. |

## <a name="remarks"></a>Remarques

 _Number_ et _multiple_ doivent tous deux avoir le même signe, sinon une erreur #NOMBRE! est renvoyée. Si _number_ ou _multiple_ ne peuvent être convertis en valeur, une erreur #VALEUR! est renvoyée. Si _number_ ou _multiple_ sont égaux à 0, le résultat est 0.
  
## <a name="example-1"></a>Exemple 1

CEILING(3.7)
  
Renvoie 4
  
## <a name="example-2"></a>Exemple 2

CEILING(-3,7)
  
Renvoie -4
  
## <a name="example-3"></a>Exemple 3

CEILING(3.7, 0.25)
  
Renvoie 3,75
  