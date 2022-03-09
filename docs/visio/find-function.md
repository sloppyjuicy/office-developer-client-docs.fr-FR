---
title: FIND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
ms.localizationpriority: medium
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte que vous recherchez par rapport à sa position dans la chaîne de texte qui la contient.
ms.openlocfilehash: ea626b3ca43d8d93808addc31d98550ccbf17dae
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405190"
---
# <a name="find-function"></a>Fonction FIND

Recherche une chaîne de texte contenue dans une autre chaîne de texte et renvoie la position de départ de la chaîne de texte que vous recherchez par rapport à sa position dans la chaîne de texte qui la contient.
  
## <a name="syntax"></a>Syntaxe

FIND (***find_text** _, _*_within_text_*_,[ _*_start_num_*_ ], [ _ *_ignore_case_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *find_text* <br/> |Requis  <br/> |**String** <br/> |Chaîne de texte à rechercher. |
| *format* <br/> |Requis  <br/> |**String** <br/> |Chaîne de texte qui contient le texte à rechercher. |
| *start_num* <br/> |Facultatif  <br/> |**Number** <br/> |Caractère auquel débute la recherche. Le premier caractère de *within_text* est 1. Si *start_num* n’est pas spécifié, la valeur 1 est utilisée par défaut. |
| *ignore_case* <br/> |Facultatif  <br/> |**Boolean** <br/> |Par défaut, la fonction FIND respecte la casse. Si vous souhaitez qu’elle ignore la casse, attribuez à cet argument la valeur TRUE. |

### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Si la fonction FIND détecte plusieurs correspondances, elle renvoie la position de début de la première chaîne. L *find_text* argument ne considère pas les caractères comme des caractères génériques.
  
Si *find_text* :
  
- est vide (""), FIND recherche le première caractère de la chaîne recherchée (c’est-à-dire, le caractère dont le numéro est *start_num* ou 1) ;
- n’apparaît pas dans *within_text*, FIND renvoie la valeur d’erreur #VALEUR!.

Si *start_num* :
  
- n’est pas supérieur à zéro (0), FIND renvoie la valeur d’erreur #VALEUR! ;
- est supérieur à la longueur de *within_text*, FIND renvoie la valeur d’erreur #VALEUR!.

## <a name="example"></a>Exemple

FIND ("2003";"20 janvier 2003")
  
Renvoie 12.
  