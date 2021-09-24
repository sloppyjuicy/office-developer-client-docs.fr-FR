---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9ea204f2f1cf324b4276563005c2cd90ac53e0c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549909"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cartes une valeur d’un nom complet pour cette valeur. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Members

 **pszDisplayName**
  
> Chaîne qui contient le nom complet de la valeur spécifiée dans le membre **nVal.** 
    
 **nVal**
  
> Valeur d’éumération pour le nom complet pointé par le membre **pszDisplayName.** 
    
## <a name="remarks"></a>Remarques

Lorsqu’un utilisateur sélectionne un nom complet dans un formulaire, la valeur d’éumération correspondante du nom est stockée à l’aide de l’implémentation de l’interface [IMAPIProp](imapipropiunknown.md) associée au formulaire. 
  
## <a name="see-also"></a>Voir aussi



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

