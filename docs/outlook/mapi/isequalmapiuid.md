---
title: IsEqualMAPIUID
description: Décrit la syntaxe, les paramètres et les remarques pour IsEqualMAPIUID, qui teste deux structures MAPIUID pour déterminer si elles contiennent le même identificateur.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
ms.openlocfilehash: bdedcf64cb8d150783f11b362c88ada69d277089
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828212"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Teste deux structures [MAPIUID](mapiuid.md) pour déterminer si elles contiennent le même identificateur. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure associée :  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Paramètres

 _lpuid1_
  
> Pointeur vers la première structure **MAPIUID** à tester. 
    
 _lpuid2_
  
> Pointeur vers la deuxième structure **MAPIUID** à tester. 
    
## <a name="remarks"></a>Remarques

La macro **IsEqualMAPIUID** retourne TRUE si les deux structures **MAPIUID** contiennent le même identificateur et FALSE si ce n’est pas le cas. 
  
La macro **IsEqualMAPIUID** nécessite que le fichier d’en-tête Memory.h soit inclus. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)


[Macros liées aux structures](macros-related-to-structures.md)

