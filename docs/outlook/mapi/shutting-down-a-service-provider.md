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
ms.openlocfilehash: 70db0b0a62568cc499cf915634756bb422ae82ca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567194"
---
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="33dc1-103">Arrêt d’un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="33dc1-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="33dc1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33dc1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33dc1-105">Lorsqu’un client appelle la méthode [IMAPISession::Logoff](imapisession-logoff.md) à la fin de la session et arrêter tous les fournisseurs de service active, MAPI appelle à son tour les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="33dc1-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="33dc1-106">[IABLogon::Logoff](iablogon-logoff.md) pour les fournisseurs de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="33dc1-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="33dc1-107">[IMSLogon::Logoff](imslogon-logoff.md) pour les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="33dc1-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="33dc1-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) pour les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="33dc1-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="33dc1-109">Ces méthodes ont des implémentations similaires.</span><span class="sxs-lookup"><span data-stu-id="33dc1-109">These methods have similar implementations.</span></span> <span data-ttu-id="33dc1-110">Les principales tâches qui effectue une méthode de fermeture de session sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="33dc1-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="33dc1-111">Libérer tous les objets ouverts, y compris les sous-objets et objets d’état.</span><span class="sxs-lookup"><span data-stu-id="33dc1-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="33dc1-112">Appel de méthode [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l’objet de la prise en charge pour décrémenter son décompte de références.</span><span class="sxs-lookup"><span data-stu-id="33dc1-112">Calling the support object's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="33dc1-113">Suppression de toutes les structures [MAPIUID](mapiuid.md) inscrits votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="33dc1-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="33dc1-114">Suppression de ligne de votre fournisseur dans la table d’état.</span><span class="sxs-lookup"><span data-stu-id="33dc1-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="33dc1-115">Effectue toutes les tâches qui sont associées au nettoyage de ressources, telles que les suivantes :</span><span class="sxs-lookup"><span data-stu-id="33dc1-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="33dc1-116">Arrêt d’une connexion avec un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="33dc1-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="33dc1-117">Nombre de décrémenter la référence sur l’objet d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="33dc1-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="33dc1-118">Suppression de l’objet d’ouverture de session dans la liste d’objets d’ouverture de session qui stocke de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="33dc1-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="33dc1-119">En mode débogage, émettre des traces pour localiser des objets qui ont une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="33dc1-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="33dc1-120">Retourne la méthode de fermeture de session MAPI appelle les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="33dc1-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="33dc1-121">Méthode **IUnknown::Release** de l’objet d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="33dc1-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="33dc1-122">Méthode de **l’arrêt** de l’objet de votre fournisseur pour effectuer les tâches de nettoyage final.</span><span class="sxs-lookup"><span data-stu-id="33dc1-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="33dc1-123">Selon le type de votre fournisseur, une des méthodes suivantes est appelée :</span><span class="sxs-lookup"><span data-stu-id="33dc1-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="33dc1-124">[IABProvider::Shutdown](iabprovider-shutdown.md) pour les fournisseurs de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="33dc1-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="33dc1-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) pour les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="33dc1-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="33dc1-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) pour les fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="33dc1-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="33dc1-127">Méthode **IUnknown::Release** de l’objet de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="33dc1-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="33dc1-128">Si votre fournisseur est une banque de messages, un appel client [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) lance également le processus d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="33dc1-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="33dc1-129">**StoreLogoff** fournisseur de magasins d’un message particulier s’arrête et n’a aucun effet sur la session.</span><span class="sxs-lookup"><span data-stu-id="33dc1-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="33dc1-130">Qu’un fournisseur de magasin de message peut être arrêté avec cette méthode ; Il n’existe pas de manière explicite pour arrêter un fournisseur de transport ou du carnet d’adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="33dc1-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="33dc1-131">Pour plus d’informations sur la façon de répondre à un **StoreLogoff** appel, voir [Arrêt vers le bas un Message fournisseur de magasins](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="33dc1-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="33dc1-132">DLL de votre fournisseur sera déchargé MAPI appelle la fonction API Win32 **FreeLibrary**, un appel est effectué après que le dernier client actif a appelé [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="33dc1-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="33dc1-133">À ce stade, votre fournisseur de services est arrêtés.</span><span class="sxs-lookup"><span data-stu-id="33dc1-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33dc1-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33dc1-134">See also</span></span>



[<span data-ttu-id="33dc1-135">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="33dc1-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

