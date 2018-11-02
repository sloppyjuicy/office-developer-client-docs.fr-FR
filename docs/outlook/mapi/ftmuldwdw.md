---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8002698b1644fb63292b4242d4fb3d784a99a03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592023"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Multiplie un entier non signé de 32 bits par une autre.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Paramètres

 _Multiplicand_
  
> [in] Un mot double contenant le nombre entier non signé 32 bits à multipliées par la valeur dans le paramètre _Multiplicateur_ . 
    
 _Multiplicateur_
  
> [in] Un mot double contenant le multiplicateur de nombre entier non signé 32 bits.
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtMulDwDw** renvoie une structure [FILETIME](filetime.md) qui contient le produit de deux entiers. Les deux paramètres d’entrée restent inchangées. 
  

