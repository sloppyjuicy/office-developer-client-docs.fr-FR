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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783877"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="2d631-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="2d631-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="2d631-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d631-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d631-105">Annule des rappels pour un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2d631-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="2d631-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="2d631-106">Parameters</span></span>

 <span data-ttu-id="2d631-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2d631-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2d631-108">[in] Indicateurs d’annulation de rappel.</span><span class="sxs-lookup"><span data-stu-id="2d631-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="2d631-109">Seule la valeur MAPIOFFLINE_UNADVISE_DEFAULT est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2d631-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="2d631-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="2d631-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="2d631-111">[in] Un jeton advise qui identifie l’inscription du rappel qui doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="2d631-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2d631-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2d631-112">Return value</span></span>

<span data-ttu-id="2d631-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d631-113">S_OK</span></span>
  
> <span data-ttu-id="2d631-114">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="2d631-114">The call was successful.</span></span> <span data-ttu-id="2d631-115">Cet appel doit renvoyer S_OK.</span><span class="sxs-lookup"><span data-stu-id="2d631-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d631-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d631-116">Remarks</span></span>

<span data-ttu-id="2d631-117">Supprime l’inscription du rappel qui a été associé avec *ulAdviseToken* renvoyé à partir d’un appel précédent à **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="2d631-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="2d631-118">Entraîne l’objet **IMAPIOfflineMgr** libérer sa référence à l’objet **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associé *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="2d631-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d631-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d631-119">See also</span></span>



[<span data-ttu-id="2d631-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="2d631-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="2d631-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="2d631-121">MAPI Constants</span></span>](mapi-constants.md)

