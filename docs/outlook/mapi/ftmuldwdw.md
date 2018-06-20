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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783386"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**S’applique à**: Outlook 
  
Multiplie un entier non signé de 32 bits par une autre.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction **FtMulDwDw** renvoie une structure [FILETIME](filetime.md) qui contient le produit de deux entiers. Les deux paramètres d’entrée restent inchangées. 
  

