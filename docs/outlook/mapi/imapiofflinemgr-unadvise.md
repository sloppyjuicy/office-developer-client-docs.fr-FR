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
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579521"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="3ea7a-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="3ea7a-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="3ea7a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ea7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ea7a-105">Annule des rappels pour un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3ea7a-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="3ea7a-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="3ea7a-106">Parameters</span></span>

 <span data-ttu-id="3ea7a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ea7a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3ea7a-108">[in] Indicateurs d’annulation de rappel.</span><span class="sxs-lookup"><span data-stu-id="3ea7a-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="3ea7a-109">Seule la valeur MAPIOFFLINE_UNADVISE_DEFAULT est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3ea7a-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="3ea7a-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="3ea7a-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="3ea7a-111">[in] Un jeton advise qui identifie l’inscription du rappel qui doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="3ea7a-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3ea7a-112">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3ea7a-112">Return value</span></span>

<span data-ttu-id="3ea7a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ea7a-113">S_OK</span></span>
  
> <span data-ttu-id="3ea7a-114">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="3ea7a-114">The call was successful.</span></span> <span data-ttu-id="3ea7a-115">Cet appel doit renvoyer S_OK.</span><span class="sxs-lookup"><span data-stu-id="3ea7a-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ea7a-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3ea7a-116">Remarks</span></span>

<span data-ttu-id="3ea7a-117">Supprime l’inscription du rappel qui a été associé avec *ulAdviseToken* renvoyé à partir d’un appel précédent à **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="3ea7a-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="3ea7a-118">Entraîne l’objet **IMAPIOfflineMgr** libérer sa référence à l’objet **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associé *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="3ea7a-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ea7a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ea7a-119">See also</span></span>



[<span data-ttu-id="3ea7a-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="3ea7a-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="3ea7a-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3ea7a-121">MAPI Constants</span></span>](mapi-constants.md)

