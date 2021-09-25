---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d12795d083053460dc61a2f7e36df3802120665d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579858"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Désigne un service de message comme fournisseur de l’identité principale du profil.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> [in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique du service de message pour fournir l’identité principale, ou NULL, qui indique que **SetPrimaryIdentity** doit effacer l’identité actuelle. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le service de message a été correctement affecté au fournisseur de l’identité principale.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** a tenté de désigner un service de message dont l’indicateur SERVICE_NO_PRIMARY_IDENTITY est PR_RESOURCE_FLAGS **(** [PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
## <a name="remarks"></a>Remarques

La **méthode IMsgServiceAdmin::SetPrimaryIdentity** établit un service de message en tant que fournisseur de l’identité principale du profil. L’identité principale est généralement l’utilisateur qui est connecté au service de message. Il est représenté par trois propriétés : 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Chaque fournisseur de services dans le service de messagerie désigné définit ces trois propriétés sur le nom complet, l’identificateur d’entrée et la clé de recherche de l’utilisateur de messagerie qui fournit l’identité principale. Les clients peuvent récupérer l’identificateur d’entrée de l’identité principale en appelant la méthode [IMAPISession::QueryIdentity.](imapisession-queryidentity.md) 
  
La **propriété PR_RESOURCE_FLAGS** est définie sur STATUS_PRIMARY_IDENTITY pour chaque fournisseur membre du service de messagerie qui fournit l’identité principale et sur SERVICE_PRIMARY_IDENTITY pour le service de messagerie. Lorsqu’un fournisseur de services ne peut pas fournir l’identité principale de son service de messagerie, il PR_RESOURCE_FLAGS **à** STATUS_NO_PRIMARY_IDENTITY. **SetPrimaryIdentity** définit la **propriété PR_RESOURCE_FLAGS** de chaque service de message qui ne fournit pas l’identité principale à SERVICE_NO_PRIMARY_IDENTITY. 
  
Chaque fournisseur de services de messagerie dont MAPI dispose d’informations peut établir une identité pour chacun de ses utilisateurs lorsqu’un client se connecte au service. Toutefois, étant donné que MAPI prend en charge les connexions à plusieurs fournisseurs de services pour chaque session MAPI, il n’existe aucune définition précise de l’identité d’un utilisateur particulier pour la session MAPI dans son ensemble ; L’identité d’un utilisateur dépend du service concerné. Les clients peuvent appeler **SetPrimaryIdentity** pour désigner l’une des nombreuses identités établies pour un utilisateur par les services de message en tant qu’identité principale pour cet utilisateur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

