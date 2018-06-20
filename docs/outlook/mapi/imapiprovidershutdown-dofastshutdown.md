---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7c38f0650315495875357862f5fa7fe138d2c61b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783900"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="146d8-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="146d8-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="146d8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="146d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="146d8-105">Indique au fournisseur MAPI que le client MAPI va s’arrêter immédiatement, afin que le fournisseur MAPI maintient les modifications pour éviter toute perte de données.</span><span class="sxs-lookup"><span data-stu-id="146d8-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="146d8-106">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="146d8-106">Return value</span></span>

<span data-ttu-id="146d8-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="146d8-107">S_OK</span></span>
  
> <span data-ttu-id="146d8-108">Le fournisseur MAPI est prêt pour le client MAPI quitter immédiatement.</span><span class="sxs-lookup"><span data-stu-id="146d8-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="146d8-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="146d8-109">See also</span></span>



[<span data-ttu-id="146d8-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="146d8-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="146d8-111">Arrêt du client dans MAPI</span><span class="sxs-lookup"><span data-stu-id="146d8-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

