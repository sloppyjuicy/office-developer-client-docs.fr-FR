---
title: MAPIUID
description: MAPIUID est une version indépendante de l’ordre des octets d’une structure GUID utilisée pour identifier de manière unique un fournisseur de services.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
ms.openlocfilehash: 49f51d213524a8bb361c2e5ec7ca69c4eac307f9
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828517"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Version indépendante d’un ordre d’octet d’une structure [GUID](guid.md) utilisée pour identifier de manière unique un fournisseur de services. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro associée :  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Members

 **Ab**
  
> Tableau qui contient un identificateur de 16 octets.
    
## <a name="remarks"></a>Remarques

Une structure **MAPIUID** est une structure **GUID** placée dans l’ordre des octets du processeur Intel®. 
  
MAPI crée des structures **MAPIUID** de manière à ce qu’il soit très rare que deux éléments différents aient le même identificateur. Les structures **MAPIUID** peuvent être stockées sous forme de propriétés binaires ou de fichiers, sans tenir compte de l’ordre des octets de l’ordinateur qui stocke ou accède aux informations. 
  
 Les structures **MAPIUID** sont utilisées : 
  
- Pour identifier une section de profil.
    
- Dans les identificateurs d’entrée des objets de magasin de messages et de carnet d’adresses pour identifier le fournisseur de services responsable.
    
- Dans la **propriété PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) des messages.
    
Pour générer un identificateur **MAPIUID** pour une clé de recherche, les fournisseurs de services appellent [IMAPISupport::NewUID](imapisupport-newuid.md).
  
Lorsqu’un client transmet un message sur un réseau, il doit utiliser un protocole ou un format de transmission qui ne modifie pas l’ordre des octets des données **MAPIUID** . 
  
Pour plus d’informations sur l’utilisation des structures **MAPIUID** , consultez les rubriques suivantes : 
  
[Inscription des identificateurs uniques du fournisseur de services](registering-service-provider-unique-identifiers.md)
  
[Définition de l’ordre de transport](setting-transport-order.md)
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Structures MAPI](mapi-structures.md)

