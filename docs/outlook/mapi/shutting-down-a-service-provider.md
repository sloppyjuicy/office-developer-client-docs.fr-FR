---
title: Arrêt d’un fournisseur de services
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e518830b-0aaa-4ce4-a85a-07e4f00750a9
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 4e25dad1e04927e10af38cdfbf8f30c9bd04234b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339206"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="7df3e-103">Arrêt d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="7df3e-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="7df3e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7df3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7df3e-105">Lorsqu’un client appelle la méthode [IMAPISession::Logoff](imapisession-logoff.md) pour mettre fin à la session et arrêter tous les fournisseurs de services actifs, MAPI appelle à son tour les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7df3e-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="7df3e-106">[IABLogon::Logoff](iablogon-logoff.md) pour les fournisseurs de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="7df3e-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="7df3e-107">[IMSLogon::Logoff](imslogon-logoff.md) pour les fournisseurs de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="7df3e-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="7df3e-108">[IXPLogon::TransportLogoff pour](ixplogon-transportlogoff.md) les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="7df3e-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="7df3e-109">Ces méthodes ont des implémentations similaires.</span><span class="sxs-lookup"><span data-stu-id="7df3e-109">These methods have similar implementations.</span></span> <span data-ttu-id="7df3e-110">Les principales tâches effectuées par une méthode de ff de logo sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7df3e-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="7df3e-111">Libération de tous les objets ouverts, y compris les sous-objets et les objets d’état.</span><span class="sxs-lookup"><span data-stu-id="7df3e-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="7df3e-112">Appel de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l’objet de support pour décrémenter son nombre de références.</span><span class="sxs-lookup"><span data-stu-id="7df3e-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="7df3e-113">Suppression de toutes les structures [MAPIUID](mapiuid.md) inscrites de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7df3e-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="7df3e-114">Suppression de la ligne de votre fournisseur dans la table d’état.</span><span class="sxs-lookup"><span data-stu-id="7df3e-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="7df3e-115">Effectuer toutes les tâches liées au nettoyage des ressources, telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7df3e-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="7df3e-116">Arrêt d’une connexion avec un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="7df3e-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="7df3e-117">Décrémentation du nombre de références sur l’objet d’logon.</span><span class="sxs-lookup"><span data-stu-id="7df3e-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="7df3e-118">Suppression de l’objet d' logon dans la liste des objets d' logo que votre fournisseur stocke.</span><span class="sxs-lookup"><span data-stu-id="7df3e-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="7df3e-119">En mode débogage, émission de suivis pour localiser les objets dont la mémoire a été divulguée.</span><span class="sxs-lookup"><span data-stu-id="7df3e-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="7df3e-120">Lorsque votre méthode de ff de logo renvoie, MAPI appelle les appels suivants :</span><span class="sxs-lookup"><span data-stu-id="7df3e-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="7df3e-121">Méthode **IUnknown::Release** de votre objet d’logo.</span><span class="sxs-lookup"><span data-stu-id="7df3e-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="7df3e-122">Méthode d’arrêt **de** votre objet fournisseur pour effectuer les tâches de nettoyage finales.</span><span class="sxs-lookup"><span data-stu-id="7df3e-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="7df3e-123">Selon le type de votre fournisseur, l’une des méthodes suivantes est appelée :</span><span class="sxs-lookup"><span data-stu-id="7df3e-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="7df3e-124">[IABProvider::Shutdown](iabprovider-shutdown.md) pour les fournisseurs de carnets d’adresses</span><span class="sxs-lookup"><span data-stu-id="7df3e-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="7df3e-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) pour les fournisseurs de magasins de messages</span><span class="sxs-lookup"><span data-stu-id="7df3e-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="7df3e-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) pour les fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="7df3e-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="7df3e-127">Méthode **IUnknown::Release** de votre objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7df3e-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="7df3e-128">Si votre fournisseur est un magasin de messages, un appel client à [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) lancera également le processus d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="7df3e-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="7df3e-129">**StoreLogoff** arrête un fournisseur de magasin de messages particulier et n’a aucun effet sur la session.</span><span class="sxs-lookup"><span data-stu-id="7df3e-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="7df3e-130">Seul un fournisseur de magasin de messages peut être arrêté avec cette méthode ; il n’existe aucun moyen explicite d’arrêter un carnet d’adresses ou un fournisseur de transport particulier.</span><span class="sxs-lookup"><span data-stu-id="7df3e-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="7df3e-131">Pour plus d’informations sur la réponse à un appel **StoreLogoff,** voir [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7df3e-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="7df3e-132">La DLL de votre fournisseur sera déchargée lorsque MAPI appelle la fonction API Win32 **FreeLibrary**, un appel effectué après que le dernier client actif a appelé [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="7df3e-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="7df3e-133">À ce moment-là, votre fournisseur de services aura fini de s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="7df3e-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7df3e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7df3e-134">See also</span></span>



[<span data-ttu-id="7df3e-135">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="7df3e-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

