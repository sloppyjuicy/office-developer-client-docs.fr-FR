---
title: MAPIUID
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 74205b0d6016f50d395c95e202858f33d6d83781
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725270"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Version indépendante d’un ordre d’byte d’une structure [GUID](guid.md) utilisée pour identifier de manière unique un fournisseur de services. 
  
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

 **ab**
  
> Tableau qui contient un identificateur de 16 byte.
    
## <a name="remarks"></a>Remarques

Une structure **MAPIUID** est une structure **GUID** mise dans l’ordre d’byte du processeur Intel®. 
  
MAPI crée des structures **MAPIUID** de manière à ce qu’il soit très rare que deux éléments différents ont le même identificateur. Les structures **MAPIUID** peuvent être stockées en tant que propriétés binaires ou en tant que fichiers, sans prendre en compte l’ordre d’byte de l’ordinateur stockant ou accédant aux informations. 
  
 **Les structures MAPIUID** sont utilisées : 
  
- Pour identifier une section de profil.
    
- Dans les identificateurs d’entrée des objets de magasin de messages et de carnet d’adresses pour identifier le fournisseur de services responsable.
    
- Dans la **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) des messages.
    
Pour générer un **identificateur MAPIUID** pour une clé de recherche, les fournisseurs de services appellent [IMAPISupport::NewUID](imapisupport-newuid.md).
  
Lorsqu’un client transmet un message sur un réseau, il doit utiliser un format de protocole ou de transmission qui ne modifie pas l’ordre d’byte des données **MAPIUID** . 
  
Pour plus d’informations sur l’utilisation des structures **MAPIUID** , consultez les rubriques suivantes : 
  
[Inscription des identificateurs uniques du fournisseur de services](registering-service-provider-unique-identifiers.md)
  
[Définition de l’ordre de transport](setting-transport-order.md)
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Structures MAPI](mapi-structures.md)

