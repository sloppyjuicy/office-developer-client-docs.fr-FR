---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: Contient une liste d’attributs pour les propriétés d’un objet. La structure SPropAttrArray est utilisée par les objets de données de propriété qui implémentent l’interface IPropData:IMAPIProp.
ms.openlocfilehash: 6453a70d02769962df806c1ca9d395becb3be7e0
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456258"
---
# <a name="spropattrarray"></a>SPropAttrArray

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste d’attributs pour les propriétés d’un objet. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Imessage.h  <br/> |
|Macros associées :  <br/> |[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Nombre d’attributs de propriété dans le **membre aPropAttr** . 
    
 **aPropAttr**
  
> Tableau d’attributs de propriété. Les valeurs valides pour les attributs sont les suivantes :

  - PROPATTR_MANDATORY
  - PROPATTR_READABLE
  - PROPATTR_WRITEABLE
  - PROPATTR_NOT_PRESENT
    
## <a name="remarks"></a>Remarques

La structure **SPropAttrArray** est utilisée par les objets de données de propriété qui implémentent l’interface [IPropData : IMAPIProp](ipropdataimapiprop.md) . Il est également utilisé par l’implémentation MAPI de [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) basé sur un stockage structuré. 
  
## <a name="see-also"></a>Voir aussi



[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[CbNewSPropAttrArray](cbnewspropattrarray.md)
  
[CbSPropAttrArray](cbspropattrarray.md)


[Structures MAPI](mapi-structures.md)

