---
title: REPT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
ms.localizationpriority: medium
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Répète le texte un certain nombre de fois.
ms.openlocfilehash: 4a87253f655d04924cd73b3c290d6332c10333b3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374571"
---
# <a name="rept-function"></a>Fonction REPT

Répète le texte un certain nombre de fois.
  
## <a name="syntax"></a>Syntaxe

REPT (***text** _, _ *_number_times_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *text* <br/> |Obligatoire  <br/> |**String** <br/> | Texte à répéter. |
| *number_times* <br/> |Requis  <br/> |**Number** <br/> |Valeur positive spécifiant le nombre de fois que le texte doit être répété. |

## <a name="remarks"></a>Remarques

Si *number_times* :
  
- est zéro (0), REPT renvoie "" (texte vide) ;

- n’est pas un entier, il est tronqué.

## <a name="example"></a>Exemple

REPT (« \* », 5)
  
Renvoie \*\*\*\*\*.
  