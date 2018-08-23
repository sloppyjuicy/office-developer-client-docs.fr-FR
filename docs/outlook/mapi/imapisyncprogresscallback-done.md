---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cdd3db3f3779c2078b90352e19f8da6b29cffb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573206"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="a592c-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="a592c-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="a592c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a592c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a592c-105">Informe Microsoft Outlook que la synchronisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="a592c-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="a592c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a592c-106">Parameters</span></span>

 <span data-ttu-id="a592c-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="a592c-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="a592c-108">Un événement qui est passé précédent pour permettre à Microsoft Outlook fermer le handle.</span><span class="sxs-lookup"><span data-stu-id="a592c-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="a592c-109">Il peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="a592c-109">It can be NULL.</span></span>
    
 <span data-ttu-id="a592c-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="a592c-110">**hResult**</span></span>
  
> <span data-ttu-id="a592c-111">Une valeur HRESULT indiquant l’état final de la progression.</span><span class="sxs-lookup"><span data-stu-id="a592c-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a592c-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a592c-112">Return value</span></span>

<span data-ttu-id="a592c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a592c-113">S_OK</span></span> 
  
> <span data-ttu-id="a592c-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a592c-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a592c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a592c-115">See also</span></span>



[<span data-ttu-id="a592c-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a592c-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

