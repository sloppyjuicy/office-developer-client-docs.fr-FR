---
title: Administration des profils et des services de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1e64241008a4adde4431b2c9683199294f21e396
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410559"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="846b8-103">Administration des profils et des services de messages</span><span class="sxs-lookup"><span data-stu-id="846b8-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="846b8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="846b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="846b8-105">L’administration des services de messagerie et de profil peut impliquer la création de profils, la suppression d’anciens profils et la modification du contenu des profils existants en modifiant les services de messagerie et les fournisseurs de services qu’ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="846b8-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="846b8-106">Tous les clients ne sont pas tous en charge l’administration des profils et des services de messages en tant que fonctionnalités standard.</span><span class="sxs-lookup"><span data-stu-id="846b8-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="846b8-107">Certains clients n’ont rien d’autre à faire avec les profils que d’autoriser leurs utilisateurs à en sélectionner un à l’heure de l’logo.</span><span class="sxs-lookup"><span data-stu-id="846b8-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="846b8-108">Si vous prendre en charge l’administration de profil ou de service de message, vous utiliserez peut-être les interfaces suivantes implémentées par MAPI :</span><span class="sxs-lookup"><span data-stu-id="846b8-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="846b8-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) pour administrer un service de message dans un profil, accessible via [IMAPISession::AdminServices](imapisession-adminservices.md) ou [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="846b8-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="846b8-110">Les clients de messagerie appellent généralement **IMAPISession** tandis que les clients de configuration, ou les clients qui n’envoient ou ne reçoivent pas de messages, appellent **IProfAdmin**.</span><span class="sxs-lookup"><span data-stu-id="846b8-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="846b8-111">Dans la mesure du possible, appelez **la méthode IProfAdmin,** car le service de message n’est pas démarré.</span><span class="sxs-lookup"><span data-stu-id="846b8-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="846b8-112">Pour plus d’informations sur l’utilisation de l’interface **IMsgServiceAdmin,** consultez les rubriques suivantes : Configuration d’un service de [message,](configuring-a-message-service.md)copie d’un [service](copying-a-message-service.md)de message et suppression d’un [service de message.](deleting-a-message-service.md)</span><span class="sxs-lookup"><span data-stu-id="846b8-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="846b8-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) pour administrer un profil, accessible via la [fonction MAPIAdminProfiles.](mapiadminprofiles.md)</span><span class="sxs-lookup"><span data-stu-id="846b8-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="846b8-114">Pour plus d’informations sur l’utilisation de l’interface **IProfAdmin,** consultez les rubriques suivantes : Création d’un profil à l’aide de [code](creating-a-profile-by-using-custom-code.md) [personnalisé,](copying-a-profile.md)copie d’un [profil,](deleting-a-profile.md)suppression d’un [profil,](finding-a-profile-name.md)recherche d’un nom de profil et définition d’un profil par [défaut.](setting-a-default-profile.md)</span><span class="sxs-lookup"><span data-stu-id="846b8-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="846b8-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) pour gérer les propriétés dans une section de profil, accessibles via la méthode [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="846b8-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="846b8-116">Pour plus d’informations sur les sections de profil, voir [Profils MAPI.](mapi-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="846b8-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="846b8-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) pour administrer les fournisseurs de services dans un service de messagerie, accessible via [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="846b8-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="846b8-118">Pour plus d’informations sur l’utilisation de l’interface **IProviderAdmin,** voir Ajout ou suppression de fournisseurs [dans un service de messagerie.](adding-or-deleting-providers-in-a-message-service.md)</span><span class="sxs-lookup"><span data-stu-id="846b8-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="846b8-119">Soyez prudent dans la prise en charge de l’administration des services de profil et de message.</span><span class="sxs-lookup"><span data-stu-id="846b8-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="846b8-120">Il n’existe aucune protection contre la modification négative d’un profil en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="846b8-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="846b8-121">MAPI peut vous empêcher de supprimer un profil en cours d’utilisation, mais ne peut pas vous empêcher de supprimer chaque service de message qu’il comprend.</span><span class="sxs-lookup"><span data-stu-id="846b8-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="846b8-122">Si vous supprimez tous les services de messagerie d’un profil, tous les fournisseurs de services de ces services s’arrêteront, ce qui provoquera des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="846b8-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="846b8-123">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="846b8-123">In this section</span></span>

[<span data-ttu-id="846b8-124">Création d’un profil</span><span class="sxs-lookup"><span data-stu-id="846b8-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="846b8-125">Décrit comment créer un profil.</span><span class="sxs-lookup"><span data-stu-id="846b8-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="846b8-126">Copie d’un profil</span><span class="sxs-lookup"><span data-stu-id="846b8-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="846b8-127">Décrit comment copier un profil.</span><span class="sxs-lookup"><span data-stu-id="846b8-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="846b8-128">Suppression d’un profil</span><span class="sxs-lookup"><span data-stu-id="846b8-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="846b8-129">Décrit comment supprimer un profil.</span><span class="sxs-lookup"><span data-stu-id="846b8-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="846b8-130">Définition d’un profil par défaut</span><span class="sxs-lookup"><span data-stu-id="846b8-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="846b8-131">Décrit comment définir un profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="846b8-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="846b8-132">Recherche d’un nom de profil</span><span class="sxs-lookup"><span data-stu-id="846b8-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="846b8-133">Décrit comment rechercher un nom de profil.</span><span class="sxs-lookup"><span data-stu-id="846b8-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="846b8-134">Ajout d’un service de message</span><span class="sxs-lookup"><span data-stu-id="846b8-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="846b8-135">Décrit comment ajouter un service de message.</span><span class="sxs-lookup"><span data-stu-id="846b8-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="846b8-136">Configuration d’un service de message</span><span class="sxs-lookup"><span data-stu-id="846b8-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="846b8-137">Décrit comment configurer un service de message.</span><span class="sxs-lookup"><span data-stu-id="846b8-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="846b8-138">Copie d’un service de message</span><span class="sxs-lookup"><span data-stu-id="846b8-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="846b8-139">Décrit comment copier un service de message dans un profil.</span><span class="sxs-lookup"><span data-stu-id="846b8-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="846b8-140">Suppression d’un service de message</span><span class="sxs-lookup"><span data-stu-id="846b8-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="846b8-141">Décrit comment supprimer un service de message.</span><span class="sxs-lookup"><span data-stu-id="846b8-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="846b8-142">Ajout ou suppression de fournisseurs dans un service de messagerie</span><span class="sxs-lookup"><span data-stu-id="846b8-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="846b8-143">Décrit comment ajouter ou supprimer des fournisseurs dans un service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="846b8-143">Describes how to add or delete providers in a message service.</span></span>
    

