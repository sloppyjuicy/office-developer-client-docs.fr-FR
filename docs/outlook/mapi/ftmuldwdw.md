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
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412911"
---
# <a name="ftmuldwdw"></a>FtMulDwDw

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Multiplie un nombre integer 32 bits non signé par un autre.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a>Parameters

 _Multiplicand_
  
> [in] Mot double qui contient l’integer 32 bits non signé  à multiplier par la valeur du paramètre Multiplicateur. 
    
 _Multiplicateur_
  
> [in] Mot double qui contient le multiplicateur d’nombres integer 32 bits non signé.
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction FtMulDwDw** renvoie une structure [FILETIME](filetime.md) qui contient le produit des deux nombres entières. Les deux paramètres d’entrée restent inchangés. 
  

