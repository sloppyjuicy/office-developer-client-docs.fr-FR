---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405246"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="d22d8-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="d22d8-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="d22d8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d22d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d22d8-105">Indique au fournisseur MAPI qu'un client MAPI va effectuer un arrêt rapide, afin que le fournisseur puisse prendre des mesures pour empêcher toute perte de données.</span><span class="sxs-lookup"><span data-stu-id="d22d8-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="d22d8-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d22d8-106">Return value</span></span>

<span data-ttu-id="d22d8-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="d22d8-107">S_OK</span></span>
  
> <span data-ttu-id="d22d8-108">Le fournisseur MAPI prend des mesures pour empêcher la perte de données lors de l'arrêt du client MAPI.</span><span class="sxs-lookup"><span data-stu-id="d22d8-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d22d8-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d22d8-109">See also</span></span>



[<span data-ttu-id="d22d8-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d22d8-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="d22d8-111">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="d22d8-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

