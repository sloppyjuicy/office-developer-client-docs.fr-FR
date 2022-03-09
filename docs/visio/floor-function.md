---
title: FLOOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
ms.localizationpriority: medium
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Arrondit un nombre à 0 (zéro), à l’integer suivant ou à l’instance suivante de plusieurs.
ms.openlocfilehash: dcbd3c50bf07e80784309904a8d8106ea1e09d80
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405629"
---
# <a name="floor-function"></a>Fonction FLOOR

Arrondit un nombre à 0 (zéro), à l’integer suivant ou à l’instance suivante de _plusieurs_.
  
## <a name="syntax"></a>Syntaxe

FLOOR(***number** _, _ *_multiple_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Number** <br/> |Nombre à arrondir. |
| _multiple_ <br/> |Requis  <br/> |**Number** <br/> |Multiple vers lequel arrondir. |

### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si le _multiple_ n’est pas précisé, le nombre est arrondi à l’entier le plus proche de 0.
  
 _Number_ et _multiple_ doivent tous deux avoir le même signe, sinon une erreur #NOMBRE! est renvoyée. Si _number_ ou _multiple_ ne peuvent être convertis en valeur, une erreur #VALEUR! est renvoyée. Si _number_ ou _multiple_ sont égaux à 0, le résultat est 0.
  
## <a name="example-1"></a>Exemple 1

FLOOR(3.7)
  
Renvoie 3.
  
## <a name="example-2"></a>Exemple 2

FLOOR(-3.7)
  
Renvoie -3.
  
## <a name="example-3"></a>Exemple 3

FLOOR(3.7, 0.5)
  
Renvoie 3,5.
  