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
ms.openlocfilehash: 8d397e12b8b24c5031e6e6d89d98134d487a815b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422347"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="af12d-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="af12d-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="af12d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af12d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="af12d-105">Informe Microsoft Outlook que la synchronisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="af12d-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="af12d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af12d-106">Parameters</span></span>

 <span data-ttu-id="af12d-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="af12d-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="af12d-108">Événement transmis pour permettre à Microsoft Outlook de fermer le handle.</span><span class="sxs-lookup"><span data-stu-id="af12d-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="af12d-109">Elle peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="af12d-109">It can be NULL.</span></span>
    
 <span data-ttu-id="af12d-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="af12d-110">**hResult**</span></span>
  
> <span data-ttu-id="af12d-111">HRESULT indiquant l’état final de la progression.</span><span class="sxs-lookup"><span data-stu-id="af12d-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="af12d-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af12d-112">Return value</span></span>

<span data-ttu-id="af12d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="af12d-113">S_OK</span></span> 
  
> <span data-ttu-id="af12d-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="af12d-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af12d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af12d-115">See also</span></span>



[<span data-ttu-id="af12d-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af12d-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

