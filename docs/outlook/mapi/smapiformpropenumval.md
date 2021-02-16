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
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435410"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété m’indique si une valeur d’un nom complet est un nom complet. 
  
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

