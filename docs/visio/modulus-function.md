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
ms.openlocfilehash: f25de1ca0aeb4cdf9766d9bf08f33bf8de67fbbb
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62786128"
---
# <a name="modulus-function"></a>Fonction MODULUS

Renvoie le reste (module) qui se traduit lorsqu’un nombre est divisé par un diviseur.
  
## <a name="syntax"></a>Syntaxe

MODULUS(** *number* **, ** *divisor* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Requis  <br/> |**Number** <br/> |Dividende |
| _diviseur_ <br/> |Requis  <br/> |**Number** <br/> |Diviseur |
   
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
  

