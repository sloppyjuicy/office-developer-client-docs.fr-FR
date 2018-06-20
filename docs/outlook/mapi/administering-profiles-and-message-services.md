---
title: Administration des profils et des Services de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89a2ac43-9601-47fc-b736-db48585fe879
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 71e8cf50c1951abf1df6163cae4757ffebc979b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782893"
---
# <a name="administering-profiles-and-message-services"></a><span data-ttu-id="4bcae-103">Administration des profils et des Services de messagerie</span><span class="sxs-lookup"><span data-stu-id="4bcae-103">Administering Profiles and Message Services</span></span>

  
  
<span data-ttu-id="4bcae-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4bcae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4bcae-105">Profil et le message d’administration du service peut impliquer créer de nouveaux profils, la suppression des anciens profils et modifier le contenu des profils existants en modifiant le message les services et les fournisseurs de services qu’ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="4bcae-105">Profile and message service administration can involve creating new profiles, deleting old profiles, and modifying the contents of existing profiles by changing the message services and service providers contained within them.</span></span> <span data-ttu-id="4bcae-106">Pas tous les clients prennent en charge l’administration du service de profil et message en tant que fonctionnalités standard.</span><span class="sxs-lookup"><span data-stu-id="4bcae-106">Not all clients support profile and message service administration as standard features.</span></span> <span data-ttu-id="4bcae-107">Certains clients ont rien d’autre à faire avec des profils à autoriser les utilisateurs à sélectionner une au moment de l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="4bcae-107">Some clients have nothing more to do with profiles than allow their users to select one at logon time.</span></span>
  
<span data-ttu-id="4bcae-108">Si vous prenez en charge d’administration du service de profil ou un message, sans doute que vous allez utiliser les interfaces suivantes qui sont implémentés par MAPI :</span><span class="sxs-lookup"><span data-stu-id="4bcae-108">If you support profile or message service administration, chances are you will use the following interfaces that are implemented by MAPI:</span></span>
  
- <span data-ttu-id="4bcae-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) pour administrer un service de message dans un profil, accessible via [IMAPISession::AdminServices](imapisession-adminservices.md) ou [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span><span class="sxs-lookup"><span data-stu-id="4bcae-109">[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md) to administer a message service in a profile, accessible through either [IMAPISession::AdminServices](imapisession-adminservices.md) or [IProfAdmin::AdminServices](iprofadmin-adminservices.md).</span></span> <span data-ttu-id="4bcae-110">En général, les clients de messagerie appellent **IMAPISession** lors de la configuration clients ou des clients qui ne pas envoyer ou recevoir des messages, appelez **IProfAdmin**.</span><span class="sxs-lookup"><span data-stu-id="4bcae-110">Messaging clients typically call **IMAPISession** while configuration clients, or clients that do not send or receive messages, call **IProfAdmin**.</span></span> <span data-ttu-id="4bcae-111">La mesure du possible, appelez la méthode de **IProfAdmin** , car elle n’entraîne pas le service de message doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="4bcae-111">Whenever possible, call the **IProfAdmin** method because it does not cause the message service to be started.</span></span> <span data-ttu-id="4bcae-112">Pour plus d’informations sur l’utilisation de l’interface **IMsgServiceAdmin** , consultez les rubriques suivantes : [configuration d’un Service de Message](configuring-a-message-service.md)et [copie d’un Service de Message de](copying-a-message-service.md) [suppression d’un Service de Message](deleting-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="4bcae-112">For more information about using the **IMsgServiceAdmin** interface, see the following topics: [Configuring a Message Service](configuring-a-message-service.md), [Copying a Message Service](copying-a-message-service.md), and [Deleting a Message Service](deleting-a-message-service.md).</span></span>
    
- <span data-ttu-id="4bcae-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) pour administrer un profil, accessible via la fonction [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="4bcae-113">[IProfAdmin : IUnknown](iprofadminiunknown.md) to administer a profile, accessible through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> <span data-ttu-id="4bcae-114">Pour plus d’informations sur l’utilisation de l’interface **IProfAdmin** , consultez les rubriques suivantes : [Création d’un profil en utilisant le Code personnalisé](creating-a-profile-by-using-custom-code.md), [copie d’un profil](copying-a-profile.md), [suppression d’un profil](deleting-a-profile.md), [recherche d’un nom de profil](finding-a-profile-name.md)et [paramètre un Profil par défaut](setting-a-default-profile.md).</span><span class="sxs-lookup"><span data-stu-id="4bcae-114">For more information about using the **IProfAdmin** interface, see the following topics: [Creating a Profile by Using Custom Code](creating-a-profile-by-using-custom-code.md), [Copying a Profile](copying-a-profile.md), [Deleting a Profile](deleting-a-profile.md), [Finding a Profile Name](finding-a-profile-name.md), and [Setting a Default Profile](setting-a-default-profile.md).</span></span>
    
- <span data-ttu-id="4bcae-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) pour mettre à jour les propriétés d’une section de profil, accessible via la méthode [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) ou [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="4bcae-115">[IProfSect : IMAPIProp](iprofsectimapiprop.md) to maintain the properties in a profile section, accessible through the [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> <span data-ttu-id="4bcae-116">Pour plus d’informations sur les sections de profil, voir [Profils MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="4bcae-116">For more information about profile sections, see [MAPI Profiles](mapi-profiles.md).</span></span>
    
- <span data-ttu-id="4bcae-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) pour administrer les fournisseurs de services dans un service de message, accessible via [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span><span class="sxs-lookup"><span data-stu-id="4bcae-117">[IProviderAdmin : IUnknown](iprovideradminiunknown.md) to administer the service providers in a message service, accessible through [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md).</span></span> <span data-ttu-id="4bcae-118">Pour plus d’informations sur l’utilisation de l’interface **IProviderAdmin** , voir [Ajout ou suppression des fournisseurs dans un Service de Message](adding-or-deleting-providers-in-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="4bcae-118">For more information about using the **IProviderAdmin** interface, see [Adding or Deleting Providers in a Message Service](adding-or-deleting-providers-in-a-message-service.md).</span></span>
    
<span data-ttu-id="4bcae-119">Soyez prudent dans votre prise en charge de l’administration du service de profil et le message.</span><span class="sxs-lookup"><span data-stu-id="4bcae-119">Be careful in your support of profile and message service administration.</span></span> <span data-ttu-id="4bcae-120">Il n’existe aucune protection contre la modification négatif d’un profil qui est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="4bcae-120">There are no safeguards to protect against adversely modifying a profile that is in use.</span></span> <span data-ttu-id="4bcae-121">MAPI peut empêcher la suppression d’un profil en cours d’utilisation, mais ne peut pas empêcher la suppression de tous les services dans ce message.</span><span class="sxs-lookup"><span data-stu-id="4bcae-121">MAPI can prevent you from deleting a profile in use, but cannot prevent you from deleting every message service in it.</span></span> <span data-ttu-id="4bcae-122">Si vous supprimez tous les services dans un profil de message, tous les fournisseurs de services dans ces services seront arrête ce qui provoque des résultats imprévisibles se produise.</span><span class="sxs-lookup"><span data-stu-id="4bcae-122">If you delete every message service in a profile, all of the service providers in these services will stop thereby causing unpredictable results to occur.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="4bcae-123">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4bcae-123">In this section</span></span>

[<span data-ttu-id="4bcae-124">Création d’un profil</span><span class="sxs-lookup"><span data-stu-id="4bcae-124">Creating a Profile</span></span>](creating-a-profile.md)
  
> <span data-ttu-id="4bcae-125">Explique comment créer un profil.</span><span class="sxs-lookup"><span data-stu-id="4bcae-125">Describes how to create a profile.</span></span>
    
[<span data-ttu-id="4bcae-126">Copie d’un profil</span><span class="sxs-lookup"><span data-stu-id="4bcae-126">Copying a Profile</span></span>](copying-a-profile.md)
  
> <span data-ttu-id="4bcae-127">Explique comment copier un profil.</span><span class="sxs-lookup"><span data-stu-id="4bcae-127">Describes how to copy a profile.</span></span>
    
[<span data-ttu-id="4bcae-128">Suppression d’un profil</span><span class="sxs-lookup"><span data-stu-id="4bcae-128">Deleting a Profile</span></span>](deleting-a-profile.md)
  
> <span data-ttu-id="4bcae-129">Explique comment supprimer un profil.</span><span class="sxs-lookup"><span data-stu-id="4bcae-129">Describes how to delete a profile.</span></span>
    
[<span data-ttu-id="4bcae-130">Définir un profil par défaut</span><span class="sxs-lookup"><span data-stu-id="4bcae-130">Setting a Default Profile</span></span>](setting-a-default-profile.md)
  
> <span data-ttu-id="4bcae-131">Décrit comment définir un profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="4bcae-131">Describes how to set a default profile.</span></span>
    
[<span data-ttu-id="4bcae-132">Recherche d’un nom de profil</span><span class="sxs-lookup"><span data-stu-id="4bcae-132">Finding a Profile Name</span></span>](finding-a-profile-name.md)
  
> <span data-ttu-id="4bcae-133">Décrit comment rechercher un nom d’un profil.</span><span class="sxs-lookup"><span data-stu-id="4bcae-133">Describes how to find a name of a profile.</span></span>
    
[<span data-ttu-id="4bcae-134">Ajout d’un Service de Message</span><span class="sxs-lookup"><span data-stu-id="4bcae-134">Adding a Message Service</span></span>](adding-a-message-service.md)
  
> <span data-ttu-id="4bcae-135">Explique comment ajouter un service de message.</span><span class="sxs-lookup"><span data-stu-id="4bcae-135">Describes how to add a message service.</span></span>
    
[<span data-ttu-id="4bcae-136">Configuration d’un Service de Message</span><span class="sxs-lookup"><span data-stu-id="4bcae-136">Configuring a Message Service</span></span>](configuring-a-message-service.md)
  
> <span data-ttu-id="4bcae-137">Explique comment configurer un service de message.</span><span class="sxs-lookup"><span data-stu-id="4bcae-137">Describes how to configure a message service.</span></span>
    
[<span data-ttu-id="4bcae-138">Copie d’un Service de Message</span><span class="sxs-lookup"><span data-stu-id="4bcae-138">Copying a Message Service</span></span>](copying-a-message-service.md)
  
> <span data-ttu-id="4bcae-139">Décrit la copie d’un service de message à un profil.</span><span class="sxs-lookup"><span data-stu-id="4bcae-139">Describes how to copy a message service to a profile.</span></span>
    
[<span data-ttu-id="4bcae-140">Suppression d’un Service de Message</span><span class="sxs-lookup"><span data-stu-id="4bcae-140">Deleting a Message Service</span></span>](deleting-a-message-service.md)
  
> <span data-ttu-id="4bcae-141">Explique comment supprimer un service de message.</span><span class="sxs-lookup"><span data-stu-id="4bcae-141">Describes how to delete a message service.</span></span>
    
[<span data-ttu-id="4bcae-142">Ajout ou suppression de fournisseurs dans un Service de Message</span><span class="sxs-lookup"><span data-stu-id="4bcae-142">Adding or Deleting Providers in a Message Service</span></span>](adding-or-deleting-providers-in-a-message-service.md)
  
> <span data-ttu-id="4bcae-143">Décrit comment ajouter ou supprimer des fournisseurs dans un service de message.</span><span class="sxs-lookup"><span data-stu-id="4bcae-143">Describes how to add or delete providers in a message service.</span></span>
    

