---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409656"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="76086-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76086-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="76086-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76086-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76086-105">Permet au sous-système MAPI d’informer un fournisseur MAPI de l’arrêt rapide d’un client MAPI, afin que le fournisseur MAPI puisse répondre à l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="76086-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76086-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="76086-106">Header file:</span></span>  <br/> |<span data-ttu-id="76086-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76086-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="76086-108">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="76086-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="76086-109">Objets fournisseur : [IXPProvider,](ixpprovideriunknown.md) [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="76086-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="76086-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="76086-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="76086-111">Fournisseur MAPI</span><span class="sxs-lookup"><span data-stu-id="76086-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="76086-112">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="76086-112">Called by:</span></span>  <br/> |<span data-ttu-id="76086-113">Sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="76086-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="76086-114">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="76086-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="76086-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="76086-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="76086-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="76086-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="76086-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="76086-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="76086-118">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="76086-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="76086-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="76086-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="76086-120">Interroge le fournisseur MAPI pour obtenir une prise en charge de l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="76086-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="76086-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="76086-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="76086-122">Indique au fournisseur MAPI qu’un client MAPI va faire un arrêt rapide, afin que le fournisseur puisse prendre des mesures pour empêcher la perte de données.</span><span class="sxs-lookup"><span data-stu-id="76086-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="76086-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="76086-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="76086-124">Indique au fournisseur MAPI que le client MAPI quitte immédiatement, afin que le fournisseur MAPI continue à apporter des modifications afin d’éviter toute perte de données.</span><span class="sxs-lookup"><span data-stu-id="76086-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76086-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="76086-125">Remarks</span></span>

<span data-ttu-id="76086-126">L’arrêt rapide permet à un client MAPI de quitter son processus dans un court délai, avec un peu de chance une fois que le client et les fournisseurs MAPI chargés ont enregistré les paramètres et les données MAPI.</span><span class="sxs-lookup"><span data-stu-id="76086-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="76086-127">Le client MAPI lance toujours un arrêt rapide et doit interroger le sous-système MAPI pour obtenir la prise en charge de l’arrêt rapide des fournisseurs MAPI chargés.</span><span class="sxs-lookup"><span data-stu-id="76086-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="76086-128">Un administrateur peut définir le Registre Windows au niveau de l’utilisateur pour spécifier le niveau de prise en charge du fournisseur nécessaire pour autoriser l’arrêt rapide de tous les clients MAPI.</span><span class="sxs-lookup"><span data-stu-id="76086-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="76086-129">Pour plus d’informations sur les paramètres du Registre, voir Options utilisateur d’arrêt [rapide.](fast-shutdown-user-options.md)</span><span class="sxs-lookup"><span data-stu-id="76086-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="76086-130">Toutefois, pour que l’arrêt rapide se produise sans perte de données, les fournisseurs MAPI doivent implémenter l’interface **IMAPIProviderShutdown.**</span><span class="sxs-lookup"><span data-stu-id="76086-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="76086-131">Un fournisseur MAPI qui doit prendre en charge l’arrêt rapide du client doit renvoyer S_OK au sous-système MAPI dans la méthode **IMAPIProviderShutdown::QueryFastShutdown.**</span><span class="sxs-lookup"><span data-stu-id="76086-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="76086-132">Lorsque le sous-système MAPI appelle par la suite les méthodes **IMAPIProviderShutdown::NotifyProcessShutdown** et **IMAPIProviderShutdown::D oFastShutdown,** le fournisseur MAPI doit prendre les mesures nécessaires pour enregistrer les données et paramètres MAPI et préparer la sortie du client.</span><span class="sxs-lookup"><span data-stu-id="76086-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="76086-133">Les fournisseurs MAPI qui n’ont pas besoin de prendre en charge l’arrêt rapide du client doivent toujours implémenter l’interface **IMAPIProviderShutdown** et faire en retour la méthode **IMAPIProviderShutdown::QueryFastShutdown** MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="76086-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="76086-134">Pour Outlook en tant que client MAPI, Outlook attend alors que toutes les références externes soient publiées avant de se quitter.</span><span class="sxs-lookup"><span data-stu-id="76086-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="76086-135">Selon le paramètre de Registre Windows de l’utilisateur pour un arrêt rapide, le fait de ne pas implémenter l’interface **IMAPIProviderShutdown** n’empêche pas nécessairement un arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="76086-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="76086-136">Pour plus d’informations sur le processus d’arrêt rapide, voir [Vue d’ensemble de l’arrêt rapide.](fast-shutdown-overview.md)</span><span class="sxs-lookup"><span data-stu-id="76086-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="76086-137">Pour plus d’informations sur la réalisation d’un arrêt rapide, voir [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="76086-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="76086-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76086-138">See also</span></span>



[<span data-ttu-id="76086-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="76086-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="76086-140">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="76086-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

