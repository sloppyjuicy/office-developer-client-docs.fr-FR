---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 784a2f497811ba7c4ba0abf260ff32fde75de76a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584932"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="e76dc-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="e76dc-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="e76dc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e76dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e76dc-105">Requêtes du sous-système MAPI pour arrêt rapide prennent en charge fournie par les fournisseurs MAPI chargés.</span><span class="sxs-lookup"><span data-stu-id="e76dc-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="e76dc-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e76dc-106">Return value</span></span>

<span data-ttu-id="e76dc-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="e76dc-107">S_OK</span></span>
  
> <span data-ttu-id="e76dc-108">Le sous-système MAPI prend en charge le client MAPI pour rapide de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e76dc-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="e76dc-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e76dc-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="e76dc-110">Le fournisseur MAPI ne gère pas le client MAPI pour rapide de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e76dc-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e76dc-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="e76dc-111">Remarks</span></span>

<span data-ttu-id="e76dc-112">Si le sous-système MAPI prend en charge le client MAPI à rapide d’arrêt dépend du paramètre de Registre Windows de l’utilisateur ou le comportement par défaut du client MAPI pour l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="e76dc-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="e76dc-113">Cela dépend également la possibilité des fournisseurs MAPI chargés pour prendre en charge l’arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="e76dc-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="e76dc-114">Pour plus d’informations, voir [Options d’utilisateur de l’arrêt rapide](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="e76dc-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e76dc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e76dc-115">See also</span></span>



[<span data-ttu-id="e76dc-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e76dc-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="e76dc-117">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="e76dc-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

