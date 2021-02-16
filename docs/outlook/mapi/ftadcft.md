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
  
Ajoute un integer 64 bits non signé à un autre, éventuellement à l’aide d’un indicateur de transport.
  
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

 _ft1_
  
> [in] Structure [FILETIME](filetime.md) qui contient le premier entière 64 bits non signé à ajouter. 
    
 _ft2_
  
> [in] Structure FILETIME qui contient le deuxième integer 64 bits non signé à ajouter.
    
 _pwCarry_
  
> [in, out, optional] Lors de l’entrée, un pointeur vers l’indicateur de transport entrant. En sortie, un pointeur vers le résultat de transport pour l’ajout. Ce paramètre peut être NULL si le résultat de transport n’est pas requis.
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction FtAdcFt** renvoie une structure **FILETIME** qui contient la somme des deux nombres entières. Les deux paramètres d’entrée restent inchangés. Si **pwCarry n’est** pas null, il contient le résultat de transport pour la somme, soit 0, soit 1. 
  
## <a name="remarks"></a>Remarques

La **fonction FtAdcFt** est identique à **FtAddFt** lorsque  _pwCarry a la valeur_ NULL. Si _pwCarry n’a_ pas la valeur NULL et pointe sur 0, **FtAdcFt** renvoie la même valeur **FILETIME** que **ftAddFt.** 
  
## <a name="see-also"></a>Voir aussi



[FtAddFt](ftaddft.md)

