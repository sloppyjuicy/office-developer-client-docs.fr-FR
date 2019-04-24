---
title: Administration des profils et des services de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330232"
---
# <a name="administering-profiles-and-message-services"></a>Administration des profils et des services de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'administration des profils et des services de messagerie peut impliquer la création de profils, la suppression d'anciens profils et la modification du contenu des profils existants en modifiant les services de messagerie et les fournisseurs de services qu'ils contiennent. Tous les clients ne prennent pas en charge l'administration des profils et des services de messagerie en tant que fonctionnalités standard. Certains clients n'ont plus rien à voir avec les profils, plutôt que d'autoriser leurs utilisateurs à en sélectionner un lors de l'ouverture de session.
  
Si vous prenez en charge l'administration des profils ou des services de messagerie, il est probable que vous utilisiez les interfaces suivantes qui sont implémentées par MAPI:
  
- [IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md) pour administrer un service de messagerie dans un profil, accessible via [IMAPISession:: AdminServices](imapisession-adminservices.md) ou [IProfAdmin:: AdminServices](iprofadmin-adminservices.md). Les clients de messagerie appellent généralement **IMAPISession** pendant que les clients de configuration, ou les clients qui n'envoient pas ou ne reçoivent pas de messages, appellent **IProfAdmin**. Dans la mesure du possible, appelez la méthode **IProfAdmin** car elle n'entraîne pas le démarrage du service de messagerie. Pour plus d'informations sur l'utilisation de l'interface **IMsgServiceAdmin** , consultez les rubriques suivantes: [configuration d'un service de messagerie](configuring-a-message-service.md), [copie d'un service de messagerie](copying-a-message-service.md)et [Suppression d'un service de messagerie](deleting-a-message-service.md).
    
- [IProfAdmin: IUnknown](iprofadminiunknown.md) pour administrer un profil, accessible via la fonction [MAPIAdminProfiles](mapiadminprofiles.md) . Pour plus d'informations sur l'utilisation de l'interface **IProfAdmin** , consultez les rubriques suivantes: création d'un profil à [l'aide de code personnalisé](creating-a-profile-by-using-custom-code.md), [copie d'un profil](copying-a-profile.md), [Suppression d'un profil](deleting-a-profile.md), [recherche d'un nom de profil](finding-a-profile-name.md)et [définition d'un Profil par défaut](setting-a-default-profile.md).
    
- [IProfSect: IMAPIProp](iprofsectimapiprop.md) pour gérer les propriétés d'une section de profil, accessible via la méthode [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) . Pour plus d'informations sur les sections de profil, consultez la rubrique [MAPI Profiles](mapi-profiles.md).
    
- [IProviderAdmin: IUnknown](iprovideradminiunknown.md) pour administrer les fournisseurs de services dans un service de messagerie, accessible via [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md). Pour plus d'informations sur l'utilisation de l'interface **IProviderAdmin** , consultez la rubrique [Ajout ou suppression de fournisseurs dans un service de messagerie](adding-or-deleting-providers-in-a-message-service.md).
    
Soyez vigilant lors de la prise en charge de l'administration des profils et des services de messagerie. Il n'existe aucune protection contre la modification défavorable d'un profil en cours d'utilisation. MAPI peut vous empêcher de supprimer un profil en cours d'utilisation, mais ne peut pas vous empêcher de supprimer chaque service de messagerie qu'il contient. Si vous supprimez tous les services de messagerie d'un profil, tous les fournisseurs de services de ces services se bloquent, ce qui entraîne des résultats imprévisibles.
  
## <a name="in-this-section"></a>Contenu de cette section

[Création d'un profil](creating-a-profile.md)
  
> Indique comment créer un profil.
    
[Copie d'un profil](copying-a-profile.md)
  
> Indique comment copier un profil.
    
[Suppression d'un profil](deleting-a-profile.md)
  
> Décrit comment supprimer un profil.
    
[Définition d'un profil par défaut](setting-a-default-profile.md)
  
> Indique comment définir un profil par défaut.
    
[Recherche d'un nom de profil](finding-a-profile-name.md)
  
> Indique comment rechercher le nom d'un profil.
    
[Ajout d'un service de messagerie](adding-a-message-service.md)
  
> Indique comment ajouter un service de messagerie.
    
[Configuration d'un service de messagerie](configuring-a-message-service.md)
  
> Décrit la configuration d'un service de messagerie.
    
[Copie d'un service de messagerie](copying-a-message-service.md)
  
> Décrit comment copier un service de messagerie vers un profil.
    
[Suppression d'un service de messagerie](deleting-a-message-service.md)
  
> Décrit comment supprimer un service de messagerie.
    
[Ajout ou suppression de fournisseurs dans un service de messagerie](adding-or-deleting-providers-in-a-message-service.md)
  
> Indique comment ajouter ou supprimer des fournisseurs dans un service de messagerie.
    

