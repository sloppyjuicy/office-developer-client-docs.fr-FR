---
title: Options d’arrêt rapide utilisateur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Dernière modification : 26 juin 2012'
ms.openlocfilehash: a58f8b98ab2f5a5c1028440676a561427272d028
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783277"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="c8af4-103">Options d’arrêt rapide utilisateur</span><span class="sxs-lookup"><span data-stu-id="c8af4-103">Fast shutdown user options</span></span>

<span data-ttu-id="c8af4-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c8af4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c8af4-105">Cette rubrique décrit les trois paramètres du Registre Windows qui sont disponibles, démarrage de Microsoft Outlook 2010 et maintenant, y compris Microsoft Outlook 2013, pour l’arrêt rapide des clients MAPI de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8af4-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="c8af4-106">Les administrateurs peuvent utiliser ces paramètres de Registre pour spécifier le comportement de l’arrêt de client par défaut en fonction de la prise en charge des fournisseurs MAPI pour arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="c8af4-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="c8af4-107">L’administrateur, à son tour, détermine comment le sous-système MAPI répond aux appels du client MAPI à [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) en termes de prise en charge de l’arrêt rapide disponibles.</span><span class="sxs-lookup"><span data-stu-id="c8af4-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="c8af4-108">Même si un paramètre de Registre reflète la préférence de l’administrateur au niveau de l’utilisateur pour l’arrêt rapide pour tous les clients MAPI, un développeur de client MAPI peut décider si le client prend en charge l’arrêt rapide indépendamment des autres clients MAPI et paramètre de Registre de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c8af4-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="c8af4-109">Néanmoins, pour l’arrêt rapide se déroule correctement, l’utilisateur doit avoir le paramètre de Registre nécessaires, un client MAPI doit initier l’arrêt rapide à l’aide de la [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface et fournisseurs MAPI qui fonctionnent avec le client doit implémenter la [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface pour prendre en charge l’arrêt rapide de client.</span><span class="sxs-lookup"><span data-stu-id="c8af4-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="c8af4-110">La liste suivante décrit les trois options de niveau utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8af4-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="c8af4-111">Option 1 : Le sous-système MAPI permet d’arrêt rapide, sauf si les fournisseurs MAPI exclure explicitement</span><span class="sxs-lookup"><span data-stu-id="c8af4-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="c8af4-112">À compter d’Outlook 2010, il s’agit du comportement par défaut lorsque Outlook est le client MAPI ; Il n’est pas nécessairement le comportement par défaut pour les autres clients MAPI.</span><span class="sxs-lookup"><span data-stu-id="c8af4-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="c8af4-113">Pour spécifier explicitement cette option pour Outlook, les administrateurs peuvent choisir définir la valeur et la clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="c8af4-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="c8af4-114">Clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="c8af4-114">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="c8af4-115">Valeur :</span><span class="sxs-lookup"><span data-stu-id="c8af4-115">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="c8af4-116">Lorsqu’un client MAPI initie un arrêt rapide et appelle **IMAPIClientShutdown::QueryFastShutdown** à la requête pour la prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en retournant S\_OK tant qu’aucun fournisseur MAPI qui possède un MAPI active session avec le client MAPI a choisi explicitement en dehors de la prise en charge de l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="c8af4-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="c8af4-117">Un fournisseur MAPI choisit en dehors de l’arrêt rapide en implémentant la méthode [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) renvoie une erreur (MAPI\_E\_non\_prise en charge).</span><span class="sxs-lookup"><span data-stu-id="c8af4-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="c8af4-118">Si un ou plusieurs fournisseurs MAPI renvoient une erreur dans **IMAPIProviderShutdown::QueryFastShutdown**, le sous-système MAPI renvoie MAPI_\E_\NO\_ **IMAPIClientShutdown::QueryFastShutdown**prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c8af4-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="c8af4-119">Sauf si un fournisseur MAPI exclut, la renvoie du sous-système MAPI S\_OK, même si un ou plusieurs fournisseurs n’ont pas implémenté la **IMAPIProviderShutdown : IUnknown** interface.</span><span class="sxs-lookup"><span data-stu-id="c8af4-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="c8af4-120">Option 2 : Le sous-système MAPI permet d’arrêt rapide uniquement si tous les fournisseurs MAPI choisit explicitement dans</span><span class="sxs-lookup"><span data-stu-id="c8af4-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="c8af4-121">Les administrateurs doivent définir explicitement la clé de Registre suivante et une valeur pour spécifier cette préférence pour arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="c8af4-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="c8af4-122">Clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="c8af4-122">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="c8af4-123">Valeur :</span><span class="sxs-lookup"><span data-stu-id="c8af4-123">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="c8af4-124">Lorsqu’un client MAPI initie un arrêt rapide et appelle **IMAPIClientShutdown::QueryFastShutdown** à la requête pour la prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en retournant S\_OK si tous les fournisseurs MAPI qui ont des sessions actives avec l’arrêt MAPI client prise en charge rapide.</span><span class="sxs-lookup"><span data-stu-id="c8af4-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="c8af4-125">Un fournisseur MAPI illustre la prise en charge par l’implémentation **IMAPIProviderShutdown::QueryFastShutdown** pour renvoyer un code d’erreur non (S\_OK).</span><span class="sxs-lookup"><span data-stu-id="c8af4-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="c8af4-126">Si un ou plusieurs de ces fournisseurs MAPI renvoient MAPI\_E\_non\_prise en charge, ou qui n’implémentent pas **IMAPIProviderShutdown::QueryFastShutdown**, le sous-système MAPI retourne un code d’erreur à **IMAPIClientShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="c8af4-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="c8af4-127">Option 3 : Un administrateur désactive la prise en charge de l’arrêt rapide client</span><span class="sxs-lookup"><span data-stu-id="c8af4-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="c8af4-128">Les administrateurs doivent définir explicitement la clé de Registre suivante et une valeur pour désactiver la prise en charge de l’arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="c8af4-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="c8af4-129">Clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="c8af4-129">Registry key:</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="c8af4-130">Valeur :</span><span class="sxs-lookup"><span data-stu-id="c8af4-130">Value:</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="c8af4-131">Lorsqu’un client MAPI initie un arrêt rapide et appelle **IMAPIClientShutdown::QueryFastShutdown** à la requête pour la prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en retournant MAPI_E_NO_SUPPORT, quel que soit si tout fournisseur MAPI prend en charge rapide de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="c8af4-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="c8af4-132">Sous ce paramètre de Registre, le sous-système MAPI appelle jamais la méthode **IMAPIProviderShutdown::QueryFastShutdown** ou [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) d’un des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="c8af4-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c8af4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8af4-133">See also</span></span>

- [<span data-ttu-id="c8af4-134">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="c8af4-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="c8af4-135">Vue d’ensemble de l’arrêt rapide</span><span class="sxs-lookup"><span data-stu-id="c8af4-135">Fast Shutdown Overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="c8af4-136">Meilleures pratiques pour l’arrêt rapide</span><span class="sxs-lookup"><span data-stu-id="c8af4-136">Best Practices for Fast Shutdown</span></span>](best-practices-for-fast-shutdown.md)

