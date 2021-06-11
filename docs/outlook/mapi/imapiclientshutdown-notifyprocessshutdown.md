---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438868"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="eb4b4-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="eb4b4-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="eb4b4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb4b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb4b4-105">Indique l’intention du client MAPI de poursuivre l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="eb4b4-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eb4b4-106">Return value</span></span>

<span data-ttu-id="eb4b4-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb4b4-107">S_OK</span></span>
  
> <span data-ttu-id="eb4b4-108">Le sous-système MAPI a tenté d’informer les fournisseurs MAPI chargés que le client MAPI va faire un arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="eb4b4-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb4b4-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="eb4b4-109">Remarks</span></span>

<span data-ttu-id="eb4b4-110">Pour éviter la perte de données suite à l’arrêt rapide d’un client MAPI, les clients MAPI doivent appeler les méthodes **IMAPIClientShutdown::NotifyProcessShutdown** et [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) basées sur le résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md)</span><span class="sxs-lookup"><span data-stu-id="eb4b4-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="eb4b4-111">Pour plus d’informations, voir [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="eb4b4-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb4b4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb4b4-112">See also</span></span>



[<span data-ttu-id="eb4b4-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb4b4-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="eb4b4-114">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="eb4b4-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

