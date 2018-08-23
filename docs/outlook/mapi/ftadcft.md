---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f073dbb9655585ee56ab38be35bea4ef320042c0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569770"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ajoute un entier non signé de 64 bits à un autre, si vous le souhaitez à l’aide d’un indicateur de transport.
  
|||
|:-----|:-----|
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Paramètres

 _FT1_
  
> [in] Une structure [FILETIME](filetime.md) qui contient le premier entier non signé 64 bits à ajouter. 
    
 _ft2_
  
> [in] Une structure FILETIME qui contient le deuxième entier 64 bits non signé à ajouter.
    
 _pwCarry_
  
> [entrée, sortie, facultatif] À l’entrée, un pointeur vers entrantes exécuter indicateur. Dans la sortie, un pointeur vers le résultat de transport pour l’ajout. Ce paramètre peut être NULL si le résultat de transport n’est pas nécessaire.
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction **FtAdcFt** renvoie une structure **FILETIME** qui contient la somme de deux entiers. Les deux paramètres d’entrée restent inchangées. Si **pwCarry** n’est pas NULL, il contient le résultat de transport pour les fonctions sum, 0 ou 1. 
  
## <a name="remarks"></a>Remarques

La fonction **FtAdcFt** est identique à **FtAddFt** lorsque _pwCarry_ est NULL. Si _pwCarry_ n’est pas NULL et points à 0, **FtAdcFt** renvoie la même valeur **FILETIME** qui renvoie **FtAddFt** . 
  
## <a name="see-also"></a>Voir aussi



[FtAddFt](ftaddft.md)

