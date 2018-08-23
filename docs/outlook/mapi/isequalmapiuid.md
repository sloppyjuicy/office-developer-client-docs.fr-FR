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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566662"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Teste deux structures [MAPIUID](mapiuid.md) pour déterminer s’ils contiennent le même identificateur. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Paramètres

 _lpuid1_
  
> Pointeur vers la structure **MAPIUID** premier à tester. 
    
 _lpuid2_
  
> Pointeur vers la structure **MAPIUID** deuxième à tester. 
    
## <a name="remarks"></a>Remarques

La macro **IsEqualMAPIUID** renvoie la valeur TRUE si les deux structures **MAPIUID** contiennent les mêmes identificateur et FALSE si elles n’est pas. 
  
La macro **IsEqualMAPIUID** exige que le fichier d’en-tête Memory.h être inclus. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)


[Macros liées aux structures](macros-related-to-structures.md)

