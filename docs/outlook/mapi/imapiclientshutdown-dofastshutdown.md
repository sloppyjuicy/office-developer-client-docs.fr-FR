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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 447832d88a9740875fcf39a32adcf4ebb99e05ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783690"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="e01a6-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="e01a6-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="e01a6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e01a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e01a6-105">Indique l’intention du client MAPI pour quitter le processus de client immédiatement.</span><span class="sxs-lookup"><span data-stu-id="e01a6-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="e01a6-106">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e01a6-106">Return value</span></span>

<span data-ttu-id="e01a6-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="e01a6-107">S_OK</span></span>
  
> <span data-ttu-id="e01a6-108">Le sous-système MAPI a indiqué pour les fournisseurs MAPI chargés que le client MAPI vient de quitter immédiatement, et les fournisseurs MAPI sont prêts pour la sortie du client.</span><span class="sxs-lookup"><span data-stu-id="e01a6-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="e01a6-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e01a6-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="e01a6-110">Le sous-système MAPI ne gère pas l’arrêt rapide du client.</span><span class="sxs-lookup"><span data-stu-id="e01a6-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e01a6-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="e01a6-111">Remarks</span></span>

<span data-ttu-id="e01a6-112">Pour éviter toute perte de données à partir de l’arrêt rapide d’un client MAPI, les clients MAPI doivent appeler les méthodes [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) et **IMAPIClientShutdown::DoFastShutdown** en fonction du résultat S_OK renvoyé par le sous-système MAPI dans la méthode [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="e01a6-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="e01a6-113">Pour plus d’informations, voir [Meilleures pratiques pour l’arrêt rapide](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="e01a6-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e01a6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e01a6-114">See also</span></span>



[<span data-ttu-id="e01a6-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e01a6-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="e01a6-116">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="e01a6-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

