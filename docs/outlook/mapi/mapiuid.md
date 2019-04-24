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
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269922"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Version indépendante de l'ordre des octets d'une structure de [GUID](guid.md) utilisée pour identifier un fournisseur de services de manière unique. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macro connexe:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Members

 **opér**
  
> Tableau qui contient un identificateur de 16 octets.
    
## <a name="remarks"></a>Remarques

Une structure **MAPIUID** est une structure de **GUID** placée dans le processeur Intel ® Order Byte. 
  
MAPI crée des structures **MAPIUID** de manière à ce qu'il soit très rare que deux éléments aient le même identificateur. Les structures **MAPIUID** peuvent être stockées en tant que propriétés binaires ou en tant que fichiers, indépendamment de l'ordre des octets de l'ordinateur stockant les informations ou d'y accéder. 
  
 Les structures **MAPIUID** sont utilisées: 
  
- Pour identifier une section de profil.
    
- Dans les identificateurs d'entrée des objets de banque de messages et de carnet d'adresses pour identifier le fournisseur de services responsable.
    
- Dans la propriété **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) des messages.
    
Pour générer un identificateur **MAPIUID** pour une clé de recherche, les fournisseurs de services appellent [IMAPISupport:: NewUID](imapisupport-newuid.md).
  
Lorsqu'un client transmet un message via un réseau, il doit utiliser un protocole ou un format de transmission qui ne change pas l'ordre des données **MAPIUID** . 
  
Pour plus d'informations sur l'utilisation des structures **MAPIUID** , consultez les rubriques suivantes: 
  
[Inscription des identificateurs uniques des fournisseurs de services](registering-service-provider-unique-identifiers.md)
  
[Définition de l'ordre de transport](setting-transport-order.md)
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Structures MAPI](mapi-structures.md)

