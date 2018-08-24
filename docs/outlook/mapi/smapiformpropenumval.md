---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578716"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Mappe une valeur entière énumérée à un nom d’affichage pour cette valeur. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a>Members

 **pszDisplayName**
  
> Chaîne qui contient le nom complet de la valeur spécifiée dans le membre **nVal** . 
    
 **nVal**
  
> Une valeur d’énumération pour le nom complet vers laquelle pointe le membre **pszDisplayName** . 
    
## <a name="remarks"></a>Remarques

Lorsqu’un utilisateur sélectionne un nom d’affichage d’un formulaire, la valeur d’énumération du nom correspondant est stocké à l’aide de l’implémentation d’interface [IMAPIProp](imapipropiunknown.md) qui est associée au formulaire. 
  
## <a name="see-also"></a>Voir aussi



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

