---
title: MODULUS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
ms.localizationpriority: medium
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Renvoie le reste (module) qui se traduit lorsqu’un nombre est divisé par un diviseur.
ms.openlocfilehash: 6d6d9893800aa8db0e882dd92d4adb0d05acb930
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623333"
---
# <a name="modulus-function"></a>Fonction MODULUS

Renvoie le reste (module) qui se traduit lorsqu’un nombre est divisé par un diviseur.
  
## <a name="syntax"></a>Syntaxe

MODULUS(** *number* **, ** *divisor* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Dividende  <br/> |
| _diviseur_ <br/> |Obligatoire  <br/> |**Number** <br/> |Diviseur  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

Le résultat a le même signe que le diviseur. Une erreur #DIV/0! est renvoyée si le diviseur est égal à 0. 
  
Dans la plupart des cas, il est préférable d’utiliser la fonction MODULUS plutôt que la fonction MOD. 
  
## <a name="example-1"></a>Exemple 1

MODULUS(5; 1,4)
  
Renvoie 0,8.
  
## <a name="example-2"></a>Exemple 2

MODULUS(5; -1,4)
  
Renvoie -0,6.
  
## <a name="example-3"></a>Exemple 3

MODULUS(-5; 1,4)
  
Renvoie 0,6.
  
## <a name="example-4"></a>Exemple 4

MODULUS(-5; -1,4)
  
Renvoie -0,8.
  

