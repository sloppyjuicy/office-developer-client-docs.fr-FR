---
title: IMsgServiceAdminSetPrimaryIdentity
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.SetPrimaryIdentity
api_type:
- COM
ms.assetid: 763cab41-f6f6-4cb0-8cb8-170fdf2a92e6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b237a57dfea020c7bfcb66d49d43428c1f6506c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430363"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Désigne un service de messagerie en tant que fournisseur de l'identité principale pour le profil.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique pour le service de message afin de fournir l'identité principale, ou null, qui indique que **SetPrimaryIdentity** doit effacer l'identité actuelle. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le service de messagerie a été correctement attribué au fournisseur de l'identité principale.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** a tenté de désigner un service de messagerie dont l'indicateur SERVICE_NO_PRIMARY_IDENTITY est défini dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin:: SetPrimaryIdentity** établit un service de messagerie en tant que fournisseur de l'identité principale pour le profil. L'identité principale est généralement l'utilisateur qui est connecté au service de messagerie. Il est représenté par trois propriétés: 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Chaque fournisseur de services dans le service de messages désigné définit ces trois propriétés sur le nom complet, l'identificateur d'entrée et la clé de recherche de l'utilisateur de messagerie qui fournit l'identité principale. Les clients peuvent récupérer l'identificateur d'entrée de l'identité principale en appelant la méthode [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) . 
  
La propriété **PR_RESOURCE_FLAGS** est définie sur STATUS_PRIMARY_IDENTITY pour chaque fournisseur qui est membre du service de messagerie qui fournit l'identité principale et sur SERVICE_PRIMARY_IDENTITY pour le service de messagerie. Lorsqu'un fournisseur de services ne peut pas fournir l'identité principale pour son service de messagerie, il définit **PR_RESOURCE_FLAGS** sur STATUS_NO_PRIMARY_IDENTITY. **SetPrimaryIdentity** définit la propriété **PR_RESOURCE_FLAGS** de chaque service de messagerie qui ne fournit pas l'identité principale à SERVICE_NO_PRIMARY_IDENTITY. 
  
Chaque fournisseur de services de messagerie pour lequel MAPI dispose d'informations sur peut établir une identité pour chacun de ses utilisateurs lorsqu'un client se connecte au service. Toutefois, dans la mesure où MAPI prend en charge les connexions à plusieurs fournisseurs de services pour chaque session MAPI, il n'existe pas de définition ferme de l'identité d'un utilisateur particulier pour la session MAPI dans son ensemble. l'identité d'un utilisateur dépend du service impliqué. Les clients peuvent appeler **SetPrimaryIdentity** pour désigner l'une des nombreuses identités établies pour un utilisateur par les services de messagerie en tant qu'identité principale de cet utilisateur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

