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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350903"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="dae15-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="dae15-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="dae15-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dae15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dae15-105">Indique l'intention du client MAPI de quitter immédiatement le processus client.</span><span class="sxs-lookup"><span data-stu-id="dae15-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="dae15-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dae15-106">Return value</span></span>

<span data-ttu-id="dae15-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="dae15-107">S_OK</span></span>
  
> <span data-ttu-id="dae15-108">Le sous-système MAPI a indiqué à charger des fournisseurs MAPI que le client MAPI quitte immédiatement, et les fournisseurs MAPI sont prêts pour la fermeture du client.</span><span class="sxs-lookup"><span data-stu-id="dae15-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="dae15-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="dae15-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="dae15-110">Le sous-système MAPI ne prend pas en charge l'arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="dae15-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dae15-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="dae15-111">Remarks</span></span>

<span data-ttu-id="dae15-112">Pour éviter toute perte de données lors de l'arrêt rapide d'un client MAPI, les clients MAPI doivent appeler les [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) et **IMAPIClientShutdown::D ofastshutdown** méthodes basées sur le résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="dae15-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="dae15-113">Pour plus d'informations, consultez la rubrique [meilleures pratiques pour l'arrêt rapide](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="dae15-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dae15-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dae15-114">See also</span></span>



[<span data-ttu-id="dae15-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dae15-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="dae15-116">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="dae15-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

