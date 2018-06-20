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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9dc368e6502bbb14cf42f6bc5a08fd2893f98bf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784049"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="791b6-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="791b6-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="791b6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="791b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="791b6-105">Fournit des informations qui sont affichent dans la boîte de dialogue d’envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="791b6-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="791b6-106">Si vous rencontrez des erreurs lors de la synchronisation, le fournisseur de banque appelle cette fonction.</span><span class="sxs-lookup"><span data-stu-id="791b6-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="791b6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="791b6-107">Parameters</span></span>

 <span data-ttu-id="791b6-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="791b6-108">**hResult**</span></span>
  
> <span data-ttu-id="791b6-109">HRESULT de l’erreur ou avertissement.</span><span class="sxs-lookup"><span data-stu-id="791b6-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="791b6-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="791b6-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="791b6-111">Pointeur vers la chaîne associée à l’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="791b6-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="791b6-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="791b6-112">Return value</span></span>

<span data-ttu-id="791b6-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="791b6-113">S_OK</span></span> 
  
> <span data-ttu-id="791b6-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="791b6-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="791b6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="791b6-115">See also</span></span>



[<span data-ttu-id="791b6-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="791b6-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

