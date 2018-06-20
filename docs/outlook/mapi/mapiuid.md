---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3675c6a8ee2ee208f175dd5f7d219447aa52e9ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784786"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**S’applique à**: Outlook 
  
Une version indépendante de l’ordre des octets d’une structure [GUID](guid.md) qui sert à identifier de manière unique un fournisseur de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro connexe :  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Membres

 **Carnet d’adresses**
  
> Tableau qui contient un identificateur de 16 octets.
    
## <a name="remarks"></a>Remarques

Une structure **MAPIUID** est une structure **GUID** placer dans l’ordre d’octet Intel® processeur. 
  
MAPI crée des structures **MAPIUID** d’une manière qui rend très rare ont le même identificateur de deux éléments différents. Structures **MAPIUID** peuvent être stockées en tant que propriétés binaires ou en tant que fichiers, quel que soit l’ordre d’octets de l’ordinateur de stockage ou d’accéder aux informations. 
  
 Structures **MAPIUID** sont utilisés : 
  
- Pour identifier une section de profil.
    
- Dans les identificateurs d’entrée du message stocker et résoudre les objets book pour identifier le fournisseur de services responsables.
    
- Dans la propriété **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) des messages.
    
Pour générer un identificateur **MAPIUID** une clé de recherche, les fournisseurs de services d’appel [IMAPISupport::NewUID](imapisupport-newuid.md).
  
Lorsqu’un client transmet un message sur un réseau, il doit utiliser un format de protocole ou de transmission qui ne modifie pas l’ordre d’octets de données **MAPIUID** . 
  
Pour plus d’informations sur l’utilisation des structures **MAPIUID** , consultez les rubriques suivantes : 
  
[Inscription des identificateurs uniques de fournisseur de Service](registering-service-provider-unique-identifiers.md)
  
[Ordre de Transport de paramètre](setting-transport-order.md)
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Structures MAPI](mapi-structures.md)

