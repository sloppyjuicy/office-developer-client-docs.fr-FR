---
title: Administration des profils et des services de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 124f4875834e035e29d4c63e52789bf07f18258d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587543"
---
# <a name="administering-profiles-and-message-services"></a>Administration des profils et des services de messagerie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Profil et le message d’administration du service peut impliquer créer de nouveaux profils, la suppression des anciens profils et modifier le contenu des profils existants en modifiant le message les services et les fournisseurs de services qu’ils contiennent. Pas tous les clients prennent en charge l’administration du service de profil et message en tant que fonctionnalités standard. Certains clients ont rien d’autre à faire avec des profils à autoriser les utilisateurs à sélectionner une au moment de l’ouverture de session.
  
Si vous prenez en charge d’administration du service de profil ou un message, sans doute que vous allez utiliser les interfaces suivantes qui sont implémentés par MAPI :
  
- [IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) pour administrer un service de message dans un profil, accessible via [IMAPISession::AdminServices](imapisession-adminservices.md) ou [IProfAdmin::AdminServices](iprofadmin-adminservices.md). En général, les clients de messagerie appellent **IMAPISession** lors de la configuration clients ou des clients qui ne pas envoyer ou recevoir des messages, appelez **IProfAdmin**. La mesure du possible, appelez la méthode de **IProfAdmin** , car elle n’entraîne pas le service de message doit être démarré. Pour plus d’informations sur l’utilisation de l’interface **IMsgServiceAdmin** , consultez les rubriques suivantes : [configuration d’un Service de Message](configuring-a-message-service.md)et [copie d’un Service de Message de](copying-a-message-service.md) [suppression d’un Service de Message](deleting-a-message-service.md).
    
- [IProfAdmin : IUnknown](iprofadminiunknown.md) pour administrer un profil, accessible via la fonction [MAPIAdminProfiles](mapiadminprofiles.md) . Pour plus d’informations sur l’utilisation de l’interface **IProfAdmin** , consultez les rubriques suivantes : [Création d’un profil en utilisant le Code personnalisé](creating-a-profile-by-using-custom-code.md), [copie d’un profil](copying-a-profile.md), [suppression d’un profil](deleting-a-profile.md), [recherche d’un nom de profil](finding-a-profile-name.md)et [paramètre un Profil par défaut](setting-a-default-profile.md).
    
- [IProfSect : IMAPIProp](iprofsectimapiprop.md) pour mettre à jour les propriétés d’une section de profil, accessible via la méthode [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) . Pour plus d’informations sur les sections de profil, voir [Profils MAPI](mapi-profiles.md).
    
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md) pour administrer les fournisseurs de services dans un service de message, accessible via [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Pour plus d’informations sur l’utilisation de l’interface **IProviderAdmin** , voir [Ajout ou suppression des fournisseurs dans un Service de Message](adding-or-deleting-providers-in-a-message-service.md).
    
Soyez prudent dans votre prise en charge de l’administration du service de profil et le message. Il n’existe aucune protection contre la modification négatif d’un profil qui est en cours d’utilisation. MAPI peut empêcher la suppression d’un profil en cours d’utilisation, mais ne peut pas empêcher la suppression de tous les services dans ce message. Si vous supprimez tous les services dans un profil de message, tous les fournisseurs de services dans ces services seront arrête ce qui provoque des résultats imprévisibles se produise.
  
## <a name="in-this-section"></a>Dans cette section

[Création d’un profil](creating-a-profile.md)
  
> Explique comment créer un profil.
    
[Copie d’un profil](copying-a-profile.md)
  
> Explique comment copier un profil.
    
[Suppression d’un profil](deleting-a-profile.md)
  
> Explique comment supprimer un profil.
    
[Définition d’un profil par défaut](setting-a-default-profile.md)
  
> Décrit comment définir un profil par défaut.
    
[Recherche d’un nom de profil](finding-a-profile-name.md)
  
> Décrit comment rechercher un nom d’un profil.
    
[Ajout d’un service de messagerie](adding-a-message-service.md)
  
> Explique comment ajouter un service de message.
    
[Configuration d’un service de messagerie](configuring-a-message-service.md)
  
> Explique comment configurer un service de message.
    
[Copie d’un service de messagerie](copying-a-message-service.md)
  
> Décrit la copie d’un service de message à un profil.
    
[Suppression d’un service de messagerie](deleting-a-message-service.md)
  
> Explique comment supprimer un service de message.
    
[Ajout ou suppression de fournisseurs dans un service de messagerie](adding-or-deleting-providers-in-a-message-service.md)
  
> Décrit comment ajouter ou supprimer des fournisseurs dans un service de message.
    

