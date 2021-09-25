---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c1e37da677fa38eb83a22db0c170eb6dd45cb8be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561760"
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

La **fonction FtAdcFt** est identique à **FtAddFt** lorsque  _pwCarry a la_ valeur NULL. Si _pwCarry n’a_ pas la valeur NULL et pointe sur 0, **FtAdcFt** renvoie la même valeur **FILETIME** que **ftAddFt.** 
  
## <a name="see-also"></a>Voir aussi



[FtAddFt](ftaddft.md)

