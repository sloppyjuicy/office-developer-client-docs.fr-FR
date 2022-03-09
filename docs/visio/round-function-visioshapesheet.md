---
title: ROUND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
ms.localizationpriority: medium
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Arrondit un nombre à la précision représentée par numberofdigits.
ms.openlocfilehash: 1d06e8018c562fda1d6191fc3c9a0f0ba2466a23
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372681"
---
# <a name="round-function-visioshapesheet"></a>ROUND Function (VisioShapeSheet)

Arrondit un nombre à la précision représentée par *numberofdigits*.
  
## <a name="syntax"></a>Syntaxe

ROUND(***number** _, _ *_numberofdigits_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *number* <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à arrondir |
| *numberofdigits* <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre de décimales de précision |

## <a name="remarks"></a>Remarques

Si *numberofdigits* est supérieur à 0, *number* est arrondi à x chiffres après la virgule, x correspondant à *numberofdigits*. Si *numberofdigits* est égal à 0, *number* est arrondi à un entier. Si *numberofdigits* est inférieur à 0, *number* est arrondi à x chiffres avant la virgule, x correspondant à *numberofdigits*.
  
## <a name="example-1"></a>Exemple 1

ROUND(123.654,2)
  
Renvoie 123,65.
  
## <a name="example-2"></a>Exemple 2

ROUND(123.654,0)
  
Renvoie 124.
  
## <a name="example-3"></a>Exemple 3

ROUND(123,654,-1)
  
Renvoie 120.
  