---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426932"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Teste deux structures [MAPIUID](mapiuid.md) pour déterminer si elles contiennent le même identificateur. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Paramètres

 _lpuid1_
  
> Pointeur vers la première structure **MAPIUID** à tester. 
    
 _lpuid2_
  
> Pointeur vers la deuxième structure **MAPIUID** à tester. 
    
## <a name="remarks"></a>Remarques

La macro **IsEqualMAPIUID** renvoie true si les deux structures **MAPIUID** contiennent le même identificateur et FALSE si ce n’est pas le cas. 
  
La macro **IsEqualMAPIUID nécessite** que le fichier d’en-tête Memory.h soit inclus. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)


[Macros liées aux structures](macros-related-to-structures.md)

