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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e47f4e0d1ab9ab3ecfd53932b8ef26440134c603
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407241"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une structure [EntryID](entryid.md) et un nombre d'octets qui spécifie la taille de la structure **EntryID** . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>Members

 **cb**
  
> Nombre d'octets dans le membre **abEntry** . 
    
 **abEntry**
  
> Identificateur d'entrée complet qui inclut le tableau des indicateurs et des données binaires.
    
## <a name="remarks"></a>Remarques

Une structure **FLATENTRY** ressemble à une structure [EntryID](entryid.md) . Toutefois, il existe quelques différences: 
  
- Une structure **FLATENTRY** stocke la taille de l'identificateur d'entrée; **EntryID** ne fait pas. 
    
- Une structure **FLATENTRY** stocke les données d'indicateur avec le reste de l'identificateur d'entrée; **EntryID** les stocke séparément. 
    
- Une structure **FLATENTRY** est utilisée pour stocker un identificateur d'entrée dans un fichier ou le transmettre dans un flux d'octets, tandis qu'une structure **EntryID** est utilisée par les méthodes d'interface [IMAPIProp](imapipropiunknown.md) et par les méthodes **OpenEntry** suivantes: [IABLogon: : OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), IMAPISupport: [: OpenEntry](imapisupport-openentry.md), IMsgStore [::](imsgstore-openentry.md)OpenEntry, IMSLogon: [: OpenEntry](imslogon-openentry.md)
    
- Une structure **FLATENTRY** est utilisée pour stocker un identificateur d'entrée dans un fichier ou le transmettre dans un flux d'octets. Une structure **EntryID** est utilisée pour stocker un identificateur d'entrée sur le disque. 
    
## <a name="see-also"></a>Voir aussi



[ENTRYID](entryid.md)


[Structures MAPI](mapi-structures.md)

