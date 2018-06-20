---
title: POW, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Renvoie un nombre élevé à la puissance d’un exposant.
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789347"
---
# <a name="pow-function"></a>POW, fonction

Renvoie un nombre élevé à la puissance d’un exposant.
  
## <a name="syntax"></a>Syntaxe

POW (** *numéro* **, ** *exposant* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à élever à la puissance d’un exposant  <br/> |
| _exposant_ <br/> |Obligatoire  <br/> |**Number** <br/> |Exposant  <br/> |
   
## <a name="remarks"></a>Remarques

_Nombre_ et _exposant_ peuvent être des nombres entiers non, et ils peuvent être négatives. Si _nombre_ n’est pas 0 et _exposant_ est 0, cette fonction renvoie la valeur 1. Si _nombre_ est 0 et _exposant_ est négatif, cette fonction renvoie 0,0. Si _nombre_ et _exposant_ sont égales à 0 ou si _nombre_ est négatif et _exposant_ n’est pas un entier, la fonction renvoie 0,0. Si _nombre_ et _exposant_ sont négatifs, la fonction renvoie -1. #IND. 
  
## <a name="example"></a>Exemple

POW(5;2) 
  
Renvoie 25. 
  

