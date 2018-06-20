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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: e0a34e1cc0b1da1b5e2127d0697cce472c8530c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784054"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="b7bb9-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="b7bb9-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="b7bb9-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7bb9-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="b7bb9-105">Informe Microsoft Outlook que la synchronisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="b7bb9-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="b7bb9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7bb9-106">Parameters</span></span>

 <span data-ttu-id="b7bb9-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="b7bb9-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="b7bb9-108">Un événement qui est passé précédent pour permettre à Microsoft Outlook fermer le handle.</span><span class="sxs-lookup"><span data-stu-id="b7bb9-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="b7bb9-109">Il peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="b7bb9-109">It can be NULL.</span></span>
    
 <span data-ttu-id="b7bb9-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="b7bb9-110">**hResult**</span></span>
  
> <span data-ttu-id="b7bb9-111">Une valeur HRESULT indiquant l’état final de la progression.</span><span class="sxs-lookup"><span data-stu-id="b7bb9-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b7bb9-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b7bb9-112">Return value</span></span>

<span data-ttu-id="b7bb9-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7bb9-113">S_OK</span></span> 
  
> <span data-ttu-id="b7bb9-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b7bb9-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7bb9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7bb9-115">See also</span></span>



[<span data-ttu-id="b7bb9-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7bb9-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

