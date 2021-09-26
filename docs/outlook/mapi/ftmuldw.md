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
ms.openlocfilehash: 430eff9b19f4052a77d3792ceb4f9b3412ee79ed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630851"
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
  
> [in] Structure [FILETIME](filetime.md) qui contient l’integer 64 bits non signé à multiplier par la valeur du paramètre Multiplicateur.  
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction FtMulDw** renvoie une structure **FILETIME** qui contient le produit des deux nombres entières. Les deux paramètres d’entrée restent inchangés. 
  

