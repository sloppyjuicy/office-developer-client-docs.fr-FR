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
ms.openlocfilehash: 13dd6483b39af4aaf4d857cf332a32b12c3d331c
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779587"
---
# <a name="pow-function"></a>Fonction POW

Renvoie un nombre élevé à la puissance d’un exposant.
  
## <a name="syntax"></a>Syntaxe

POW(** *number* **, ** *exponent* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Number** <br/> |Nombre à élever à la puissance d’un exposant |
| _exposant_ <br/> |Requis  <br/> |**Number** <br/> |Exposant |
   
## <a name="remarks"></a>Remarques

Le  _nombre_ et  _l’exposant_ peuvent être des nombres non-nombres et être négatifs. Si  _le nombre_ n’est pas 0 et  _l’exposant_ est 0, cette fonction renvoie 1. Si  _le nombre_ est 0  _et que l’exposant_ est négatif, cette fonction renvoie 0,0. Si le _nombre et_   _l’exposant_ sont tous les deux 0, ou si le nombre est négatif et qu’il n’est pas un nombre d’exposants, cette fonction renvoie 0,0. Si le  _nombre et_  _l’exposant_ sont négatifs, cette fonction renvoie -1,#IND. 
  
## <a name="example"></a>Exemple

POW(5,2) 
  
Renvoie 25. 
  

