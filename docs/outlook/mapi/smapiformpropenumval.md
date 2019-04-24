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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309491"
---
# <a name="smapiformpropenumval"></a>SMAPIFormPropEnumVal

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Mappe une valeur entière énumérée à un nom complet pour cette valeur. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
   
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
  
> Valeur d'énumération pour le nom complet désigné par le membre **pszDisplayName** . 
    
## <a name="remarks"></a>Remarques

Lorsqu'un utilisateur sélectionne un nom d'affichage dans un formulaire, la valeur d'énumération correspondante du nom est stockée à l'aide de l'implémentation de l'interface [IMAPIProp](imapipropiunknown.md) associée au formulaire. 
  
## <a name="see-also"></a>Voir aussi



[SMAPIFormProp](smapiformprop.md)
  
[SPropValue](spropvalue.md)


[Structures MAPI](mapi-structures.md)

