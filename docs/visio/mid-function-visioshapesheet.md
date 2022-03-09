---
title: MID Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
ms.localizationpriority: medium
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Renvoie un nombre spécifique de caractères à partir d’une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.
ms.openlocfilehash: e62d471b6126cdccd7b18f7a344773fa918305e7
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376755"
---
# <a name="mid-function-visioshapesheet"></a>MID Function (VisioShapeSheet)

Renvoie un nombre spécifique de caractères à partir d’une chaîne de texte, en commençant à la position que vous spécifiez, en fonction du nombre de caractères que vous spécifiez.
  
## <a name="syntax"></a>Syntaxe

MID (***text** _, _*_start_num_*_, _ *_num_chars_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *text* <br/> |Obligatoire  <br/> |**String** <br/> |Chaîne de texte qui contient les caractères à extraire. |
| *start_num* <br/> |Requis  <br/> |**Number** <br/> |Position du premier caractère à extraire. Le premier caractère de la chaîne de texte est à la position 1. |
| *num_chars* <br/> |Requis  <br/> |**Number** <br/> |Nombre de caractères à renvoyer. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Si  *start_num*  est :
  
- supérieur à la longueur de *text*, MID renvoie "" (texte vide) ;

- Inférieur à la longueur du *texte, mais*  *start_num plus*  *num_chars*  dépasse la longueur du *texte, MID* renvoie les caractères jusqu’à la fin du *texte*.

- inférieur à 1, MID renvoie la valeur d’erreur #VALEUR!.

Si  *num_chars*  est négatif, MID renvoie la valeur #VALUE! Autrement, la méthode INDEX renvoie la valeur d'erreur #REF!.
  
## <a name="example"></a>Exemple

MID ("SSN 999-99-9999";5;11)
  
Renvoie 999-99-9999.
  