---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 80010ca19999ba519f051e914f02f240abb524e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424930"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="683c6-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="683c6-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="683c6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="683c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="683c6-105">Fournit les détails affichés dans la boîte de dialogue d'envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="683c6-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="683c6-106">Si des erreurs sont rencontrées lors de la synchronisation, le fournisseur Store appelle cette fonction.</span><span class="sxs-lookup"><span data-stu-id="683c6-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="683c6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="683c6-107">Parameters</span></span>

 <span data-ttu-id="683c6-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="683c6-108">**hResult**</span></span>
  
> <span data-ttu-id="683c6-109">HRESULT de l'erreur ou de l'avertissement.</span><span class="sxs-lookup"><span data-stu-id="683c6-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="683c6-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="683c6-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="683c6-111">Pointeur vers la chaîne associée à l'erreur à afficher.</span><span class="sxs-lookup"><span data-stu-id="683c6-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="683c6-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="683c6-112">Return value</span></span>

<span data-ttu-id="683c6-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="683c6-113">S_OK</span></span> 
  
> <span data-ttu-id="683c6-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="683c6-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="683c6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="683c6-115">See also</span></span>



[<span data-ttu-id="683c6-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="683c6-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

