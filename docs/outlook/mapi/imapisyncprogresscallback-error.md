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
ms.openlocfilehash: 8cff424e3b589af292e56cef1ca19198e9c80d1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594984"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="b9a4b-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="b9a4b-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="b9a4b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9a4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9a4b-105">Fournit des informations qui sont affichent dans la boîte de dialogue d’envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="b9a4b-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="b9a4b-106">Si vous rencontrez des erreurs lors de la synchronisation, le fournisseur de banque appelle cette fonction.</span><span class="sxs-lookup"><span data-stu-id="b9a4b-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="b9a4b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9a4b-107">Parameters</span></span>

 <span data-ttu-id="b9a4b-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="b9a4b-108">**hResult**</span></span>
  
> <span data-ttu-id="b9a4b-109">HRESULT de l’erreur ou avertissement.</span><span class="sxs-lookup"><span data-stu-id="b9a4b-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="b9a4b-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="b9a4b-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="b9a4b-111">Pointeur vers la chaîne associée à l’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b9a4b-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b9a4b-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b9a4b-112">Return value</span></span>

<span data-ttu-id="b9a4b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9a4b-113">S_OK</span></span> 
  
> <span data-ttu-id="b9a4b-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b9a4b-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9a4b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9a4b-115">See also</span></span>



[<span data-ttu-id="b9a4b-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9a4b-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

