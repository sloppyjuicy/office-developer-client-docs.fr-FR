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
description: Cartes valeur d’un nom complet pour cette valeur pour les Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 97a2e45f639ebb26bb59e5efa299f6b0d88c85a6
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455509"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cartes valeur d’un nom complet pour cette valeur. 
  
|Propriété |Valeur |
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
  
> Chaîne qui contient le nom complet de la valeur spécifiée dans le membre **nVal** . 
    
 **nVal**
  
> Valeur d’éumération pour le nom complet pointé par le membre **pszDisplayName** . 
    
## <a name="remarks"></a>Remarques

Lorsqu’un utilisateur sélectionne un nom complet dans un formulaire, la valeur d’éumération correspondante du nom est stockée à l’aide de l’implémentation de l’interface [IMAPIProp](imapipropiunknown.md) associée au formulaire. 
  
## <a name="see-also"></a>Voir aussi



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

