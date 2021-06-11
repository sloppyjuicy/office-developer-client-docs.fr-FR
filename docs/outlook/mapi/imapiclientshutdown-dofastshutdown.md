---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408683"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="2d5d2-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="2d5d2-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="2d5d2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d5d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d5d2-105">Indique l’intention du client MAPI de quitter immédiatement le processus client.</span><span class="sxs-lookup"><span data-stu-id="2d5d2-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="2d5d2-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2d5d2-106">Return value</span></span>

<span data-ttu-id="2d5d2-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d5d2-107">S_OK</span></span>
  
> <span data-ttu-id="2d5d2-108">Le sous-système MAPI a indiqué aux fournisseurs MAPI chargés que le client MAPI quitte immédiatement et que les fournisseurs MAPI sont prêts pour la sortie du client.</span><span class="sxs-lookup"><span data-stu-id="2d5d2-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="2d5d2-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2d5d2-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="2d5d2-110">Le sous-système MAPI ne prend pas en charge l’arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="2d5d2-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d5d2-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d5d2-111">Remarks</span></span>

<span data-ttu-id="2d5d2-112">Pour éviter la perte de données suite à l’arrêt rapide d’un client MAPI, les clients MAPI doivent appeler les méthodes [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) et **IMAPIClientShutdown::D oFastShutdown** basées sur le résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md)</span><span class="sxs-lookup"><span data-stu-id="2d5d2-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="2d5d2-113">Pour plus d’informations, voir [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="2d5d2-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d5d2-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d5d2-114">See also</span></span>



[<span data-ttu-id="2d5d2-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d5d2-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="2d5d2-116">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="2d5d2-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

