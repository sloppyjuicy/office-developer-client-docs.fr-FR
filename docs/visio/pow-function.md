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
ms.openlocfilehash: 5c829bb4ec236b251cc258fed6d2c862ede54980
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570329"
---
# <a name="pow-function"></a>Fonction POW

Renvoie un nombre élevé à la puissance d’un exposant.
  
## <a name="syntax"></a>Syntaxe

POW(** *number* **, ** *exponent* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à élever à la puissance d’un exposant  <br/> |
| _exposant_ <br/> |Obligatoire  <br/> |**Number** <br/> |Exposant  <br/> |
   
## <a name="remarks"></a>Remarques

Le  _nombre_ et  _l’exposant_ peuvent être des nombres non-nombres et être négatifs. Si  _le nombre_ n’est pas 0 et  _l’exposant_ est 0, cette fonction renvoie 1. Si  _le nombre_ est 0 et que  _l’exposant_ est négatif, cette fonction renvoie 0,0. Si le _nombre et_ l’exposant  sont tous  les deux 0, ou si le nombre est négatif et qu’il n’est pas un nombre d’exposants, cette fonction renvoie 0,0.  Si le  _nombre et_  _l’exposant_ sont négatifs, cette fonction renvoie -1,#IND. 
  
## <a name="example"></a>Exemple

POW(5,2) 
  
Renvoie 25. 
  

