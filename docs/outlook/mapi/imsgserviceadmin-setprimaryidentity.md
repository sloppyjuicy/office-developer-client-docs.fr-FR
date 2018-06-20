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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 38d55f45280b0b037dc9b5cbbd0dc8809ed04e35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784238"
---
# <a name="imsgserviceadminsetprimaryidentity"></a>IMsgServiceAdmin::SetPrimaryIdentity

  
  
**S’applique à**: Outlook 
  
Désigne un service de message pour être le fournisseur de l’identité principale pour le profil.
  
```cpp
HRESULT SetPrimaryIdentity(
  LPMAPIUID lpUID,
  ULONG ulFlags  
);
```

## <a name="parameters"></a>Paramètres

 _lpUID_
  
> [in] Un pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique pour le service de message fournir l’identité du principale, ou valeur NULL, ce qui indique que **SetPrimaryIdentity** doit effacer l’identité en cours. 
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le service de message a été correctement assigné le fournisseur de l’identité du principal.
    
MAPI_E_NO_ACCESS 
  
> **SetPrimaryIdentity** a tenté de désigner un service de message qui possède l’indicateur SERVICE_NO_PRIMARY_IDENTITY dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::SetPrimaryIdentity** établit un service de message en tant que le fournisseur de l’identité principale pour le profil. L’identité du principale est généralement l’utilisateur qui est connecté au service de message. Il est représenté par trois propriétés : 
  
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))
    
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))
    
Chaque fournisseur de service dans le service message désignés définit ces trois propriétés pour le nom complet, un identificateur d’entrée et une clé de recherche de l’utilisateur de messagerie qui fournit l’identité du principale. Les clients peuvent récupérer identificateur d’entrée de l’identité principale en appelant la méthode [IMAPISession::QueryIdentity](imapisession-queryidentity.md) . 
  
La propriété **PR_RESOURCE_FLAGS** est définie à STATUS_PRIMARY_IDENTITY pour chaque fournisseur qui est un membre du service de message qui fournit l’identité principale et SERVICE_PRIMARY_IDENTITY pour le service de message. Lorsqu’un fournisseur de services ne peut pas fournir l’identité du principale pour son service de message, il définit **PR_RESOURCE_FLAGS** STATUS_NO_PRIMARY_IDENTITY. **SetPrimaryIdentity** définit la propriété **PR_RESOURCE_FLAGS** de chaque service de message qui ne fournit pas l’identité principale à SERVICE_NO_PRIMARY_IDENTITY. 
  
Chaque fournisseur de service de message MAPI dispose d’informations sur peut établir une identité pour chacun de ses utilisateurs lorsqu’un client se connecte au service. Toutefois, MAPI prenant en charge les connexions à plusieurs fournisseurs de services pour chaque session MAPI, il n’existe aucune ferme définition de l’identité d’un utilisateur particulier pour la session MAPI dans sa globalité ; l’identité d’un utilisateur dépend du service qui est impliqué. Les clients peuvent appeler **SetPrimaryIdentity** pour désigner l’une des nombreuses identités ouverte pour un utilisateur par les services de messagerie comme l’identité du principale de cet utilisateur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

