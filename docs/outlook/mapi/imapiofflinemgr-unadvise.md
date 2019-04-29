---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404854"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="ca1f3-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ca1f3-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="ca1f3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca1f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca1f3-105">Annule les rappels pour un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="ca1f3-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="ca1f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca1f3-106">Parameters</span></span>

 <span data-ttu-id="ca1f3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca1f3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ca1f3-108">dans Indicateurs pour l'annulation du rappel.</span><span class="sxs-lookup"><span data-stu-id="ca1f3-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="ca1f3-109">Seule la valeur MAPIOFFLINE_UNADVISE_DEFAULT est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca1f3-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="ca1f3-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="ca1f3-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="ca1f3-111">dans Un jeton d'avertissement qui identifie l'inscription de rappel qui doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="ca1f3-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ca1f3-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ca1f3-112">Return value</span></span>

<span data-ttu-id="ca1f3-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca1f3-113">S_OK</span></span>
  
> <span data-ttu-id="ca1f3-114">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="ca1f3-114">The call was successful.</span></span> <span data-ttu-id="ca1f3-115">Cet appel doit retourner S_OK.</span><span class="sxs-lookup"><span data-stu-id="ca1f3-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca1f3-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca1f3-116">Remarks</span></span>

<span data-ttu-id="ca1f3-117">Supprime l'inscription pour le rappel associé à *ulAdviseToken* renvoyé par un appel antérieur à **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="ca1f3-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="ca1f3-118">Fait en sorte que l'objet **IMAPIOfflineMgr** libère sa référence sur l'objet **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associé à *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="ca1f3-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca1f3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca1f3-119">See also</span></span>



[<span data-ttu-id="ca1f3-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="ca1f3-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="ca1f3-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ca1f3-121">MAPI Constants</span></span>](mapi-constants.md)

