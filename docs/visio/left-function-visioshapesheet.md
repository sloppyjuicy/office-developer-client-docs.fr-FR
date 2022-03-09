---
title: LEFT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
ms.localizationpriority: medium
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Renvoie le ou les caractères les plus à gauche dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: 9fb898176ee27402196f184c9db5f266a5e3017f
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404557"
---
# <a name="left-function-visioshapesheet"></a>LEFT Function (VisioShapeSheet)

Renvoie le ou les caractères les plus à gauche dans une chaîne de texte, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

LEFT(***text** _, [, _ *_num_chars_opt_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *text* <br/> |Requis  <br/> |**String** <br/> |Chaîne de texte qui contient les caractères à extraire. |
| *num_chars_opt* <br/> |Facultatif  <br/> |**Numérique** <br/> |Nombre de caractères à extraire. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La valeur de *num_chars_opt* doit être supérieure ou égale à zéro (0).
  
Si *num_chars_opt* est supérieure à la longueur du texte, left renvoie tout le texte. Si *num_chars_opt* est omis, il est supposé être 1.
  
## <a name="example"></a>Exemple

LEFT ("Janvier 1 2004", 3)
  
Renvoie la valeur "Jan".
  