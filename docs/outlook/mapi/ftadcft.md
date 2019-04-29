---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429704"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un entier non signé 64 bits à un autre, éventuellement à l'aide d'un indicateur de transport.
  
|||
|:-----|:-----|
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a>Paramètres

 _FT1_
  
> dans Une structure [fileTime](filetime.md) qui contient le premier entier non signé 64 bits à ajouter. 
    
 _ft2_
  
> dans Une structure FILETIME qui contient le deuxième entier non signé 64 bits à ajouter.
    
 _pwCarry_
  
> [in, out, optional] En entrée, pointeur vers l'indicateur de transport entrant. En sortie, pointeur vers le résultat du transport pour l'addition. Ce paramètre peut être NULL si le résultat du transport n'est pas obligatoire.
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtAdcFt** renvoie une structure **fileTime** qui contient la somme des deux entiers. Les deux paramètres d'entrée restent inchangés. Si **pwCarry** est non null, il contient le résultat de transport pour la somme, 0 ou 1. 
  
## <a name="remarks"></a>Remarques

La fonction **FtAdcFt** est identique à **FtAddFt** lorsque _pwCarry_ est null. Si _pwCarry_ n'est pas null et pointe sur 0, **FtAdcFt** renvoie la même valeur **fileTime** que **FtAddFt** . 
  
## <a name="see-also"></a>Voir aussi



[FtAddFt](ftaddft.md)

