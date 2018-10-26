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
ms.openlocfilehash: 1c66032788758b04558a37a4c35ff4dd6c702fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568265"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="54232-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="54232-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="54232-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54232-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54232-105">Indique l’intention de poursuivre du client MAPI arrêté.</span><span class="sxs-lookup"><span data-stu-id="54232-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="54232-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54232-106">Return value</span></span>

<span data-ttu-id="54232-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="54232-107">S_OK</span></span>
  
> <span data-ttu-id="54232-108">Le sous-système MAPI a tenté d’informer les fournisseurs MAPI chargés que le client MAPI sur le point d’effectuer un arrêt rapide.</span><span class="sxs-lookup"><span data-stu-id="54232-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="54232-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="54232-109">Remarks</span></span>

<span data-ttu-id="54232-110">Pour éviter toute perte de données à partir de l’arrêt rapide d’un client MAPI, les clients MAPI doivent appeler les méthodes **IMAPIClientShutdown::NotifyProcessShutdown** et [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) en fonction du résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="54232-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="54232-111">Pour plus d’informations, voir [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="54232-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54232-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54232-112">See also</span></span>



[<span data-ttu-id="54232-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54232-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="54232-114">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="54232-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

