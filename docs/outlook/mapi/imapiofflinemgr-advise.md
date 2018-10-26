---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e0c8c4c6251581506c7bdd78c009bb12e8291c81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586934"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="71a47-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="71a47-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="71a47-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71a47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71a47-105">Enregistre un client pour recevoir des rappels sur un objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="71a47-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="71a47-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="71a47-106">Parameters</span></span>

 <span data-ttu-id="71a47-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="71a47-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="71a47-108">[in] Indicateurs qui modifient le comportement.</span><span class="sxs-lookup"><span data-stu-id="71a47-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="71a47-109">Seule la valeur MAPIOFFLINE_ADVISE_DEFAULT est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="71a47-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="71a47-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="71a47-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="71a47-111">[in] Informations sur le type de rappel, quand recevoir un rappel, une interface de rappel pour l’appelant et d’autres détails.</span><span class="sxs-lookup"><span data-stu-id="71a47-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="71a47-112">Il contient également un jeton client par l’envoi de rappels de notification suivants à l’appelant client Outlook.</span><span class="sxs-lookup"><span data-stu-id="71a47-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="71a47-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="71a47-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="71a47-114">[out] Un jeton advise est renvoyé à l’appelant de client d’annulation par la suite de rappel pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="71a47-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="71a47-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71a47-115">Return value</span></span>

<span data-ttu-id="71a47-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="71a47-116">S_OK</span></span>
  
> <span data-ttu-id="71a47-117">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="71a47-117">The call was successful.</span></span>
    
<span data-ttu-id="71a47-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="71a47-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="71a47-119">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="71a47-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="71a47-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="71a47-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="71a47-121">L’interface de rappel spécifié dans *pAdviseInfo* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="71a47-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="71a47-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="71a47-122">Remarks</span></span>

<span data-ttu-id="71a47-123">À l’ouverture d’un objet en mode hors connexion à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client obtient un objet en mode hors connexion qui prend en charge **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="71a47-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="71a47-124">Le client peut vérifier les types de rappels pris en charge par l’objet à l’aide de **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="71a47-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="71a47-125">Le client peut déterminer le type et autres détails sur le rappel il souhaite et ensuite appeler **IMAPIOfflineMgr::Advise** s’inscrire pour recevoir ces rappels sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="71a47-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="71a47-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71a47-126">See also</span></span>



[<span data-ttu-id="71a47-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="71a47-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="71a47-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="71a47-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="71a47-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="71a47-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="71a47-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="71a47-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

