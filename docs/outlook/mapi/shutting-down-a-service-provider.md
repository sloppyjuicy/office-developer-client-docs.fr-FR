---
title: Arrêt d'un fournisseur de services
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
# <a name="shutting-down-a-service-provider"></a><span data-ttu-id="70752-103">Arrêt d'un fournisseur de services</span><span class="sxs-lookup"><span data-stu-id="70752-103">Shutting Down a Service Provider</span></span>

 
  
<span data-ttu-id="70752-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70752-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70752-105">Lorsqu'un client appelle la méthode [IMAPISession:: Logoff](imapisession-logoff.md) pour mettre fin à la session et arrêter tous les fournisseurs de services actifs, MAPI à son tour appelle les méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="70752-105">When a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end the session and shut down all active service providers, MAPI in turn calls the following methods:</span></span> 
  
- <span data-ttu-id="70752-106">[IABLogon:: Logoff](iablogon-logoff.md) pour les fournisseurs de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="70752-106">[IABLogon::Logoff](iablogon-logoff.md) for address book providers.</span></span> 
    
- <span data-ttu-id="70752-107">[IMSLogon:: Logoff](imslogon-logoff.md) pour les fournisseurs de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="70752-107">[IMSLogon::Logoff](imslogon-logoff.md) for message store providers.</span></span> 
    
- <span data-ttu-id="70752-108">[IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) pour les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="70752-108">[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) for transport providers.</span></span> 
    
<span data-ttu-id="70752-109">Ces méthodes ont des implémentations similaires.</span><span class="sxs-lookup"><span data-stu-id="70752-109">These methods have similar implementations.</span></span> <span data-ttu-id="70752-110">Les principales tâches qu'une méthode de fermeture de session effectue sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="70752-110">The main tasks that a logoff method performs are as follows:</span></span>
  
- <span data-ttu-id="70752-111">La publication de tous les objets ouverts, y compris les objets de sous-objets et d'État.</span><span class="sxs-lookup"><span data-stu-id="70752-111">Releasing all open objects, including subobjects and status objects.</span></span>
    
- <span data-ttu-id="70752-112">Appel de la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l'objet de prise en charge pour décrémenter son décompte de références.</span><span class="sxs-lookup"><span data-stu-id="70752-112">Calling the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="70752-113">Suppression de toutes les structures [MAPIUID](mapiuid.md) enregistrées du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="70752-113">Removing all of your provider's registered [MAPIUID](mapiuid.md) structures.</span></span> 
    
- <span data-ttu-id="70752-114">Suppression de la ligne de votre fournisseur dans le tableau d'État.</span><span class="sxs-lookup"><span data-stu-id="70752-114">Removing your provider's row in the status table.</span></span>
    
- <span data-ttu-id="70752-115">Effectuer toutes les tâches liées au nettoyage des ressources, telles que les suivantes:</span><span class="sxs-lookup"><span data-stu-id="70752-115">Performing any tasks that relate to cleaning up resources, such as the following:</span></span>
    
  - <span data-ttu-id="70752-116">Arrêt d'une connexion à un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="70752-116">Terminating a connection with a remote server.</span></span>
    
  - <span data-ttu-id="70752-117">Décrémentation du décompte de références sur l'objet d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="70752-117">Decrementing the reference count on the logon object.</span></span>
    
  - <span data-ttu-id="70752-118">Suppression de l'objet Logon de la liste des objets d'ouverture de session que votre fournisseur stocke.</span><span class="sxs-lookup"><span data-stu-id="70752-118">Removing the logon object from the list of logon objects that your provider stores.</span></span>
    
  - <span data-ttu-id="70752-119">En mode de débogage, l'émission de traces pour localiser des objets ayant divulgué de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="70752-119">In debug mode, issuing traces to locate objects that have leaked memory.</span></span>
    
<span data-ttu-id="70752-120">Lorsque votre méthode de fermeture de session est renvoyée, MAPI appelle les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="70752-120">When your logoff method returns, MAPI calls the following:</span></span>
  
- <span data-ttu-id="70752-121">La méthode **IUnknown:: Release** de votre objet d'ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="70752-121">Your logon object's **IUnknown::Release** method.</span></span> 
    
- <span data-ttu-id="70752-122">La méthode d' **arrêt** de votre objet fournisseur pour effectuer les tâches de nettoyage finales.</span><span class="sxs-lookup"><span data-stu-id="70752-122">Your provider object's **Shutdown** method to perform any final cleanup tasks.</span></span> <span data-ttu-id="70752-123">Selon le type de votre fournisseur, l'une des méthodes suivantes est appelée:</span><span class="sxs-lookup"><span data-stu-id="70752-123">Depending on the type of your provider, one of the following methods is called:</span></span> 
    
  - <span data-ttu-id="70752-124">[IABProvider:: Shutdown](iabprovider-shutdown.md) pour les fournisseurs de carnets d'adresses</span><span class="sxs-lookup"><span data-stu-id="70752-124">[IABProvider::Shutdown](iabprovider-shutdown.md) for address book providers</span></span> 
    
  - <span data-ttu-id="70752-125">[IMSProvider:: Shutdown](imsprovider-shutdown.md) pour les fournisseurs de banque de messages</span><span class="sxs-lookup"><span data-stu-id="70752-125">[IMSProvider::Shutdown](imsprovider-shutdown.md) for message store providers</span></span> 
    
  - <span data-ttu-id="70752-126">[IXPProvider:: arrêt](ixpprovider-shutdown.md) pour les fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="70752-126">[IXPProvider::Shutdown](ixpprovider-shutdown.md) for transport providers</span></span> 
    
- <span data-ttu-id="70752-127">La méthode **IUnknown:: Release** de votre objet fournisseur.</span><span class="sxs-lookup"><span data-stu-id="70752-127">Your provider object's **IUnknown::Release** method.</span></span> 
    
<span data-ttu-id="70752-128">Si votre fournisseur est une banque de messages, un appel client à [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) lancera également le processus d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="70752-128">If your provider is a message store, a client call to [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) will also initiate the shutdown process.</span></span> <span data-ttu-id="70752-129">**StoreLogoff** ferme un fournisseur de banque de messages particulier et n'a aucun effet sur la session.</span><span class="sxs-lookup"><span data-stu-id="70752-129">**StoreLogoff** shuts down one particular message store provider and has no effect on the session.</span></span> <span data-ttu-id="70752-130">Seul un fournisseur de banque de messages peut être arrêté avec cette méthode; Il n'existe pas de méthode explicite pour arrêter un carnet d'adresses ou un fournisseur de transport particulier.</span><span class="sxs-lookup"><span data-stu-id="70752-130">Only a message store provider can be shut down with this method; there is no explicit way to shut down a particular address book or transport provider.</span></span> <span data-ttu-id="70752-131">Pour plus d'informations sur la façon de répondre à un appel **StoreLogoff** , consultez la rubrique [arrêt d'un fournisseur de banque de messages](shutting-down-a-message-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="70752-131">For information about how to respond to a **StoreLogoff** call, see [Shutting Down a Message Store Provider](shutting-down-a-message-store-provider.md).</span></span>
  
<span data-ttu-id="70752-132">La DLL de votre fournisseur est déchargée lorsque MAPI appelle la fonction de l'API Win32 **FreeLibrary**, un appel passé après le dernier client actif a appelé [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="70752-132">Your provider's DLL will be unloaded when MAPI calls the Win32 API function **FreeLibrary**, a call that is made after the last active client has called [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="70752-133">À ce stade, votre fournisseur de services aura terminé l'arrêt.</span><span class="sxs-lookup"><span data-stu-id="70752-133">By this time, your service provider will have finished shutting down.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70752-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70752-134">See also</span></span>



[<span data-ttu-id="70752-135">Fournisseurs de services MAPI</span><span class="sxs-lookup"><span data-stu-id="70752-135">MAPI Service Providers</span></span>](mapi-service-providers.md)

