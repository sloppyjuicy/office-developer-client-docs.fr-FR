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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327999"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Multiplie un entier non signé 64 bits par un entier non signé 32 bits.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a>Paramètres

 _Multiplicateur_
  
> dans Un double mot qui contient le multiplicateur de nombres entiers non signés 32 bits. 
    
 _Multiplicand_
  
> dans Une structure [fileTime](filetime.md) qui contient l'entier non signé 64 bits à multiplier par la valeur dans le paramètre _multiplicateur_ . 
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtMulDw** renvoie une structure **fileTime** qui contient le produit des deux entiers. Les deux paramètres d'entrée restent inchangés. 
  

