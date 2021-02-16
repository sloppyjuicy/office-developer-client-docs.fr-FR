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
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426918"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="6dd09-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="6dd09-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="6dd09-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dd09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dd09-105">Inscrit un client pour recevoir des rappels sur un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6dd09-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="6dd09-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6dd09-106">Parameters</span></span>

 <span data-ttu-id="6dd09-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6dd09-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="6dd09-108">[in] Indicateurs qui modifient le comportement.</span><span class="sxs-lookup"><span data-stu-id="6dd09-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="6dd09-109">Seule la valeur MAPIOFFLINE_ADVISE_DEFAULT est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6dd09-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="6dd09-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="6dd09-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="6dd09-111">[in] Informations sur le type de rappel, le moment où recevoir un rappel, une interface de rappel pour l’appelant et d’autres détails.</span><span class="sxs-lookup"><span data-stu-id="6dd09-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="6dd09-112">Il contient également un jeton client qu’Outlook utilise pour envoyer des rappels de notification ultérieurs à l’appelant client.</span><span class="sxs-lookup"><span data-stu-id="6dd09-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="6dd09-113">_péAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="6dd09-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="6dd09-114">[out] Jeton de conseil renvoyé à l’appelant client pour annuler ultérieurement le rappel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6dd09-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6dd09-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6dd09-115">Return value</span></span>

<span data-ttu-id="6dd09-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6dd09-116">S_OK</span></span>
  
> <span data-ttu-id="6dd09-117">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="6dd09-117">The call was successful.</span></span>
    
<span data-ttu-id="6dd09-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="6dd09-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="6dd09-119">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="6dd09-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="6dd09-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="6dd09-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="6dd09-121">Interface de rappel spécifiée dans  *pAdviseInfo*  non valide.</span><span class="sxs-lookup"><span data-stu-id="6dd09-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6dd09-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="6dd09-122">Remarks</span></span>

<span data-ttu-id="6dd09-123">Lors de l’ouverture d’un objet hors connexion à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="6dd09-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="6dd09-124">Le client peut vérifier les types de rappels pris en charge par l’objet à l’aide de **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="6dd09-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="6dd09-125">Le client peut déterminer le type et d’autres détails sur le rappel qu’il souhaite, puis appeler **IMAPIOfflineMgr::Advise** pour recevoir ces rappels sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="6dd09-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6dd09-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dd09-126">See also</span></span>



[<span data-ttu-id="6dd09-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="6dd09-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="6dd09-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6dd09-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="6dd09-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6dd09-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="6dd09-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="6dd09-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

