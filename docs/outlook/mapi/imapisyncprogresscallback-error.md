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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 80010ca19999ba519f051e914f02f240abb524e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341334"
---
# <a name="imapisyncprogresscallbackerror"></a><span data-ttu-id="8b757-103">IMAPISyncProgressCallback::Error</span><span class="sxs-lookup"><span data-stu-id="8b757-103">IMAPISyncProgressCallback::Error</span></span>

  
  
<span data-ttu-id="8b757-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b757-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b757-105">Fournit les détails affichés dans la boîte de dialogue d'envoi/réception.</span><span class="sxs-lookup"><span data-stu-id="8b757-105">Provides details that are displayed in the Send/Receive dialog.</span></span> <span data-ttu-id="8b757-106">Si des erreurs sont rencontrées lors de la synchronisation, le fournisseur Store appelle cette fonction.</span><span class="sxs-lookup"><span data-stu-id="8b757-106">If errors are encountered during synchronization, the store provider calls this function.</span></span>
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a><span data-ttu-id="8b757-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b757-107">Parameters</span></span>

 <span data-ttu-id="8b757-108">**hResult**</span><span class="sxs-lookup"><span data-stu-id="8b757-108">**hResult**</span></span>
  
> <span data-ttu-id="8b757-109">HRESULT de l'erreur ou de l'avertissement.</span><span class="sxs-lookup"><span data-stu-id="8b757-109">The HRESULT of the error or warning.</span></span>
    
 <span data-ttu-id="8b757-110">**pwcszErrorStr**</span><span class="sxs-lookup"><span data-stu-id="8b757-110">**pwcszErrorStr**</span></span>
  
> <span data-ttu-id="8b757-111">Pointeur vers la chaîne associée à l'erreur à afficher.</span><span class="sxs-lookup"><span data-stu-id="8b757-111">A pointer to the string associated with the error to be displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b757-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b757-112">Return value</span></span>

<span data-ttu-id="8b757-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b757-113">S_OK</span></span> 
  
> <span data-ttu-id="8b757-114">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="8b757-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b757-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b757-115">See also</span></span>



[<span data-ttu-id="8b757-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b757-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

