---
title: FLATENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FLATENTRY
api_type:
- COM
ms.assetid: 03e53e08-9113-4101-84c9-ccf6d43127f6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 38b8d06b39ddab2e7c287ee913b24cda26811e26
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604970"
---
# <a name="flatentry"></a>FLATENTRY

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Structure [ENTRYID](entryid.md) plus un nombre d’byte qui spécifie la taille de la structure **ENTRYID.** 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[cbFLATENTRY](cbflatentry.md), [CbNewFLATENTRY](cbnewflatentry.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} FLATENTRY, FAR *LPFLATENTRY;

```

## <a name="members"></a>Members

 **cb**
  
> Nombre d’octets dans le **membre abEntry.** 
    
 **abEntry**
  
> Identificateur d’entrée complet qui inclut le tableau d’indicateurs et de données binaires.
    
## <a name="remarks"></a>Remarques

Une **structure FLATENTRY** ressemble à une structure [ENTRYID.](entryid.md) Toutefois, il existe certaines différences : 
  
- Une structure **FLATENTRY** stocke la taille de l’identificateur d’entrée ; **ENTRYID ne** le fait pas. 
    
- Une structure **FLATENTRY** stocke les données d’indicateur avec le reste de l’identificateur d’entrée ; **ENTRYID les** stocke séparément. 
    
- Une structure **FLATENTRY** permet de stocker un identificateur d’entrée dans un fichier ou de le transmettre dans un flux d’octets, tandis qu’une structure **ENTRYID** est utilisée par les méthodes d’interface [IMAPIProp](imapipropiunknown.md) et par les méthodes **OpenEntry** suivantes : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Une structure **FLATENTRY** permet de stocker un identificateur d’entrée dans un fichier ou de le transmettre dans un flux d’octets. Une structure **ENTRYID** est utilisée pour stocker un identificateur d’entrée sur le disque. 
    
## <a name="see-also"></a>Voir aussi



[ENTRYID](entryid.md)


[Structures MAPI](mapi-structures.md)

