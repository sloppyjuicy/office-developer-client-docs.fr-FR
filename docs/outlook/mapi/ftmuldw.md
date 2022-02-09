---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 363c00e8ab2b706d9fd55573abffcc8c04713f2c
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462065"
---
# <a name="ftmuldw"></a>FtMulDw

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Multiplie un nombre integer 64 bits non signé par un nombre integer 32 bits non signé.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Mot double qui contient le multiplicateur d’nombres integer 32 bits non signé. 
    
 _Multiplicand_
  
> [in] Structure [FILETIME](filetime.md) qui contient l’ensemble non signé 64 bits à multiplier par la valeur dans le paramètre Multiplicateur. 
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction FtMulDw** renvoie une structure **FILETIME** qui contient le produit des deux nombres entières. Les deux paramètres d’entrée restent inchangés. 
  

