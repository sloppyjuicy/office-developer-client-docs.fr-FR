---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418217"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="ce9b9-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="ce9b9-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="ce9b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce9b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce9b9-105">Interroge le fournisseur MAPI pour obtenir une prise en charge de l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="ce9b9-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="ce9b9-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ce9b9-106">Return value</span></span>

<span data-ttu-id="ce9b9-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce9b9-107">S_OK</span></span>
  
> <span data-ttu-id="ce9b9-108">Le fournisseur MAPI prend en charge le client MAPI pour un arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="ce9b9-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="ce9b9-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ce9b9-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="ce9b9-110">Le fournisseur MAPI ne prend pas en charge le client MAPI pour un arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="ce9b9-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce9b9-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="ce9b9-111">Remarks</span></span>

<span data-ttu-id="ce9b9-112">Les fournisseurs MAPI qui n’ont pas besoin de prendre en charge l’arrêt rapide du client doivent toujours implémenter l’interface [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) et faire en quoi la méthode **IMAPIProviderShutdown::QueryFastShutdown** doit être MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="ce9b9-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="ce9b9-113">Pour Outlook client MAPI, cela entraîne Outlook attendre que toutes les références externes soient libérées avant de se quitter.</span><span class="sxs-lookup"><span data-stu-id="ce9b9-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="ce9b9-114">Selon le paramètre de Registre Windows de l’utilisateur pour un arrêt rapide, le fait de ne pas implémenter l’interface **IMAPIProviderShutdown** n’empêche pas nécessairement un arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="ce9b9-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce9b9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce9b9-115">See also</span></span>



[<span data-ttu-id="ce9b9-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce9b9-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="ce9b9-117">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="ce9b9-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

