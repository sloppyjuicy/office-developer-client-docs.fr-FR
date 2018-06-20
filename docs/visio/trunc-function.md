---
title: TRUNC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Renvoie un nombre tronqué dans le nombre de chiffres spécifié.
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789934"
---
# <a name="trunc-function"></a>TRUNC, fonction

Renvoie un nombre tronqué dans le nombre de chiffres spécifié.
  
## <a name="syntax"></a>Syntaxe

TRUNC (** *numéro* **, ** *nombredechiffres* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Nombre à tronquer.  <br/> |
| _nombredechiffres_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Le nombre de chiffres auquel vous voulez tronquer _nombre_.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Numérique
  
## <a name="remarks"></a>Remarques

Si le _nombredechiffres_ est supérieur à 0, _nombre_ est arrondi au _nombredechiffres_ à droite du séparateur décimal. Si le _nombredechiffres_ est 0, _nombre_ est arrondi à un entier. Si le _nombredechiffres_ est inférieur à 0, _nombre_ est arrondi au _nombredechiffres_ à gauche du séparateur décimal. 
  
## <a name="example-1"></a>Exemple 1

TRUNC(123.654,2)
  
Renvoie 123,65.
  
## <a name="example-2"></a>Exemple 2

TRUNC(123.654,0)
  
Renvoie 123.
  
## <a name="example-3"></a>Exemple 3

TRUNC(123.654,-1)
  
Renvoie 120.
  

