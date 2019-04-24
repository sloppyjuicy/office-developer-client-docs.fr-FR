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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358113"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste d'attributs pour les propriétés d'un objet. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage. h  <br/> |
|Macros connexes:  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre d'attributs de propriété dans le membre **aPropAttr** . 
    
 **aPropAttr**
  
> Tableau d'attributs de propriété. Les valeurs valides pour les attributs sont les suivantes:
    
    - PROPATTR_MANDATORY
    
    - PROPATTR_READABLE
    
    - PROPATTR_WRITEABLE
    
    - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Remarques

La structure **SPropAttrArray** est utilisée par les objets de données de propriété qui implémentent l'interface [IPropData: IMAPIProp](ipropdataimapiprop.md) . Il est également utilisé par l'implémentation de MAPI de [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) basé sur le stockage structuré. 
  
## <a name="see-also"></a>Voir aussi



[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[Structures MAPI](mapi-structures.md)

