---
title: MODULUS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Renvoie le reste (module) qui se produit lorsqu’un nombre est divisé par un diviseur.
ms.openlocfilehash: 4e2ef7acf9dc04e788cb2b8a0ff737f12a79c61a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789153"
---
# <a name="modulus-function"></a>MODULUS, fonction

Renvoie le reste (module) qui se produit lorsqu’un nombre est divisé par un diviseur.
  
## <a name="syntax"></a>Syntaxe

MODULE (** *numéro* **, ** *diviseur* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Dividende  <br/> |
| _diviseur_ <br/> |Obligatoire  <br/> |**Number** <br/> |Diviseur  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Note

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
  

