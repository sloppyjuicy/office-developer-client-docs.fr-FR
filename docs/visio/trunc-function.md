---
title: TRUNC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
ms.localizationpriority: medium
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Renvoie un nombre tronqué au nombre de chiffres spécifié.
ms.openlocfilehash: 41e28aaddf25311fc07a5766fc92a5309c73bf01
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375768"
---
# <a name="trunc-function"></a>Fonction TRUNC

Renvoie un nombre tronqué au nombre de chiffres spécifié.
  
## <a name="syntax"></a>Syntaxe

TRUNC(***number** _, _ *_numberofdigits_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *number* <br/> |Obligatoire  <br/> |**Numérique** <br/> |Nombre à tronquer. |
| *numberofdigits* <br/> |Obligatoire  <br/> |**Numérique** <br/> |Nombre de chiffres à *tronqué.* |

### <a name="return-value"></a>Valeur renvoyée

Numérique.
  
## <a name="remarks"></a>Remarques

Si  *numberofdigits* est supérieur à *0, le* nombre est tronqué en _nombreofdigits_ à droite de la décimale. Si la valeur _numberofdigits_ est 0, _number_ est arrondi à l’entier. Si la valeur _numberofdigits_ est inférieure à 0,  _number_ est arrondi au _numberofdigits_ indiqué à gauche du séparateur décimal.
  
## <a name="example-1"></a>Exemple 1

TRUNC(123.654,2)
  
Renvoie 123,65.
  
## <a name="example-2"></a>Exemple 2

TRUNC(123.654,0)
  
Renvoie 123.
  
## <a name="example-3"></a>Exemple 3

TRUNC(123.654,-1)
  
Renvoie 120.
  