---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c823a4e3d08d9082a3b5ac5c4bd8169612caa16e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583994"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Multiplie un nombre entier non signé 64 bits en entier non signé 32 bits.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Paramètres

 _Multiplicateur_
  
> [in] Un mot double contenant le multiplicateur de nombre entier non signé 32 bits. 
    
 _Multiplicand_
  
> [in] Une structure [FILETIME](filetime.md) qui contient l’entier non signé de 64 bits à multipliées par la valeur dans le paramètre _Multiplicateur_ . 
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction **FtMulDw** renvoie une structure **FILETIME** qui contient le produit de deux entiers. Les deux paramètres d’entrée restent inchangées. 
  

