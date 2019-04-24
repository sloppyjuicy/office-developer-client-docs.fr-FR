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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321426"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="0c6fc-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="0c6fc-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="0c6fc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c6fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c6fc-105">Inscrit un client pour recevoir des rappels sur un objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="0c6fc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c6fc-106">Parameters</span></span>

 <span data-ttu-id="0c6fc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c6fc-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="0c6fc-108">dans Indicateurs qui modifient le comportement.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="0c6fc-109">Seule la valeur MAPIOFFLINE_ADVISE_DEFAULT est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="0c6fc-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="0c6fc-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="0c6fc-111">dans Informations sur le type de rappel, le moment auquel il faut recevoir un rappel, une interface de rappel pour l'appelant et d'autres détails.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="0c6fc-112">Il contient également un jeton client utilisé par Outlook lors de l'envoi de rappels de notification par la suite à l'appelant du client.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="0c6fc-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="0c6fc-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="0c6fc-114">remarquer Jeton d'avertissement renvoyé à l'appelant client pour l'annulation ultérieure du rappel pour l'objet.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c6fc-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0c6fc-115">Return value</span></span>

<span data-ttu-id="0c6fc-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c6fc-116">S_OK</span></span>
  
> <span data-ttu-id="0c6fc-117">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-117">The call was successful.</span></span>
    
<span data-ttu-id="0c6fc-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0c6fc-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="0c6fc-119">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="0c6fc-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="0c6fc-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="0c6fc-121">L'interface de rappel spécifiée dans *pAdviseInfo* n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c6fc-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c6fc-122">Remarks</span></span>

<span data-ttu-id="0c6fc-123">Lors de l'ouverture d'un objet hors connexion à l'aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="0c6fc-124">Le client peut vérifier les types de rappels pris en charge par l'objet à l'aide de **[IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="0c6fc-125">Le client peut déterminer le type et d'autres détails sur le rappel souhaité, puis appeler **IMAPIOfflineMgr:: Advise** pour recevoir ces rappels à propos de l'objet.</span><span class="sxs-lookup"><span data-stu-id="0c6fc-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c6fc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c6fc-126">See also</span></span>



[<span data-ttu-id="0c6fc-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="0c6fc-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="0c6fc-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0c6fc-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="0c6fc-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0c6fc-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="0c6fc-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="0c6fc-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

