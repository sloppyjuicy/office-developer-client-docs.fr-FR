---
title: FtAdcFt
description: Décrit FtAdcFt et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
ms.openlocfilehash: bf1d4ec65135cb60484cb31946c97a5c455fc602
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817521"
---
# <a name="ftadcft"></a>FtAdcFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un entier 64 bits non signé à un autre, éventuellement à l’aide d’un indicateur de transport.
  
|Propriété|Valeur|
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

 _Ft1_
  
> [in] Structure [FILETIME](filetime.md) qui contient le premier entier 64 bits non signé à ajouter. 
    
 _ft2_
  
> [in] Structure FILETIME qui contient le deuxième entier 64 bits non signé à ajouter.
    
 _pwCarry_
  
> [in, out, optional] Lors de l’entrée, pointeur vers l’indicateur de transport entrant. En sortie, pointeur vers le résultat de transport pour l’addition. Ce paramètre peut être NULL si le résultat de carry n’est pas requis.
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtAdcFt** retourne une structure **FILETIME** qui contient la somme des deux entiers. Les deux paramètres d’entrée restent inchangés. Si **pwCarry** n’est pas NULL, il contient le résultat carry pour la somme, 0 ou 1. 
  
## <a name="remarks"></a>Remarques

La fonction **FtAdcFt** est identique à **FtAddFt** lorsque  _pwCarry_ a la valeur NULL. Si  _pwCarry_ n’a pas la valeur NULL et pointe vers 0, **FtAdcFt** retourne la même valeur **FILETIME** que celle retournée par **FtAddFt** . 
  
## <a name="see-also"></a>Voir aussi



[FtAddFt](ftaddft.md)

