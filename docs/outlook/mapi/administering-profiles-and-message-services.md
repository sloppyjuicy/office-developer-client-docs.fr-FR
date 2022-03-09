---
title: Administration des profils et des services de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
ms.openlocfilehash: be3bb72d49da636fbe5fe301f17cea1dc2f79d9c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374508"
---
# <a name="administering-profiles-and-message-services"></a>Administration des profils et des services de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’administration des profils et des services de messagerie peut impliquer la création de profils, la suppression d’anciens profils et la modification du contenu des profils existants en modifiant les services de messagerie et les fournisseurs de services qu’ils contiennent. Tous les clients ne sont pas tous en charge l’administration des profils et des services de messages en tant que fonctionnalités standard. Certains clients n’ont rien d’autre à faire avec les profils que d’autoriser leurs utilisateurs à en sélectionner un à l’heure de l’logo.
  
Si vous prendre en charge l’administration de profil ou de service de message, il est fort de pouvoir utiliser les interfaces suivantes implémentées par MAPI :
  
- [IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) pour administrer un service de message dans un profil, accessible via [IMAPISession::AdminServices](imapisession-adminservices.md) ou [IProfAdmin::AdminServices](iprofadmin-adminservices.md). Les clients de messagerie appellent généralement **IMAPISession** tandis que les clients de configuration, ou les clients qui n’envoient ou ne reçoivent pas de messages, appellent **IProfAdmin**. Dans la mesure du possible, appelez **la méthode IProfAdmin** , car le service de message n’est pas démarré. Pour plus d’informations sur l’utilisation de l’interface **IMsgServiceAdmin** , consultez les rubriques suivantes : [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).
    
- [IProfAdmin : IUnknown](iprofadminiunknown.md) pour administrer un profil, accessible via la [fonction MAPIAdminProfiles](mapiadminprofiles.md) . Pour plus d’informations sur l’utilisation de l’interface **IProfAdmin**, voir les rubriques suivantes : Création d’un profil à l’aide de [code](creating-a-profile-by-using-custom-code.md) [personnalisé, copie](copying-a-profile.md) d’un [profil, suppression](deleting-a-profile.md) d’un [profil, recherche](finding-a-profile-name.md) d’un nom de profil et définition d’un profil par [défaut.](setting-a-default-profile.md)
    
- [IProfSect : IMAPIProp](iprofsectimapiprop.md) pour gérer les propriétés dans une section de profil, accessible via la méthode [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . Pour plus d’informations sur les sections de profil, voir [Profils MAPI](mapi-profiles.md).
    
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md) pour administrer les fournisseurs de services dans un service de messagerie, accessible via [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Pour plus d’informations sur l’utilisation de l’interface **IProviderAdmin** , voir Ajout ou suppression [de fournisseurs dans un service de messagerie](adding-or-deleting-providers-in-a-message-service.md).
    
Soyez prudent dans la prise en charge de l’administration des services de profil et de message. Il n’existe aucune protection contre la modification négative d’un profil en cours d’utilisation. MAPI peut vous empêcher de supprimer un profil en cours d’utilisation, mais ne peut pas vous empêcher de supprimer chaque service de message qu’il insérez. Si vous supprimez tous les services de messagerie d’un profil, tous les fournisseurs de services de ces services s’arrêteront, ce qui provoquera des résultats imprévisibles.
  
## <a name="in-this-section"></a>Dans cette section

[Création d’un profil](creating-a-profile.md)
  
> Décrit comment créer un profil.
    
[Copie d’un profil](copying-a-profile.md)
  
> Décrit comment copier un profil.
    
[Suppression d’un profil](deleting-a-profile.md)
  
> Décrit comment supprimer un profil.
    
[Définition d’un profil par défaut](setting-a-default-profile.md)
  
> Décrit comment définir un profil par défaut.
    
[Recherche d’un nom de profil](finding-a-profile-name.md)
  
> Indique comment trouver un nom de profil.
    
[Ajout d’un service de message](adding-a-message-service.md)
  
> Décrit comment ajouter un service de message.
    
[Configuration d’un service de message](configuring-a-message-service.md)
  
> Décrit comment configurer un service de message.
    
[Copie d’un service de message](copying-a-message-service.md)
  
> Décrit comment copier un service de message dans un profil.
    
[Suppression d’un service de message](deleting-a-message-service.md)
  
> Décrit comment supprimer un service de message.
    
[Ajout ou suppression de fournisseurs dans un service de messagerie](adding-or-deleting-providers-in-a-message-service.md)
  
> Décrit comment ajouter ou supprimer des fournisseurs dans un service de messagerie.
    

