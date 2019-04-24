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
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327978"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Multiplie un entier non signé 32 bits par un autre.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Paramètres

 _Multiplicand_
  
> dans Mot double qui contient l'entier non signé 32 bits à multiplier par la valeur dans le paramètre _multiplicateur_ . 
    
 _Multiplicateur_
  
> dans Un double mot qui contient le multiplicateur de nombres entiers non signés 32 bits.
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtMulDwDw** renvoie une structure [fileTime](filetime.md) qui contient le produit des deux entiers. Les deux paramètres d'entrée restent inchangés. 
  

