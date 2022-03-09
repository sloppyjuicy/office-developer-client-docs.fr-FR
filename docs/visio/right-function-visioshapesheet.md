---
title: RIGHT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
ms.localizationpriority: medium
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Renvoie le ou les derniers caractères d’une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: 63dd0467f6cc5f14cc478c4fa2c45f7dc53ffb8c
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404593"
---
# <a name="right-function-visioshapesheet"></a>RIGHT Function (VisioShapeSheet)

Renvoie le ou les derniers caractères d’une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

RIGHT(***text** _ [, _ *_num_chars_opt_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *text* <br/> |Requis  <br/> |**String** <br/> | Chaîne de texte contenant les caractères à extraire. |
| *num_chars_opt* <br/> |Facultatif  <br/> |**Number** <br/> |Nombre de caractères à extraire. La valeur par défaut est 1. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur de *num_chars_opt* doit être supérieure ou égale à zéro (0).
  
Si *num_chars_opt* est supérieure à la longueur du texte, right renvoie tout le texte. Si _num_chars_opt_ est omis, il est supposé être 1.
  
## <a name="example"></a>Exemple

RIGHT ("Janvier 1; 2004"; 4)
  
Renvoie la valeur 2004.
  