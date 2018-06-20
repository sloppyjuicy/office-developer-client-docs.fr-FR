---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2f5f4d50b085c437d1caab5f70dcb741afe090bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783315"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**S’applique à**: Outlook 
  
Une structure [ENTRYID](entryid.md) plus un nombre d’octets qui spécifie la taille de la structure de la **propriété ENTRYID** . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>Membres

 **cb**
  
> Nombre d’octets dans le membre **abEntry** . 
    
 **abEntry**
  
> L’identificateur d’entrée complet qui inclut le tableau des indicateurs et des données binaires.
    
## <a name="remarks"></a>Remarques

Une structure **FLATENTRY** ressemble à une structure [ENTRYID](entryid.md) . Toutefois, il existe quelques différences : 
  
- Une structure **FLATENTRY** stocke la taille de l’identificateur d’entrée. **Propriété ENTRYID** n’est pas. 
    
- Une structure **FLATENTRY** stocke les données d’indicateur avec le reste de l’identificateur d’entrée. **Propriété ENTRYID** les stocke séparément. 
    
- Structure **FLATENTRY** est utilisée pour stocker un identificateur d’entrée dans un fichier ou passez-la dans un flux d’octets, tandis que d’une structure **ENTRYID** est utilisée par les méthodes d’interface [IMAPIProp](imapipropiunknown.md) et par les méthodes **OpenEntry** suivantes : [IABLogon : : OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Une structure **FLATENTRY** sert à stocker un identificateur d’entrée dans un fichier ou passez-la dans un flux d’octets. Une structure **ENTRYID** est utilisée pour stocker un identificateur d’entrée sur le disque. 
    
## <a name="see-also"></a>Voir aussi



[PROPRIÉTÉ ENTRYID](entryid.md)


[Structures MAPI](mapi-structures.md)

