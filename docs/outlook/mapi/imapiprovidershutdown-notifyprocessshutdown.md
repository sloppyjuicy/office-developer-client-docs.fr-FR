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
ms.openlocfilehash: 251359a98f89c88e707e4f705bd94b1f30b32cbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592051"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="14cbd-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="14cbd-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="14cbd-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14cbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14cbd-105">Indique au fournisseur MAPI qu’un client MAPI sur le point d’effectuer un arrêt rapide, afin que le fournisseur peut prendre des mesures pour éviter toute perte de données.</span><span class="sxs-lookup"><span data-stu-id="14cbd-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="14cbd-106">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="14cbd-106">Return value</span></span>

<span data-ttu-id="14cbd-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="14cbd-107">S_OK</span></span>
  
> <span data-ttu-id="14cbd-108">Le fournisseur MAPI est en cours d’actions pour éviter toute perte de données lorsque le client MAPI s’arrête.</span><span class="sxs-lookup"><span data-stu-id="14cbd-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14cbd-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14cbd-109">See also</span></span>



[<span data-ttu-id="14cbd-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14cbd-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="14cbd-111">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="14cbd-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

