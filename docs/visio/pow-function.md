---
title: POW, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
ms.localizationpriority: medium
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Renvoie un nombre élevé à la puissance d’un exposant.
ms.openlocfilehash: c5576185a792c0da00c8afcec0311b0b67ac9655
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405906"
---
# <a name="pow-function"></a>Fonction POW

Renvoie un nombre élevé à la puissance d’un exposant.
  
## <a name="syntax"></a>Syntaxe

POW(***number** _, _*_exponent_**)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *number* <br/> |Requis  <br/> |**Number** <br/> |Nombre à élever à la puissance d’un exposant |
| *exposant* <br/> |Requis  <br/> |**Number** <br/> |Exposant |

## <a name="remarks"></a>Remarques

Le  *nombre* et  *l’exposant* peuvent être des nombres non-nombres et être négatifs. Si _number_ est différent de 0 et que _exponent_ est égal à 0, cette fonction renvoie 1. Si _number_ est égal à 0 et que _exponent_ est négatif, la fonction renvoie 0,0. Si _number_ et _exponent_ sont tous les deux égaux à 0 ou si _number_ est négatif et _exponent_ non entier, la fonction renvoie 0,0. Si le _nombre et_ _l’exposant_ sont négatifs, cette fonction renvoie -1,#IND.
  
## <a name="example"></a>Exemple

POW(5,2)
  
Renvoie 25.
  