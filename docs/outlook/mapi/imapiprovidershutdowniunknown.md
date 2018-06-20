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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a679d04f7697abbe0172105febf87082c0cd9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783950"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="fa582-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa582-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="fa582-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa582-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa582-105">Permet le sous-système MAPI informer un fournisseur MAPI de l’arrêt rapide d’un client MAPI, afin que le fournisseur MAPI peut répondre à l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="fa582-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa582-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fa582-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa582-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa582-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fa582-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="fa582-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="fa582-109">Objets du fournisseur : [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="fa582-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="fa582-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="fa582-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa582-111">Fournisseur MAPI</span><span class="sxs-lookup"><span data-stu-id="fa582-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="fa582-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="fa582-112">Called by:</span></span>  <br/> |<span data-ttu-id="fa582-113">Sous-système MAPI</span><span class="sxs-lookup"><span data-stu-id="fa582-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="fa582-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="fa582-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fa582-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="fa582-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="fa582-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="fa582-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="fa582-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="fa582-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fa582-118">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="fa582-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="fa582-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="fa582-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="fa582-120">Requêtes le fournisseur MAPI pour arrêt rapide prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="fa582-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="fa582-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="fa582-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="fa582-122">Indique au fournisseur MAPI qu’un client MAPI sur le point d’effectuer un arrêt rapide, afin que le fournisseur peut prendre des mesures pour éviter toute perte de données.</span><span class="sxs-lookup"><span data-stu-id="fa582-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="fa582-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="fa582-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="fa582-124">Indique au fournisseur MAPI que le client MAPI va s’arrêter immédiatement, afin que le fournisseur MAPI maintient les modifications pour éviter toute perte de données.</span><span class="sxs-lookup"><span data-stu-id="fa582-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa582-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa582-125">Remarks</span></span>

<span data-ttu-id="fa582-126">Arrêt rapide permet à un client MAPI quitter son processus au sein d’un court instant, j’espère que lorsque le client et le chargement fournisseurs MAPI ont enregistré données et paramètres MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa582-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="fa582-127">Le client MAPI toujours initie un arrêt rapide et doit interroger le sous-système MAPI pour la prise en charge de l’arrêt rapide des fournisseurs MAPI chargés.</span><span class="sxs-lookup"><span data-stu-id="fa582-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="fa582-128">Un administrateur peut définir le Registre Windows au niveau de l’utilisateur de spécifier le niveau de prise en charge de fournisseur qui est nécessaire pour permettre l’arrêt rapide de tous les clients MAPI.</span><span class="sxs-lookup"><span data-stu-id="fa582-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="fa582-129">Pour plus d’informations sur les paramètres de Registre, voir [Options d’utilisateur de l’arrêt rapide](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="fa582-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="fa582-130">Toutefois, pour l’arrêt rapide se produise correctement sans perte de données, fournisseurs MAPI doivent implémenter l’interface **IMAPIProviderShutdown** .</span><span class="sxs-lookup"><span data-stu-id="fa582-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="fa582-131">Un fournisseur MAPI qui doit prendre en charge l’arrêt rapide client doit renvoyer S_OK au sous-système MAPI dans la méthode **IMAPIProviderShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="fa582-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="fa582-132">Lorsque le sous-système MAPI appelle ensuite les méthodes **IMAPIProviderShutdown::NotifyProcessShutdown** et **IMAPIProviderShutdown::DoFastShutdown** , le fournisseur MAPI doit prendre des mesures nécessaires pour enregistrer les données et les paramètres MAPI et Préparez la sortie du client.</span><span class="sxs-lookup"><span data-stu-id="fa582-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="fa582-133">Fournisseurs MAPI qui n’ont pas besoin pour prendre en charge l’arrêt rapide client doivent toujours implémenter l’interface **IMAPIProviderShutdown** et que la méthode de **IMAPIProviderShutdown::QueryFastShutdown** renvoie MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="fa582-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="fa582-134">Pour Outlook en tant qu’un client MAPI, cela entraîne à attendre que toutes les références externes doit être publié avant de quitter Outlook.</span><span class="sxs-lookup"><span data-stu-id="fa582-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="fa582-135">Dans le Registre Windows de l’utilisateur en fonction de paramètre d’arrêt rapide, ne pas l’implémentation de l’interface **IMAPIProviderShutdown** n’empêche pas nécessairement un arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="fa582-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="fa582-136">Pour plus d’informations sur le processus d’arrêt rapide, voir [Vue d’ensemble rapide de l’arrêt](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fa582-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="fa582-137">Pour plus d’informations sur la façon d’effectuer correctement arrêt rapide, voir [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="fa582-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa582-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa582-138">See also</span></span>



[<span data-ttu-id="fa582-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="fa582-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="fa582-140">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="fa582-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

