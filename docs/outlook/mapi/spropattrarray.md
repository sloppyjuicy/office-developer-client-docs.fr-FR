---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a8f4e62a8eb1b5e61cb0223c66b921e15ab9423b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577680"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une liste d’attributs pour les propriétés d’un objet. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage.h  <br/> |
|Macros connexes :  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre d’attributs de propriété dans le membre **aPropAttr** . 
    
 **aPropAttr**
  
> Tableau d’attributs de propriété. Les valeurs valides pour les attributs sont les suivantes :
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Remarques

La structure **SPropAttrArray** est utilisée par les objets de données de propriété qui implémentent le [IPropData : IMAPIProp](ipropdataimapiprop.md) interface. Il est également utilisé par l’implémentation de MAPI de [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) qui est en fonction de stockage structuré. 
  
## <a name="see-also"></a>Voir aussi



[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[Structures MAPI](mapi-structures.md)

