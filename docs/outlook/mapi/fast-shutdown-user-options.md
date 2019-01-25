---
title: Options utilisateur en cas d’arrêt rapide
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 220aeab5-20f6-4520-96c9-8aaa0e8ea15b
description: 'Dernière modification : 26 juin 2012'
localization_priority: Priority
ms.openlocfilehash: 3c60862733c6b38e60650ae9daba9bba578fcd58
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716368"
---
# <a name="fast-shutdown-user-options"></a><span data-ttu-id="1b92f-103">Options utilisateur en cas d’arrêt rapide</span><span class="sxs-lookup"><span data-stu-id="1b92f-103">Fast shutdown user options</span></span>

<span data-ttu-id="1b92f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b92f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b92f-105">Cette rubrique décrit les trois paramètres de Registre Windows disponibles dans Microsoft Outlook 2010 et désormais dans Microsoft Outlook 2013 pour l’arrêt rapide des clients MAPI d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1b92f-105">This topic describes the three Windows registry settings that are available, starting in Microsoft Outlook 2010 and now including Microsoft Outlook 2013, for fast shutdown of a user's MAPI clients.</span></span> <span data-ttu-id="1b92f-106">Les administrateurs peuvent utiliser ces paramètres de Registre pour spécifier le comportement d’arrêt favori du client en fonction de la prise en charge des fournisseurs MAPI de l’arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="1b92f-106">Administrators can use these registry settings to specify the preferred client shutdown behavior depending on the MAPI providers' support for client fast shutdown.</span></span> <span data-ttu-id="1b92f-107">Le paramètre de l’administrateur, à son tour, détermine comment le sous-système MAPI répond à l’appel du client MAPI à l’interface [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) en matière de prise en charge de l’arrêt rapide disponible.</span><span class="sxs-lookup"><span data-stu-id="1b92f-107">The administrator's setting, in turn, determines how the MAPI subsystem responds to the MAPI client's call to [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) in terms of available fast shutdown support.</span></span> 
  
<span data-ttu-id="1b92f-108">Même si un paramètre de Registre reflète la préférence de l’administrateur au niveau utilisateur pour l’arrêt rapide pour tous les clients MAPI, un développeur client MAPI peut décider si le client prend en charge l’arrêt rapide indépendamment d’autres clients MAPI et du paramètre de Registre de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1b92f-108">Even though a registry setting reflects the administrator's preference at the user level for fast shutdown for all MAPI clients, a MAPI client developer can decide whether the client supports fast shutdown independently of other MAPI clients and the administrator's registry setting.</span></span> <span data-ttu-id="1b92f-109">Néanmoins, pour que l’arrêt rapide ait lieu correctement, l’utilisateur doit disposer du paramètre de Registre nécessaire, un client MAPI doit lancer l’arrêt rapide à l’aide de l’interface [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) et les fournisseurs MAPI qui utilisent le client doivent implémenter l’interface [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) pour prendre en charge l’arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="1b92f-109">Nonetheless, for fast shutdown to take place successfully, the user must have the necessary registry setting, a MAPI client must initiate the fast shutdown by using the [IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md) interface, and MAPI providers that work with the client should implement the [IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md) interface to support client fast shutdown.</span></span> 
  
<span data-ttu-id="1b92f-110">La liste suivante décrit les trois options au niveau utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1b92f-110">The following list describes the three user-level options.</span></span>
  
### <a name="option-1-the-mapi-subsystem-enables-fast-shutdown-unless-mapi-providers-explicitly-opt-out"></a><span data-ttu-id="1b92f-111">Option 1 : le sous-système MAPI active l’arrêt rapide, sauf si les fournisseurs MAPI le désactivent explicitement</span><span class="sxs-lookup"><span data-stu-id="1b92f-111">Option 1: The MAPI subsystem enables fast shutdown, unless MAPI providers explicitly opt out</span></span> 
    
<span data-ttu-id="1b92f-112">À partir d’Outlook 2010, il s’agit du comportement par défaut si Outlook est le client MAPI. Ce n’est pas nécessairement le comportement par défaut pour d’autres clients MAPI.</span><span class="sxs-lookup"><span data-stu-id="1b92f-112">Starting in Outlook 2010, this is the default behavior when Outlook is the MAPI client; it is not necessarily the default behavior for other MAPI clients.</span></span> <span data-ttu-id="1b92f-113">Pour spécifier explicitement cette option pour Outlook, les administrateurs peuvent choisir de définir la valeur et la clé de Registre suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b92f-113">To explicitly specify this option for Outlook, administrators can choose to set the following registry key and value.</span></span>
    
<span data-ttu-id="1b92f-114">Clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="1b92f-114"> registry key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="1b92f-115">Valeur :</span><span class="sxs-lookup"><span data-stu-id="1b92f-115">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000000`
    
<span data-ttu-id="1b92f-116">Lorsqu’un client MAPI lance un arrêt rapide et appelle l’interface **IMAPIClientShutdown::QueryFastShutdown** pour effectuer une requête pour une prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en renvoyant S\_OK tant qu’aucun fournisseur MAPI ayant une session MAPI active avec le client MAPI n’a désactivé explicitement la prise en charge de l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="1b92f-116">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK as long as no MAPI provider that has an active MAPI session with the MAPI client has explicitly opted out of fast shutdown support.</span></span> 

<span data-ttu-id="1b92f-117">Un fournisseur MAPI désactive l’arrêt rapide en implémentant la méthode [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) pour qu’elle renvoie une erreur (MAPI\_E\_NO\_SUPPORT).</span><span class="sxs-lookup"><span data-stu-id="1b92f-117">A MAPI provider opts out of fast shutdown by implementing the [IMAPIProviderShutdown::QueryFastShutdown](imapiprovidershutdown-queryfastshutdown.md) method to return an error (MAPI\_E\_NO\_SUPPORT).</span></span> <span data-ttu-id="1b92f-118">Si un ou plusieurs fournisseurs MAPI renvoient une erreur dans **IMAPIProviderShutdown::QueryFastShutdown**, le sous-système MAPI renvoie MAPI_\E_\NO\_SUPPORT à **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="1b92f-118">If one or more MAPI providers return an error in **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns MAPI_\E_\NO\_SUPPORT to **IMAPIClientShutdown::QueryFastShutdown**.</span></span> 

<span data-ttu-id="1b92f-119">Sauf si un fournisseur MAPI désactive l’arrêt rapide, le sous-système MAPI renvoie S\_OK, même si un ou plusieurs fournisseurs n’ont pas implémenté l’interface **IMAPIProviderShutdown : IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="1b92f-119">Unless a MAPI provider opts out, the MAPI subsystem returns S\_OK, even if one or more providers have not implemented the **IMAPIProviderShutdown : IUnknown** interface.</span></span> 
    
### <a name="option-2-the-mapi-subsystem-enables-fast-shutdown-only-if-every-mapi-provider-explicitly-opts-in"></a><span data-ttu-id="1b92f-120">Option 2 : le sous-système MAPI active l’arrêt rapide uniquement si chaque fournisseur MAPI l’active explicitement</span><span class="sxs-lookup"><span data-stu-id="1b92f-120">Option 2: The MAPI subsystem enables fast shutdown only if every MAPI provider explicitly opts in</span></span> 
    
<span data-ttu-id="1b92f-121">Les administrateurs doivent explicitement définir la valeur et la clé de Registre suivantes pour spécifier cette préférence pour l’arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="1b92f-121">Administrators must explicitly set the following registry key and value to specify this preference for client fast shutdown.</span></span>
    
<span data-ttu-id="1b92f-122">Clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="1b92f-122"> registry key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="1b92f-123">Valeur :</span><span class="sxs-lookup"><span data-stu-id="1b92f-123">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000001`
    
<span data-ttu-id="1b92f-124">Lorsqu’un client MAPI lance un arrêt rapide et appelle l’interface **IMAPIClientShutdown::QueryFastShutdown** pour effectuer une requête pour une prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en renvoyant S\_OK si tous les fournisseurs MAPI ayant des sessions actives avec le client MAPI prennent en charge l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="1b92f-124">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning S\_OK if all MAPI providers that have active sessions with the MAPI client support fast shutdown.</span></span> <span data-ttu-id="1b92f-125">Un fournisseur MAPI démontre sa prise en charge en implémentant **IMAPIProviderShutdown::QueryFastShutdown** de façon à renvoyer un code de non-erreur (S\_OK).</span><span class="sxs-lookup"><span data-stu-id="1b92f-125">A MAPI provider demonstrates its support by implementing **IMAPIProviderShutdown::QueryFastShutdown** to return a non-error code (S\_OK).</span></span> 

<span data-ttu-id="1b92f-126">Si un ou plusieurs de ces fournisseurs MAPI renvoient MAPI\_E\_NO\_SUPPORT ou n’implémentent pas **IMAPIProviderShutdown::QueryFastShutdown**, le sous-système MAPI renvoie un code d’erreur à **IMAPIClientShutdown::QueryFastShutdown**.</span><span class="sxs-lookup"><span data-stu-id="1b92f-126">If one or more such MAPI providers return MAPI\_E\_NO\_SUPPORT, or do not implement **IMAPIProviderShutdown::QueryFastShutdown**, the MAPI subsystem returns an error code to **IMAPIClientShutdown::QueryFastShutdown**.</span></span>
    
### <a name="option-3-an-administrator-disables-support-for-client-fast-shutdown"></a><span data-ttu-id="1b92f-127">Option 3 : un administrateur désactive la prise en charge de l’arrêt rapide du client</span><span class="sxs-lookup"><span data-stu-id="1b92f-127">Option 3: An administrator disables support for client fast shutdown</span></span>
    
<span data-ttu-id="1b92f-128">Les administrateurs doivent explicitement définir la valeur et la clé de Registre suivantes pour désactiver la prise en charge pour l’arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="1b92f-128">Administrators must explicitly set the following registry key and value to disable support for client fast shutdown.</span></span>
    
<span data-ttu-id="1b92f-129">Clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="1b92f-129"> registry key</span></span>
  
>  `[HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\14.0\Outlook\Options\Shutdown]`
    
<span data-ttu-id="1b92f-130">Valeur :</span><span class="sxs-lookup"><span data-stu-id="1b92f-130">Value</span></span>
  
>  `"FastShutdownBehavior"=dword:00000002`
    
<span data-ttu-id="1b92f-131">Lorsqu’un client MAPI lance un arrêt rapide et appelle l’interface **IMAPIClientShutdown::QueryFastShutdown** pour effectuer une requête pour une prise en charge de l’arrêt rapide, le sous-système MAPI répond à la requête en renvoyant MAPI_E_NO_SUPPORT, indépendamment du fait qu’un fournisseur MAPI prenne en charge l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="1b92f-131">When a MAPI client initiates a fast shutdown and calls **IMAPIClientShutdown::QueryFastShutdown** to query for fast shutdown support, the MAPI subsystem responds to the query by returning MAPI_E_NO_SUPPORT, regardless of whether any MAPI provider supports fast shutdown.</span></span> <span data-ttu-id="1b92f-132">Sous ce paramètre de Registre, le sous-système MAPI n’appelle jamais la méthode **IMAPIProviderShutdown::QueryFastShutdown** ou [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) de l’un des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="1b92f-132">Under this registry setting, the MAPI subsystem never calls the **IMAPIProviderShutdown::QueryFastShutdown** or [IMAPIProviderShutdown::DoFastShutdown](imapiprovidershutdown-dofastshutdown.md) method of any of the providers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1b92f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b92f-133">See also</span></span>

- [<span data-ttu-id="1b92f-134">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="1b92f-134">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)
- [<span data-ttu-id="1b92f-135">Présentation de l’arrêt rapide</span><span class="sxs-lookup"><span data-stu-id="1b92f-135">Fast shutdown overview</span></span>](fast-shutdown-overview.md)
- [<span data-ttu-id="1b92f-136">Meilleures pratiques en cas d’arrêt rapide</span><span class="sxs-lookup"><span data-stu-id="1b92f-136">Best practices for fast shutdown</span></span>](best-practices-for-fast-shutdown.md)

