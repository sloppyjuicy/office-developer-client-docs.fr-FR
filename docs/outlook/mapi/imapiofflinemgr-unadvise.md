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
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="a8dbf-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a8dbf-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="a8dbf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8dbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8dbf-105">Annule les rappels pour un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="a8dbf-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="a8dbf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8dbf-106">Parameters</span></span>

 <span data-ttu-id="a8dbf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8dbf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a8dbf-108">[in] Indicateurs pour l’annulation du rappel.</span><span class="sxs-lookup"><span data-stu-id="a8dbf-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="a8dbf-109">Seule la valeur MAPIOFFLINE_UNADVISE_DEFAULT est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a8dbf-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="a8dbf-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="a8dbf-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="a8dbf-111">[in] Jeton de conseil qui identifie l’inscription de rappel à annuler.</span><span class="sxs-lookup"><span data-stu-id="a8dbf-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a8dbf-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a8dbf-112">Return value</span></span>

<span data-ttu-id="a8dbf-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8dbf-113">S_OK</span></span>
  
> <span data-ttu-id="a8dbf-114">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="a8dbf-114">The call was successful.</span></span> <span data-ttu-id="a8dbf-115">Cet appel doit renvoyer S_OK.</span><span class="sxs-lookup"><span data-stu-id="a8dbf-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8dbf-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a8dbf-116">Remarks</span></span>

<span data-ttu-id="a8dbf-117">Supprime l’inscription pour le rappel qui était associé à  *ulAdviseToken*  renvoyé à partir d’un appel précédent à **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="a8dbf-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="a8dbf-118">Entraîne **l’objet IMAPIOfflineMgr** à libérer sa référence sur l’objet **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associé  *à ulAdviseToken*  .</span><span class="sxs-lookup"><span data-stu-id="a8dbf-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8dbf-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8dbf-119">See also</span></span>



[<span data-ttu-id="a8dbf-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="a8dbf-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="a8dbf-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a8dbf-121">MAPI Constants</span></span>](mapi-constants.md)

